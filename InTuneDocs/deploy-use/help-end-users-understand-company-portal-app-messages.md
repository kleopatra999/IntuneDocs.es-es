---
title: "Visualización de los mensajes de Portal de empresa en Android | Microsoft Docs"
description: "Describe los mensajes de la aplicación Portal de empresa que los usuarios finales de Intune pueden ver."
keywords: 
author: barlanmsft
ms.author: barlan
manager: angrobe
ms.date: 03/09/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 3df993aa-48c5-4799-b68d-c85fe4f7b02c
ms.reviewer: jeffgilb
ms.suite: ems
translationtype: Human Translation
ms.sourcegitcommit: 0936051b5c33a2e98f275ef7a3a32be2e8f5a8b0
ms.openlocfilehash: 3d5245e809263c2e5d76402ae9adc72baf7c7924
ms.lasthandoff: 03/10/2017


---

# <a name="help-end-users-understand-company-portal-app-messages"></a>Ayudar a que los usuarios finales comprendan los mensajes de la aplicación Portal de empresa

> [!NOTE]
> La siguiente información se aplica solo a dispositivos con Android 6.0 y versiones posteriores.

En distintos puntos del proceso de inscripción, los usuarios finales verán dos mensajes diferentes que podrían ser motivo de preocupación.

- __¿Permitir que el Portal de empresa realice y administre llamadas telefónicas?__
- __¿Permitir que Portal de empresa tenga acceso a fotos, elementos multimedia y archivos del dispositivo?__

## <a name="allow-company-portal-to-make-and-manage-phone-calls"></a>¿Permitir que Portal de empresa realice y administre llamadas telefónicas?

### <a name="where-it-appears"></a>Dónde aparece
El mensaje **¿Permitir que Portal de empresa realice y administre llamadas telefónicas?** aparece cuando los usuarios pulsan **Inscribir** en la aplicación Portal de empresa mientras inscriben su dispositivo.

### <a name="what-it-means"></a>Significado
Al aceptar este aviso, los usuarios permiten que se envíen los números de teléfono y de IMEI del dispositivo al servicio Intune. Aparecerán en la consola de administración en la página __Hardware__.

> [!NOTE]
> **La aplicación Portal de empresa nunca hace ni administra llamadas telefónicas.** Google controla el texto del mensaje y no se puede cambiar.

Para ver la página **Hardware**, vaya a **Grupos** > **Todos los dispositivos móviles** > **Dispositivos**. Seleccione el dispositivo del usuario y vaya a **Ver propiedades** > **Hardware**.

### <a name="what-happens-if-users-deny-access"></a>Qué sucede si los usuarios deniegan el acceso
Si los usuarios deniegan el acceso, pueden seguir usando la aplicación de Portal de empresa e inscribir su dispositivo. Sin embargo, el número de teléfono y el IMEI del dispositivo estarán en blanco en la página de __hardware__ de la consola de administración. La segunda vez que los usuarios inician sesión en la aplicación Portal de empresa después de denegar el acceso, el mensaje muestra una casilla **No volver a preguntar** que los usuarios pueden seleccionar para detener el aviso.

Si los usuarios permiten el acceso, pero luego lo deniegan, el mensaje aparece la próxima vez que los usuarios inicien sesión en la aplicación Portal de empresa después de la inscripción.

Si los usuarios más adelante deciden permitir el acceso, pueden ir a **Configuración** > **Aplicaciones** > **Portal de empresa** > **Permisos** > **Teléfono** y activarlo.

### <a name="how-to-explain-this-to-your-users"></a>Cómo explicar esto a los usuarios
Envíe a los usuarios a [Inscribir el dispositivo Android en Intune](/Intune/EndUser/enroll-your-device-in-intune-android) para más información.

## <a name="allow-company-portal-to-access-your-contacts"></a>Allow Company Portal to access your contacts? (¿Permitir que el portal de empresa tenga acceso a los contactos?)

### <a name="where-it-appears"></a>Dónde aparece
El mensaje **¿Permitir que el portal de empresa tenga acceso a los contactos?** aparece cuando los usuarios pulsan **Inscribir** en la aplicación Portal de empresa mientras inscriben el dispositivo.

### <a name="what-it-means"></a>Significado
Al aceptar este aviso, los usuarios permiten a Intune crear su cuenta de trabajo y administrar la identidad de Azure Active Directory registrada para el usuario en ese dispositivo.

> [!NOTE]
> **Microsoft nunca accede a los contactos.** Google controla el texto del mensaje y no se puede cambiar.

### <a name="what-happens-if-users-deny-access"></a>Qué sucede si los usuarios deniegan el acceso
Si los usuarios deniegan el acceso, el dispositivo no se inscribirán en Intune ni se podrá administrar. La segunda vez que los usuarios inician sesión en la aplicación Portal de empresa después de denegar el acceso, el mensaje muestra una casilla **No volver a preguntar** que los usuarios pueden seleccionar para detener el aviso.

Si los usuarios permiten el acceso, pero luego lo deniegan, el mensaje aparece la próxima vez que los usuarios inicien sesión en la aplicación Portal de empresa después de la inscripción.

Si los usuarios más adelante deciden permitir el acceso, pueden ir a **Configuración** > **Aplicaciones** > **Portal de empresa** > **Permisos** > **Teléfono** y activarlo.

### <a name="how-to-explain-this-to-your-users"></a>Cómo explicar esto a los usuarios
Envíe a los usuarios a [Inscribir el dispositivo Android en Intune](/Intune/EndUser/enroll-your-device-in-intune-android) para más información.

## <a name="allow-company-portal-to-access-photos-media-and-files-on-your-device"></a>¿Permitir que Portal de empresa tenga acceso a fotos, elementos multimedia y archivos del dispositivo?

### <a name="where-it-appears"></a>Dónde aparece
El mensaje **¿Permitir que Portal de empresa tenga acceso a fotos, elementos multimedia y archivos del dispositivo?** aparece cuando los usuarios pulsan **Enviar datos** para enviar registros a su administrador de TI.

### <a name="what-it-means"></a>Significado
Al aceptar este aviso, los usuarios permiten que su dispositivo escriba datos de registros en la tarjeta SD del dispositivo y para permitir que esos registros se muevan mediante un cable USB.   

> [!NOTE]
> **La aplicación Portal de empresa nunca tiene acceso a las fotos, elementos multimedia ni archivos de los usuarios.** Google controla el texto del mensaje y no se puede cambiar.

### <a name="what-happens-if-users-deny-access"></a>Qué sucede si los usuarios deniegan el acceso
Si los usuarios deniegan el acceso, podrán enviar registros de datos por correo electrónico, pero los registros no se copiarán en la tarjeta SD del dispositivo.

La segunda vez que los usuarios inician sesión en la aplicación Portal de empresa después de denegar el acceso, el mensaje muestra una casilla **No volver a preguntar** que los usuarios pueden seleccionar para que el mensaje no se vuelva a mostrar. Si los usuarios permiten el acceso, pero luego lo deniegan, el mensaje aparece la próxima vez que los usuarios intenten enviar registros. Si los usuarios más adelante deciden permitir el acceso, pueden ir a **Configuración** > **Aplicaciones** > **Portal de empresa** > **Permisos** > **Almacenamiento** y activar el permiso.


### <a name="how-to-explain-this-to-your-users"></a>Cómo explicar esto a los usuarios
Envíe a sus usuarios a [Enviar registros al administrador de TI mediante correo electrónico](/Intune/EndUser/send-logs-to-your-it-admin-by-email-android). También puede enviarle a [Enviar registros al administrador de TI por cable](/Intune/EndUser/send-logs-to-your-it-admin-by-cable-android) si desea poder comparar los dos métodos.


### <a name="see-also"></a>Consulte también
[Qué decirles a los usuarios finales sobre el uso de Intune](/intune/deploy-use/what-to-tell-your-end-users-about-using-microsoft-intune)

