---
title: Directivas de cumplimiento de dispositivos | Microsoft Docs
description: "En este tema se explican qué son las directivas de cumplimiento del dispositivo y cómo funcionan."
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 11/14/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 0775107a-6662-41c8-9404-be14bbb599f3
ms.reviewer: chrisgre
ms.suite: ems
ms.custom: intune-classic
translationtype: Human Translation
ms.sourcegitcommit: ab6d9b6b296fb4e1fb0aaa9496fede28976728dc
ms.openlocfilehash: 2de9a7d639ee667ee195ded2875a8ac8e478fffb
ms.lasthandoff: 04/14/2017


---

# <a name="device-compliance-policies-in-microsoft-intune"></a>Directivas de cumplimiento de dispositivos en Microsoft Intune

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

## <a name="what-is-a-compliance-policy"></a>¿Qué es una directiva de cumplimiento?
Para ayudar a proteger los datos de empresa, debe asegurarse de que los dispositivos usados para acceder a datos y aplicaciones de empresa cumplan ciertas reglas. Estas reglas pueden incluir el uso de un PIN para acceder a los dispositivos y el cifrado de los datos almacenados en ellos. A un conjunto de estas reglas se le denomina directiva de cumplimiento.

## <a name="how-should-i-use-compliance-policies"></a>¿Cómo se deben usar las directivas de cumplimiento?
Las directivas de cumplimiento se pueden usar con directivas de acceso condicional para permitir el acceso al correo electrónico y otros servicios solo a los dispositivos que cumplen con las reglas de directivas de cumplimiento. Para aprender cómo se pueden usar las dos directivas juntas, lea el artículo [Restringir el acceso al correo electrónico y los servicios de O365](restrict-access-to-email-and-o365-services-with-microsoft-intune.md).

También puede usar las directivas de cumplimiento con independencia del acceso condicional. Cuando se usan directivas de cumplimiento de forma independiente, los dispositivos de destino se evalúan y su estado se cumplimiento se notifica. Por ejemplo, si quiere informar sobre el número de dispositivos que no están cifrados o sobre qué dispositivos están liberados o modificados. Pero cuando se usan directivas de cumplimiento de manera independiente, no existen restricciones de acceso a los recursos de empresa.

Usted se encarga de implementar las directivas de cumplimiento para los usuarios. Cuando se implementa una directiva de cumplimiento para un usuario, se comprueba el cumplimiento de todos los dispositivos del usuario.
Para más información sobre cuánto tiempo tardan los dispositivos móviles en obtener una directiva una vez que esta se ha implementado, consulte [Administrar la configuración y las características de los dispositivos](https://docs.microsoft.com/intune/deploy-use/manage-settings-and-features-on-your-devices-with-microsoft-intune-policies#frequently-asked-questions-about-intune-policies).

En la tabla siguiente se enumera los tipos de dispositivos que admiten directivas de cumplimiento. También se describe cómo administrar la configuración no compatible cuando se usa una directiva de cumplimiento con una directiva de acceso condicional.

-----------------------------

|Configuración de directiva| Windows 8.1 y posterior| Windows Phone 8.1 y versiones posteriores| iOS 8.0 y versiones posteriores|Android 4.0 y versiones posteriores<br/>Samsung KNOX Standard 4.0 y posterior|
|-----|----|----|----|----|
|**Configuración de PIN o contraseña** |Corregido|Corregido|Corregido|En cuarentena|
|**Cifrado del dispositivo**|No aplicable|Corregido|Corregido (estableciendo PIN)|En cuarentena|
|**Dispositivo liberado o modificado**|No aplicable|No aplicable|En cuarentena (no es una configuración)|En cuarentena (no es una configuración)|
|**Perfil de correo electrónico**|No aplicable|No aplicable|En cuarentena|No aplicable|
|**Versión de SO mínima**|En cuarentena|En cuarentena|En cuarentena|En cuarentena|
|**Versión de SO máxima**|En cuarentena|En cuarentena|En cuarentena|En cuarentena|
|**Atestación de estado de Windows**|Windows 10 y Windows 10 Mobile están en cuarentena<br /><br />No aplicable: Windows 8.1|No aplicable|No aplicable|No aplicable|

------------------------------

**Corregido** = el sistema operativo del dispositivo exige compatibilidad. (Por ejemplo, se obliga al usuario a configurar un PIN).

**En cuarentena** = el sistema operativo del sistema no exige compatibilidad. (Por ejemplo, los dispositivos Android no obligan al usuario a cifrar el dispositivo). Si los dispositivos no son compatibles, se emprenden las acciones siguientes:

-   El dispositivo se bloquea si se aplica una directiva de acceso condicional al usuario.

-   El portal de empresa notifica al usuario acerca de los problemas de cumplimiento.

## <a name="next-steps"></a>Pasos siguientes
[Crear una directiva de cumplimiento de dispositivos](create-a-device-compliance-policy-in-microsoft-intune.md)

[Implementar y supervisar una directiva de cumplimiento de dispositivos](deploy-and-monitor-a-device-compliance-policy-in-microsoft-intune.md)

### <a name="see-also"></a>Consulte también
[Restringir el acceso al correo electrónico y los servicios de O365](restrict-access-to-email-and-o365-services-with-microsoft-intune.md)

