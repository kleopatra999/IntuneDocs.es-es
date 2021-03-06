---
title: Borrado solo de datos corporativos de aplicaciones
titleSuffix: Intune Azure preview
description: "Versión preliminar de Intune Azure: aprenda cómo borrar aplicaciones de forma selectiva con Microsoft Intune."
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 02/07/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 42605e6e-5b84-44ff-b86e-346ea123b53e
ms.reviewer: mghadial
ms.suite: ems
ms.custom: intune-azure
translationtype: Human Translation
ms.sourcegitcommit: 153cce3809e24303b8f88a833e2fc7bdd9428a4a
ms.openlocfilehash: 0d5385583265800ccfbb7d57e3dd325d6c8283e7
ms.lasthandoff: 02/18/2017

---

# <a name="how-to-wipe-only-corporate-data-from-intune-managed-apps"></a>Borrado solo de datos corporativos de aplicaciones administradas por Intune

[!INCLUDE[azure_preview](../includes/azure_preview.md)]

Cuando un dispositivo se pierde o lo roban, o cuando un empleado deja la empresa, le interesa asegurarse de que se eliminan del dispositivo los datos de la aplicación de empresa. Pero es posible que no quiera quitar del dispositivo los datos personales, sobre todo si se trata de un dispositivo propiedad de un empleado.

Para quitar de forma selectiva datos de la aplicación de empresa, siga los pasos de este tema para crear una solicitud de borrado. Una vez finalizada la solicitud, la próxima vez que la aplicación se ejecute en el dispositivo, los datos de la empresa se quitarán de la aplicación.

>[!IMPORTANT]
> Se quitan los contactos sincronizados directamente desde la aplicación en la libreta de direcciones nativa. No se pueden borrar los contactos sincronizados desde la libreta de direcciones nativa en otro origen externo. Actualmente, esto solo se aplica a la aplicación Microsoft Outlook.

## <a name="create-a-wipe-request"></a>Crear una solicitud de borrado

1.  Inicie sesión en el [Portal de Azure](https://portal.azure.com).

2.  Elija **More Services** (Más servicios), escriba **Intune** en el cuadro de texto de filtro y seleccione **Intune**. Se abre la hoja de la versión preliminar de Intune: elija la hoja **Administrar aplicaciones**.

    ![Captura de pantalla de la hoja Nueva solicitud de borrado](../media/intune-azure-preview-blade.png)

3.  En la hoja **Mobile Apps**, elija **Nueva solicitud de borrado**. Se abre la hoja **Nueva solicitud de borrado**.

4.  Elija **Nueva solicitud de borrado**. Se abre la hoja **Nueva solicitud de borrado**.

    ![Captura de pantalla de la hoja Nueva solicitud de borrado](../media/AzurePortal_MAM_NewWipeRequest.png)

5.  Elija **Usuario** para abrir la hoja **Usuario** y seleccione el usuario cuyos datos de aplicación quiera borrar.

6.  Elija **Dispositivo**. Se abre la hoja **Dispositivo** que muestra todos los dispositivos asociados al usuario seleccionado. También proporciona dos columnas: el nombre del dispositivo, que es un nombre descriptivo definido por el usuario, y el tipo de dispositivo, la plataforma del dispositivo. Seleccione el dispositivo que desea borrar.

7.  Ahora está de nuevo en la hoja **Nueva solicitud de borrado**. Seleccione **Aceptar** para realizar una solicitud de borrado. 

El servicio crea y realiza el seguimiento de una solicitud de borrado independiente para cada aplicación protegida en el dispositivo, y del usuario asociado a la solicitud de borrado.

## <a name="monitor-your-wipe-requests"></a>Supervisar las solicitudes de borrado de datos

Puede tener un informe resumido que muestre el estado general de la solicitud de borrado y que incluya el número de solicitudes pendientes y errores. Para obtener más información, siga estos pasos:

1.  En la hoja **Mobile Apps - Borrado selectivo de aplicaciones**, puede ver la lista de sus solicitudes agrupadas por usuarios. Debido a que el sistema crea una solicitud de borrado para cada aplicación protegida que se ejecuta en el dispositivo, puede que vea varias solicitudes para un mismo usuario. Este estado indica si una solicitud de borrado está **pendiente**, ha provocado un **error** o si es **correcta**.

    ![Captura de pantalla de la hoja Nueva solicitud de borrado](../media/wipe-request-status-1.png)

Además, podrá ver el nombre del dispositivo, y su tipo, lo que puede ser útil cuando se lean los informes.

>[!IMPORTANT]
> El usuario debe abrir la aplicación de la que se vaya a realizar el borrado, que puede tardar hasta 30 minutos después de efectuar la solicitud.

## <a name="delete-a-wipe-request"></a>Eliminación de una solicitud de borrado

Los borrados con estado pendiente se muestran hasta que se eliminen manualmente.  Para eliminar manualmente una solicitud de borrado:

1.  En la hoja **Solicitud de borrado**, elija el icono **Solicitud de borrado** para abrir la hoja **Solicitud de borrado**.

2.  Haga clic con el botón derecho en la solicitud de borrado que quiere eliminar y elija **Delete wipe request** (Eliminar solicitud de borrado).

    ![Captura de pantalla de la hoja Nueva solicitud de borrado](../media/delete-wipe-request.png)

3.  Se le pedirá que confirme la eliminación. Elija **Sí** o **No** y luego haga clic en **Aceptar**.

### <a name="see-also"></a>Consulte también
[What's app protection policy](what-is-app-protection-policy.md) (¿Qué es la directiva de protección de aplicaciones?)

[¿Qué es la administración de aplicaciones?](what-is-app-management.md)
