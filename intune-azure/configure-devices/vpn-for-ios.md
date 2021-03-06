---
title: "Configuración de VPN de Intune para dispositivos iOS"
titleSuffix: Intune Azure preview
description: "Versión preliminar de Intune Azure: aprenda sobre la configuración de Intune que puede usar para configurar conexiones VPN en dispositivos iOS."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 02/15/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 1447c123-ea33-4ea0-aab4-69577cdb8d00
ms.reviewer: karanda
ms.suite: ems
ms.custom: intune-azure
translationtype: Human Translation
ms.sourcegitcommit: 153cce3809e24303b8f88a833e2fc7bdd9428a4a
ms.openlocfilehash: 5b450c74a5c6353219393e10acf69ba9e61a2ccb
ms.lasthandoff: 02/18/2017


---

# <a name="vpn-settings-for-ios-devices-in-microsoft-intune"></a>Configuración de VPN para dispositivos iOS en Microsoft Intune

[!INCLUDE[azure_preview](../includes/azure_preview.md)]

Según la configuración que elija, no todos los valores de la siguiente lista se pueden configurar.

## <a name="base-vpn-settings"></a>Configuración de VPN base


**Connection name** (Nombre de la conexión): escriba un nombre para esta conexión. Los usuarios finales verán este nombre cuando exploren su dispositivo para ver la lista de conexiones VPN disponibles.
- **Dirección IP o FQDN**: proporcione la dirección IP o el nombre de dominio completo del servidor VPN al que se conectarán los dispositivos. Ejemplos: **192.168.1.1**, **vpn.contoso.com**.
- **Método de autenticación**: elija cómo se autenticarán los dispositivos en el servidor VPN. Las opciones son:
    - **Certificados**: en **Certificado de autenticación**, elija un perfil de certificado SCEP o PKCS que anteriormente creó para autenticar la conexión. Para más información sobre los perfiles de certificado, consulte [Configuración de certificados](how-to-configure-certificates.md).
    - **Nombre de usuario y contraseña**: los usuarios finales debe proporcionar un nombre de usuario y una contraseña para iniciar sesión en el servidor VPN.
- **Tipo de conexión**: seleccione el tipo de conexión VPN de la siguiente lista de proveedores:
    - **Check Point Capsule VPN**
    - **Cisco AnyConnect**
    - **Dell SonicWALL Mobile Connect**
    - **F5 Edge Client**
    - **Pulse Secure**
    - **Cisco (IPSec)**
    - **Citrix**
    - **VPN personalizada**
- **Tunelización dividida** - : puede **Habilitar** o **Deshabilitar** esta opción, que permite que los dispositivos decidan qué conexión usar en función del tráfico. Por ejemplo, un usuario en un hotel usará la conexión VPN para acceder a los archivos de trabajo, pero usará la red normal del hotel para la exploración web habitual.


## <a name="custom-vpn-settings"></a>Configuración de VPN personalizada

Si seleccionó **VPN personalizada** como el tipo de conexión, configure además estas opciones:

- **Identificador de VPN**: es un identificador de la aplicación VPN que usa, y lo suministra el proveedor de VPN.
- **Especifique pares clave-valor para los atributos de la VPN personalizada**: agregue o importe **claves** y **valores** que personalicen su conexión VPN. De nuevo, estos valores los suministra normalmente el proveedor de VPN.

## <a name="apps-per-app-vpn-settings"></a>Configuración de aplicaciones (VPN por aplicación)

- **VPN por aplicación**: habilite esta opción si quiere definir las direcciones URL que permitirán la conexión VPN cuando se visiten desde el explorador Safari. Para configurar esta opción, debe haber seleccionado **Certificados** como método de autenticación en la configuración de VPN base.
- **Especifique las direcciones URL que permitirán la conexión VPN al usar el explorador de Safari**: haga clic en esta opción para agregar una o varias direcciones URL de sitios web. Cuando se visitan estas direcciones URL; la conexión VPN se habilita.

- **Reglas a petición**: esta opción le permite configurar reglas condicionales que controlan cuándo se inicia la conexión VPN. Por ejemplo, podría crear una condición en la que la conexión VPN solo se usa cuando un dispositivo no está conectado a una de las redes Wi-Fi de empresa. Otra alternativa es crear una condición en la que, si un dispositivo no puede tener acceso a un dominio de búsqueda DNS que especifique, entonces no se inicia la conexión VPN.

    - **SSIDs or DNS search domains** (SSID o dominios de búsqueda de DNS): seleccione si esta condición usará **SSID** de red inalámbrica o **dominios de búsqueda de DNS**. Elija Agregar para configurar uno o varios SSID o dominios de búsqueda.
    - **Sondeo de cadena de dirección URL**: opcionalmente, proporcione una dirección URL que la regla usa como prueba. Si el dispositivo en el que está instalado este perfil puede acceder a esta dirección URL sin redirección, se iniciará la conexión VPN y el dispositivo se conectará a la dirección URL de destino. El usuario no verá el sitio de sondeo de cadena de dirección URL. Un ejemplo de un sondeo de cadena de dirección URL es la dirección de un servidor web de auditoría que comprueba el cumplimiento del dispositivo antes de conectarse a la VPN. Otra posibilidad es que la dirección URL comprueba la capacidad de la VPN para conectarse a un sitio, antes de conectar el dispositivo a la dirección URL de destino a través de VPN.
    - **Acción del dominio**: elija una de las siguientes:
        - Conectarse si es necesario 
        - No conectarse nunca 
    - **Acción**: elija una de las opciones siguientes:
        - Conectar 
        - Evaluar conexión 
        - Omitir 
        - Desconectar 


## <a name="proxy-settings"></a>Configuración del proxy

- **Script de configuración automática**: use un archivo para configurar el servidor proxy. Escriba la **dirección URL del servidor proxy** (por ejemplo **http://proxy.contoso.com**) que contiene el archivo de configuración.
- **Dirección**: escriba la dirección del servidor proxy (como una dirección IP).
- **Número de puerto**: especifique el número de puerto asociado con el servidor proxy.

