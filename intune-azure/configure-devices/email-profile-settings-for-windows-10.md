---
title: "Configuración del correo electrónico de Intune para dispositivos Windows 10"
titleSuffix: Intune Azure preview
description: "Versión preliminar de Intune Azure: aprenda sobre la configuración de Intune que puede usar para configurar conexiones de correo electrónico en dispositivos Windows 10."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 02/15/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 2ffafbd0-4b5d-4c86-a46b-611f9b7a58e5
ms.reviewer: heenamac
ms.suite: ems
ms.custom: intune-azure
translationtype: Human Translation
ms.sourcegitcommit: 153cce3809e24303b8f88a833e2fc7bdd9428a4a
ms.openlocfilehash: 9a052f26d87fbfdc5794cf97033b409846db6a73
ms.lasthandoff: 02/18/2017


---

# <a name="email-profile-settings-for-windows-10-devices-in-microsoft-intune"></a>Configuración del perfil de correo electrónico para dispositivos Windows 10 en Microsoft Intune

[!INCLUDE[azure_preview](../includes/azure_preview.md)]



- **Servidor de correo electrónico**: el nombre de host del servidor de Exchange.
- **Nombre de la cuenta**: el nombre para mostrar de la cuenta de correo electrónico tal y como aparecerá para los usuarios en sus dispositivos.
- **Atributo de nombre de usuario de AAD**: es el atributo de Active Directory (AD) o Azure AD que se usará para generar el nombre de usuario de este perfil de correo electrónico. Seleccione la **dirección SMTP principal**, como **user1@contoso.com**, o el **nombre principal de usuario**, como **usuario1** o **user1@contoso.com**.
- **Atributo de dirección de correo electrónico de AAD**: cómo se genera la dirección de correo electrónico para el usuario en cada dispositivo. Seleccione **Dirección SMTP primaria** para usar la dirección SMTP primaria para iniciar sesión en Exchange o **Nombre principal de usuario** para usar el nombre principal completo como dirección de correo electrónico.


## <a name="security-settings"></a>Configuración de seguridad

- **SSL**: use la comunicación de Capa de sockets seguros (SSL) al enviar correos electrónicos, recibir correos electrónicos y comunicarse con el servidor Exchange.



## <a name="synchronization-settings"></a>Configuración de sincronización

- **Cantidad de correo electrónico para sincronizar**: elija el número de días de correo electrónico que quiere sincronizar, o seleccione **Unlimited** (Sin límite) para sincronizar todos el correo electrónico disponible.
- **Programación de sincronización**: seleccione la programación por la que los dispositivos sincronizarán datos de Exchange Server. También puede seleccionar **Cuando llegan los mensajes** (los datos se sincronizan tan pronto como llegan) o **Manual** (el usuario del dispositivo debe iniciar la sincronización).

## <a name="content-sync-settings"></a>Configuración de la sincronización de contenido

- **Tipo de contenido para sincronizar**: seleccione los tipos de contenido que quiere sincronizar con los dispositivos:
    - **Contactos**
    - **Calendarioio**
    - **Tareas**

