---
title: "Configuración personalizada de perfil de Intune para Android for Work"
titleSuffix: Intune Azure preview
description: "Versión preliminar de Azure de Intune: aprenda a crear una configuración personalizada de perfil de Intune para dispositivos Android for Work."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 04/12/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 4724d6e5-05e5-496c-9af3-b74f083141f8
ms.reviewer: chrisbal
ms.suite: ems
ms.custom: intune-azure
ms.translationtype: Human Translation
ms.sourcegitcommit: 3758df744311392528be01c826527c2a9d879975
ms.openlocfilehash: 05afa9140e34b372cc49ace03a3ada965b907c17
ms.contentlocale: es-es
ms.lasthandoff: 05/10/2017


---

# <a name="create-intune-custom-profile-settings-for-android-for-work-devices"></a>Creación de configuración personalizada de perfil de Intune para dispositivos de Android for Work

Use la directiva de configuración personalizada de Android for Work de Intune para asignar las opciones de configuración de OMA-URI, que sirven para controlar características en dispositivos Android for Work. Se trata de una configuración estándar que muchos fabricantes de dispositivos móviles usan para controlar las características del dispositivo.

Esta funcionalidad está pensada para que se puedan asignar las opciones de configuración de Android que no se pueden definir con directivas de Intune. Intune admite un número limitado de directivas personalizadas de Android en este momento. Vea los ejemplos de este tema para averiguar qué directivas puede configurar.

## <a name="create-a-custom-profile"></a>Creación de un perfil personalizado

1. Siga las instrucciones que se indican en [Configuración personalizada de dispositivos](how-to-configure-custom-settings.md) para comenzar.
2. En la hoja **Configuración OMA-URI personalizada**, elija **Agregar** para agregar un nuevo valor.
3. En la hoja **Agregar fila**, configure lo siguiente:
    - **Name**: escriba un nombre único para la configuración personalizada de Android for Work que permita identificarla en el portal de Intune.
    - **Description**: proporcione una descripción que ofrezca una visión general de la directiva personalizada de Android y otra información relevante que le ayude a encontrarla.
    - **OMA-URI**: escriba la configuración OMA-URI para la que quiere suministrar un valor.
    - **Tipo de datos**: seleccione el tipo de datos en el que especificará este valor OMA-URI. Elija entre **Cadena**, **Cadena (archivo XML)**, **Fecha y hora**, **Entero**, **Punto flotante**, **Booleano** o **Base64 (archivo)**.
    - **Valor**: especifique el valor que desea asociar con el OMA-URI que especificó anteriormente. El método que usa para suministrar este valor variará según el tipo de datos que seleccionó. Por ejemplo, si eligió **Fecha y hora**, seleccionará el valor de un selector de fecha.
4. Cuando termine, elija Aceptar para volver a **Configuración OMA-URI personalizada** y, luego, agregue más configuraciones, o bien elija **Crear** para crear el perfil personalizado.


## <a name="example"></a>Ejemplo

En este ejemplo, creará un perfil personalizado que se puede usar para restringir si se permiten las acciones de copiar y pegar entre aplicaciones profesionales y aplicaciones personales en dispositivos administrados Android for Work.

1. Use el procedimiento que se indica en este tema para crear un perfil personalizado para dispositivos Android for Work con los valores siguientes:
    - **Name**: escriba "Bloqueo de la función de copiar y pegar" o un texto de su preferencia.
    - **Description**: escriba "Bloqueo de la función de copiar y pegar entre aplicaciones profesionales y personales" o un texto de su preferencia.
    - **OMA-URI**: escriba **./Vendor/MSFT/WorkProfile/DisallowCrossProfileCopyPaste**.
    - **Data type**: seleccione **Booleano** para indicar que el valor de este OMA-URI es **True** o **False**.
    - **Value**: seleccione **True**.
2. Debe terminar con una configuración similar a esta imagen.
![Bloqueo de la función de copiar y pegar para Android for Work.](./media/custom-policy-afw-copy-paste.png)
3. Ahora, cuando asigna este perfil personalizado a dispositivos Android for Work que administra, la función de copiar y pegar estará bloqueada entre las aplicaciones de los perfiles profesional y personal.
