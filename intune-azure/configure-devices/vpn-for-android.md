---
title: "Configuración de VPN de Intune para dispositivos Android"
titleSuffix: Intune Azure preview
description: "Versión preliminar de Intune Azure: aprenda sobre la configuración de Intune que puede usar para configurar conexiones VPN en dispositivos Android."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 02/15/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 16c056ca-320e-4107-ad03-a0cf96c28885
ms.reviewer: karanda
ms.suite: ems
ms.custom: intune-azure
translationtype: Human Translation
ms.sourcegitcommit: 153cce3809e24303b8f88a833e2fc7bdd9428a4a
ms.openlocfilehash: 5ecbeb43e05887dc4cadbe110e3f97bd15363073
ms.lasthandoff: 02/18/2017


---

# <a name="vpn-settings-for-android-devices-in-microsoft-intune"></a>Configuración de VPN para dispositivos Android en Microsoft Intune

[!INCLUDE[azure_preview](../includes/azure_preview.md)]

Según la configuración que elija, no todos los valores de la siguiente lista se pueden configurar.

**Connection name** (Nombre de la conexión): escriba un nombre para esta conexión. Los usuarios finales verán este nombre cuando exploren su dispositivo para ver la lista de conexiones VPN disponibles.
- **Dirección IP o FQDN**: proporcione la dirección IP o el nombre de dominio completo del servidor VPN al que se conectarán los dispositivos. Ejemplos: **192.168.1.1**, **vpn.contoso.com**.
- **Método de autenticación**: elija cómo se autenticarán los dispositivos en el servidor VPN. Las opciones son:
    - **Certificados**: seleccione un perfil de certificado SCEP o PKCS que haya creado anteriormente para autenticar la conexión. Para más información sobre los perfiles de certificado, consulte [Configuración de certificados](how-to-configure-certificates.md).
    - **Nombre de usuario y la contraseña**: los usuarios finales deben proporcionar un nombre de usuario y una contraseña para iniciar sesión en el servidor VPN.
- **Tipo de conexión**: seleccione el tipo de conexión VPN de la siguiente lista de proveedores:
    - **Check Point Capsule VPN**
    - **Cisco AnyConnect**
    - **Dell SonicWALL Mobile Connect**
    - **F5 Edge Client**
    - **Pulse Secure**
    - **Citrix**

- **Huella digital** (solo Check Point Capsule VPN): especifique una cadena (por ejemplo "Código de huella digital de Contoso") que se usará para comprobar que se puede confiar en el servidor VPN. Una huella digital se puede enviar al cliente para que sepa que puede confiar en cualquier servidor que presente esa misma huella digital al conectarse. Si el dispositivo todavía no tiene la huella digital, pedirá al usuario que confíe en el servidor VPN al que se está conectando mientras muestra la huella digital (el usuario comprueba la huella digital manualmente y selecciona Confiar para conectarse).
- **Especifique pares clave-valor para los atributos de la VPN de Citrix** (solo Citrix): escriba los pares de clave y valor, que ha suministrado Citrix, para configurar las propiedades de la conexión VPN.

