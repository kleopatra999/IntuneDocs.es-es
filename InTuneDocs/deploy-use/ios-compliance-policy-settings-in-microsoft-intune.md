---
title: "Configuración de directivas de cumplimiento para dispositivos iOS | Microsoft Docs"
description: "En este tema se describen las reglas y la configuración que puede establecer en una directiva de cumplimiento para dispositivos iOS."
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 12/15/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 4a59d24f-ed58-49b1-b874-b2d4aea3ec76
ms.reviewer: chrisgre
ms.suite: ems
ms.custom: intune-classic
translationtype: Human Translation
ms.sourcegitcommit: 9f05e516723976dcf6862475dbb78f9dce2913be
ms.openlocfilehash: f4867d18634add8cb6ffc61a4413618b1bea5a4b


---


# <a name="compliance-policy-settings-for-ios-devices-in-microsoft-intune"></a>Configuración de directivas de cumplimiento para dispositivos iOS en Microsoft Intune

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

La configuración de directivas que se describe en este tema se aplica a los dispositivos con iOS 8.0 y versiones posteriores.

Si quiere información sobre otras plataformas, seleccione uno de los siguientes temas:
> [!div class="op_single_selector"]
- [Opciones de configuración de directivas de cumplimiento para dispositivos Android](android-compliance-policy-settings-in-microsoft-intune.md)
- [Configuración de directivas de cumplimiento para Android for Work](afw-compliance-policy-settings-in-microsoft-intune.md)
- [Configuración de directivas de cumplimiento para dispositivos Windows](windows-compliance-policy-settings-in-microsoft-intune.md)

## <a name="system-security-settings"></a>Configuración de seguridad del sistema
### <a name="password"></a>Contraseña
- **Requerir una contraseña para desbloquear dispositivos móviles:** establezca esta opción en **Sí** para exigir que los usuarios escriban una contraseña antes de poder tener acceso a sus dispositivos. Los dispositivos iOS que usan una contraseña están cifrados.

- **Permitir contraseñas sencillas**: establezca esta opción en **Sí** para permitir al usuario crear una contraseña sencilla como **1234** o **1111**.

-  **Longitud mínima de la contraseña**: especifique el número mínimo de dígitos o caracteres que debe tener la contraseña del usuario.

- **Tipo de contraseña obligatoria:** especifique si el usuario debe crear una contraseña **Alfanumérica** o **Numérica**.

- **Número mínimo de conjuntos de caracteres:** si establece la opción **Tipo de contraseña requerida** en **Alfanumérica**, use esta configuración para especificar el número mínimo de conjuntos de caracteres que debe contener la contraseña. Los conjuntos de cuatro caracteres son los siguientes:
  -   Letras minúsculas
  -   Letras mayúsculas
  -   Símbolos
  -   Números

  Para establecer un número mayor será necesario que el usuario cree una contraseña más compleja.

  En el caso de dispositivos iOS, este valor de configuración se refiere al número de caracteres especiales (por ejemplo, **!**, **#**, **&amp;**) que deben incluirse en la contraseña.

- **Minutos de inactividad antes de que sea necesaria la contraseña**: especifique el tiempo de inactividad que transcurre antes de que el usuario deba volver a escribir su contraseña.

- **Caducidad de contraseña (días)**: seleccione el número de días que faltan para que la contraseña caduque y durante los cuales deben crear una nueva.

- **Recordar historial de contraseñas:** use esta opción junto con **Impedir la reutilización de contraseñas anteriores** para impedir que el usuario cree contraseñas que se han usado anteriormente.

- **Impedir la reutilización de contraseñas anteriores**: si ha seleccionado **Recordar historial de contraseñas**, especifique el número de contraseñas que se han usado previamente que no se pueden volver a usar.

- **Requerir una contraseña cuando el dispositivo vuelva de un estado de inactividad**: use este valor junto con el de la opción **Minutos de inactividad antes de que sea necesaria la contraseña**. Se pedirá al usuario que escriba una contraseña para obtener acceso a un dispositivo que haya estado inactivo durante el tiempo especificado en la opción **Minutos de inactividad antes de que sea necesaria la contraseña**.

### <a name="email-profile"></a>Perfil de correo electrónico
- **Intune debe administrar la cuenta de correo electrónico:** cuando esta opción se establece en **Sí**, el dispositivo debe utilizar el perfil de correo electrónico que tenga implementado. El dispositivo se considera no conforme en las situaciones siguientes:
  - El perfil de correo electrónico se implementa en un grupo de usuarios distinto del grupo de usuarios al que se dirige la directiva de cumplimiento.
  - El usuario ya tiene configurada una cuenta de correo electrónico en el dispositivo que coincide con el perfil de correo electrónico de Intune implementado en dicho dispositivo. Intune no puede sobrescribir el perfil implementado por el usuario y, por tanto, no puede administrarlo. Para garantizar el cumplimiento, el usuario debe quitar la configuración de correo electrónico existente. De este modo, Intune puede instalar el perfil de correo electrónico administrado.

- **Seleccione el perfil de correo electrónico que Intune debe administrar**: si se selecciona la opción **Intune debe administrar la cuenta de correo electrónico**, elija **Seleccionar** para especificar el perfil de correo electrónico de Intune. El perfil de correo electrónico debe estar presente en el dispositivo.

     Para más información sobre los perfiles de correo electrónico, consulte [Configurar el acceso al correo electrónico corporativo mediante perfiles de correo electrónico con Microsoft Intune](configure-access-to-corporate-email-using-email-profiles-with-microsoft-intune.md).

## <a name="device-health-settings"></a>Configuración de estado del dispositivo

- **El dispositivo no debe estar modificado por los métodos de acceso jailbreak o root:** si habilita esta opción, los dispositivos descodificados no serán compatibles.

##  <a name="device-properties"></a>Propiedades del dispositivo
- **SO mínimo requerido:** cuando un dispositivo no cumpla el requisito de versión de SO mínima, se notificará como no compatible.
Se mostrará un vínculo con información sobre cómo actualizar el sistema. El usuario puede elegir actualizar su dispositivo. Después de eso, puede acceder a los recursos de la empresa.

- **Versión de SO máxima permitida**: cuando un dispositivo usa una versión de SO posterior a la especificada en la regla, se bloquea el acceso a los recursos de la empresa y se solicita al usuario que se ponga en contacto con el administrador de TI. Mientras no se cambie la regla para permitir la versión de SO, este dispositivo no podrá usarse para acceder a los recursos de la empresa.



<!--HONumber=Jan17_HO4-->


