---
title: Habilitar el acceso a los recursos de empresa | Microsoft Intune
description: "Los perfiles de correo electrónico, Wi-Fi y VPN funcionan de manera conjunta para ayudar a los usuarios a acceder a los archivos y recursos que necesitan."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 11/02/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 3dd8dd4e-e165-4d0c-97b7-b3e86ebab909
ms.reviewer: jeffgilb
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: eeb85a28ea6f99a0123ec5df3b0d476a678b85cb
ms.openlocfilehash: f91c3530599b75093f536fd85eaf21d0b4e86e50


---

# <a name="enable-access-to-company-resources-with-microsoft-intune"></a>Habilitar el acceso a los recursos de empresa con Microsoft Intune
Los perfiles de correo electrónico, Wi-Fi y VPN de Microsoft Intune funcionan de manera conjunta para ayudar a los usuarios a obtener acceso a los archivos y recursos que necesitan para trabajar, estén donde estén. Los perfiles de certificado sirven para proteger ese acceso.

## <a name="wi-fi-profileswi-fi-connections-in-microsoft-intunemd-and-supported-platforms"></a>[Perfiles de Wi-Fi](wi-fi-connections-in-microsoft-intune.md) y plataformas compatibles

Implementar la configuración de red inalámbrica para los usuarios. Estas opciones de configuración facilitan a los usuarios la conexión a la red corporativa.
#### <a name="supported-platforms"></a>Plataformas compatibles

|Windows 8.1 y posterior|Windows Phone 8.1 y versiones posteriores|iOS|Android|Samsung KNOX Standard|
|---------------------|---------------------------|---|-------|------------|
|Sí (puede importar un perfil de Wi-Fi de Windows).|Sí (puede configurar OMA-URI). |Sí|Sí|Sí|

## <a name="vpn-profilesvpn-connections-in-microsoft-intunemd-and-supported-platforms"></a>[Perfiles de VPN](vpn-connections-in-microsoft-intune.md) y plataformas compatibles
Implementar la configuración de red privada virtual (VPN) a los usuarios. Estas opciones de configuración facilitan a los usuarios la conexión a los recursos de la red corporativa.

|Windows 8.1 y posterior|Windows Phone 8.1 y versiones posteriores|iOS|Android|Samsung KNOX Standard|
|---------------------|---------------------------|---|-------|------------|
|Sí|Sí|Sí|Sí|Sí|

## <a name="email-profilesconfigure-access-to-corporate-email-using-email-profiles-with-microsoft-intunemd-and-supported-platforms"></a>[Perfiles de correo electrónico](configure-access-to-corporate-email-using-email-profiles-with-microsoft-intune.md) y plataformas compatibles
Cree, implemente y supervise la configuración de cliente de correo electrónico nativo en los dispositivos de su organización.

|Windows 8.1 y posterior|Windows Phone 8.1 y versiones posteriores|iOS|Android|Samsung KNOX Standard|
|---------------------|---------------------------|---|-------|------------|
|No|Sí|Sí|No|Sí|
> [!NOTE]
> [En esta entrada de blog del equipo de Intune](https://blogs.technet.microsoft.com/enterprisemobility/2015/02/19/using-oma-uri-to-create-custom-wi-fi-profiles-for-windows-phone-8-1/) encontrará información sobre cómo configurar un perfil de Wi-Fi de Windows Phone 8.1 mediante OMA-URI.

## <a name="certificate-profilessecure-resource-access-with-certificate-profilesmd-and-supported-platforms"></a>[Perfiles de certificado](secure-resource-access-with-certificate-profiles.md) y plataformas compatibles
Contribuya a proteger el acceso a los recursos de empresa tales como las redes inalámbricas y las conexiones VPN.

|Windows 8.1 y posterior|Windows Phone 8.1 y versiones posteriores|iOS|Android|Samsung KNOX Standard|
|---------------------|---------------------------|---|-------|------------|
|Sí|Sí|Sí|Sí|Sí|



<!--HONumber=Nov16_HO1-->

