---
title: Crear un perfil de Wi-Fi con una clave precompartida
titleSuffix: Intune Azure preview
description: "Versión preliminar de Intune Azure: use un perfil personalizado de Intune para crear un perfil de Wi-Fi con una clave precompartida."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: c6fd72a6-7dc8-48fc-9df1-db5627a51597
ms.reviewer: karanda
ms.suite: ems
ms.custom: intune-azure
ms.translationtype: Human Translation
ms.sourcegitcommit: a9748a0ad6b9bbe10e36ba133ba74edb6aa6e09a
ms.openlocfilehash: d318b8c1b6ba6ac73920e3f55519ae0472cb570c
ms.contentlocale: es-es
ms.lasthandoff: 05/05/2017



---
# <a name="use-a-microsoft-intune-custom-device-profile-to-create-a-wi-fi-profile-with-a-pre-shared-key"></a>Uso de un perfil de dispositivo personalizado de Microsoft Intune para crear un perfil de Wi-Fi con una clave precompartida
[!INCLUDE[azure_preview](../includes/azure_preview.md)]

En este tema se explica cómo usar **Custom device profiles** (Personalizar perfiles de dispositivo) para crear un perfil de Wi-Fi con una clave precompartida. Además, se incluye un ejemplo de cómo crear un perfil de Wi-Fi basado en EAP.

> [!NOTE]
-    Le resultará más fácil copiar el código desde un equipo que esté conectado a esa red, tal como se describe a continuación.
- En Android también tiene la opción de usar la herramienta [Android PSK Generator](http://johnathonb.com/2015/05/intune-android-pre-shared-key-generator/) proporcionado por Johnathon Biersack.
-    Puede agregar varias redes y claves si agrega más configuraciones de OMA-URI.
-  En iOS, use Apple Configurator en una estación Mac para configurar el perfil. También puede usar la herramienta [iOS PSK Mobile Config Generator](http://johnathonb.com/2015/05/intune-ios-psk-mobile-config-generator/) proporcionado por Johnathon Biersack.


1.    Para crear un perfil de Wi-Fi con una clave precompartida para Android o Windows o un perfil de Wi-Fi basado en EAP, cuando cree una directiva, elija **Personalizada** para esa plataforma de dispositivo, en lugar de seleccionar un perfil de Wi-Fi.

2.    Proporcione un nombre y una descripción.
3.    Agregue una nueva configuración OMA-URI:

   a.    Escriba un nombre para esta configuración de red Wi-Fi.

   b.    Escriba una descripción de la configuración OMA-URI o deje este campo en blanco.

   c.    **Tipo de datos**: establezca esta opción en **Cadena**.

   d.    **OMA-URI**:

    - **Para Android**: ./Vendor/MSFT/WiFi/Profile/<SSID>/Settings
    - **Para Windows**: ./Vendor/MSFT/WiFi/Profile/MyNetwork/WlanXml

    > [!NOTE]
Asegúrese de incluir el carácter de punto al principio.

    SSID es el SSID para el que va a crear la directiva. Por ejemplo, `./Vendor/MSFT/WiFi/Profile/Hotspot-1/Settings`

  e. **Campo de valor** es donde se pega el código XML. A continuación se muestra un ejemplo. Cada valor debe adaptarse a la configuración de red. En la sección de comentarios del código puede consultar información útil.
4. Elija **Aceptar**, guarde y, luego, asigne la directiva.

    > [!NOTE]
    > Esta directiva solo se puede asignar a grupos de usuarios.

La siguiente vez que se registre cada dispositivo, se aplicará la directiva y se creará un perfil de Wi-Fi en el dispositivo. El dispositivo podrá conectarse a la red automáticamente.

## <a name="android-or-windows-wi-fi-profile"></a>Perfil de Wi-Fi de Windows o Android

Este es un ejemplo del código XML de un perfil de Wi-Fi de Android o Windows:

> [!IMPORTANT]
>
> `<protected>false</protected>`debe establecerse en **false**, ya que **true** podría hacer que el dispositivo esperara una contraseña cifrada y luego intentara descifrarla, lo que podría dar lugar a un error de conexión.
>
>  `<hex>53534944</hex>` se debe establecer en el valor hexadecimal de `<name><SSID of wifi profile></name>`.
>  Los dispositivos Windows 10 pueden devolver un falso error *0x87D1FDE8 Error de corrección*, pero aun así se aprovisionarán con el perfil.

```
<!--
<Name of wifi profile> = Name of profile
<SSID of wifi profile> = Plain text of SSID. Does not need to be escaped, could be <name>Your Company's Network</name>
<nonBroadcast><true/false></nonBroadcast>
<Type of authentication> = Type of authentication used by the network, such as WPA2PSK.
<Type of encryption> = Type of encryption used by the network
<protected>false</protected> do not change this value, as true could cause device to expect an encrypted password and then try to decrypt it, which may result in a failed connection.
<password> = Password to connect to the network
x>53534944</hex> should be set to the hexadecimal value of <name><SSID of wifi profile></name>
-->
<WLANProfile
xmlns="http://www.microsoft.com/networking/WLAN/profile/v1">
  <name><Name of wifi profile></name>
  <SSIDConfig>
    <SSID>
      <hex>53534944</hex>
 <name><SSID of wifi profile></name>
    </SSID>
    <nonBroadcast>false</nonBroadcast>
  </SSIDConfig>
  <connectionType>ESS</connectionType>
  <connectionMode>auto</connectionMode>
  <autoSwitch>false</autoSwitch>
  <MSM>
    <security>
      <authEncryption>
        <authentication><Type of authentication></authentication>
        <encryption><Type of encryption></encryption>
        <useOneX>false</useOneX>
      </authEncryption>
      <sharedKey>
        <keyType>networkKey</keyType>
        <protected>false</protected>
        <keyMaterial>MyPassword</keyMaterial>
      </sharedKey>
      <keyIndex>0</keyIndex>
    </security>
  </MSM>
</WLANProfile>
```

## <a name="eap-based-wi-fi-profile"></a>Perfil de Wi-Fi basado en EAP
Este es un ejemplo del código XML de un perfil de Wi-Fi basado en EAP:

```
    <WLANProfile xmlns="http://www.microsoft.com/networking/WLAN/profile/v1">
      <name>testcert</name>
      <SSIDConfig>
        <SSID>
          <hex>7465737463657274</hex>
          <name>testcert</name>
        </SSID>
        <nonBroadcast>true</nonBroadcast>
      </SSIDConfig>
      <connectionType>ESS</connectionType>
      <connectionMode>auto</connectionMode>
      <autoSwitch>false</autoSwitch>
      <MSM>
        <security>
          <authEncryption>
            <authentication>WPA2</authentication>
            <encryption>AES</encryption>
            <useOneX>true</useOneX>
            <FIPSMode     xmlns="http://www.microsoft.com/networking/WLAN/profile/v2">false</FIPSMode>
          </authEncryption>
          <PMKCacheMode>disabled</PMKCacheMode>
          <OneX xmlns="http://www.microsoft.com/networking/OneX/v1">
            <cacheUserData>false</cacheUserData>
            <authMode>user</authMode>
            <EAPConfig>
              <EapHostConfig     xmlns="http://www.microsoft.com/provisioning/EapHostConfig">
                <EapMethod>
                  <Type xmlns="http://www.microsoft.com/provisioning/EapCommon">13</Type>
                  <VendorId xmlns="http://www.microsoft.com/provisioning/EapCommon">0</VendorId>
                  <VendorType xmlns="http://www.microsoft.com/provisioning/EapCommon">0</VendorType>
                  <AuthorId xmlns="http://www.microsoft.com/provisioning/EapCommon">0</AuthorId>
                </EapMethod>
                <Config xmlns="http://www.microsoft.com/provisioning/EapHostConfig">
                  <Eap xmlns="http://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1">
                    <Type>13</Type>
                    <EapType xmlns="http://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV1">
                      <CredentialsSource>
                        <CertificateStore>
                          <SimpleCertSelection>true</SimpleCertSelection>
                        </CertificateStore>
                      </CredentialsSource>
                      <ServerValidation>
                        <DisableUserPromptForServerValidation>false</DisableUserPromptForServerValidation>
                        <ServerNames></ServerNames>
                      </ServerValidation>
                      <DifferentUsername>false</DifferentUsername>
                      <PerformServerValidation xmlns="http://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV2">false</PerformServerValidation>
                      <AcceptServerName xmlns="http://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV2">false</AcceptServerName>
                      <TLSExtensions xmlns="http://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV2">
                        <FilteringInfo xmlns="http://www.microsoft.com/provisioning/EapTlsConnectionPropertiesV3">
                          <AllPurposeEnabled>true</AllPurposeEnabled>
                          <CAHashList Enabled="true">
                            <IssuerHash>75 f5 06 9c a4 12 0e 9b db bc a1 d9 9d d0 f0 75 fa 3b b8 78 </IssuerHash>
                          </CAHashList>
                          <EKUMapping>
                            <EKUMap>
                              <EKUName>Client Authentication</EKUName>
                              <EKUOID>1.3.6.1.5.5.7.3.2</EKUOID>
                            </EKUMap>
                          </EKUMapping>
                          <ClientAuthEKUList Enabled="true"/>
                          <AnyPurposeEKUList Enabled="false">
                            <EKUMapInList>
                              <EKUName>Client Authentication</EKUName>
                            </EKUMapInList>
                          </AnyPurposeEKUList>
                        </FilteringInfo>
                      </TLSExtensions>
                    </EapType>
                  </Eap>
                </Config>
              </EapHostConfig>
            </EAPConfig>
          </OneX>
        </security>
      </MSM>
    </WLANProfile>
```

## <a name="create-the-xml-file-from-an-existing-wi-fi-connection"></a>Crear el archivo XML desde una conexión Wi-Fi existente
También puede crear un archivo XML desde una conexión Wi-Fi existente:
1. En un equipo que esté conectado a la red inalámbrica o que recientemente se haya conectado a ella, abra la carpeta siguiente: C:\ProgramData\Microsoft\Wlansvc\Profiles\Interfaces\{guid}.

    Es mejor usar un equipo que no esté conectado a muchas redes inalámbricas, ya que tendrá que examinar todos los perfiles para encontrar el adecuado.
3.     Busque el archivo XML que tenga el nombre correcto.
4.     Cuando haya encontrado el archivo XML correcto, copie y pegue el código XML en el campo de datos de la página de configuración de OMA-URI.

