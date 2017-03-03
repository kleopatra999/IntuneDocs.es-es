---
title: "Adición de aplicaciones web a Intune"
titleSuffix: Intune Azure preview
description: "Versión preliminar de Azure de Intune: aprenda a agregar aplicaciones web a Intune."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 02/15/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 5f08752f-0e87-4ad9-a34c-4991b3150775
ms.reviewer: mghadial
ms.suite: ems
ms.custom: intune-azure
translationtype: Human Translation
ms.sourcegitcommit: 153cce3809e24303b8f88a833e2fc7bdd9428a4a
ms.openlocfilehash: c2e54d3e57a4b02ba277b88cc672d5587c449281

---

# <a name="how-to-add-web-apps-to-microsoft-intune"></a>Agregar aplicaciones web a Microsoft Intune

[!INCLUDE[azure_preview](../includes/azure_preview.md)]

1. Inicie sesión en el portal de Azure.
2. Elija **Más servicios** > **Supervisión y administración** > **Intune**.
3. En la hoja **Intune**, elija **Administrar aplicaciones**.
4. En la carga de trabajo **Mobile Apps**, elija **Administrar** > **Aplicaciones**.
5. Encima de la lista de aplicaciones, elija **Agregar**.
6. En la hoja **Agregar aplicación**, elija **Información de la aplicación**.
7. En la hoja **Editar aplicación**, configure la siguiente información. Cuando haya terminado, haga clic en **Agregar**:
    - **Dirección URL de la aplicación**: escriba la dirección URL del sitio web que hospeda la aplicación que quiere implementar.
    - **Nombre de la aplicación**: escriba el nombre de la aplicación tal como se mostrará en el Portal de empresa.
    - **Descripción de la aplicación**: escriba una descripción de la aplicación. Esta se mostrará a los usuarios en el Portal de empresa.
    - **Publicador**: escriba el nombre del publicador de esta aplicación.
    - **Categoría (opcional)**: seleccione una o varias de las categorías de aplicaciones integradas o una categoría que haya creado. Así les resultará más fácil a los usuarios encontrar la aplicación cuando exploren el portal de empresa.
    - **Mostrar como aplicación destacada en el Portal de empresa**: la aplicación se muestra de forma destacada en la página principal del Portal de empresa cuando los usuarios buscan aplicaciones.
    - **Se necesita Managed Browser para abrir este vínculo**: al implementar un vínculo a un sitio web o aplicación web para los usuarios, estos solo podrán abrirlo en el explorador administrado de Intune. Este explorador debe instalarse en su dispositivo.
    - **Cargar icono**: carga un icono que se asociará a la aplicación. Será el icono que se muestre con la aplicación cuando los usuarios examinen el portal de empresa.
8. Cuando haya terminado, en la hoja **Agregar aplicación**, elija **Guardar**.

La aplicación que ha creado se muestra en la lista de aplicaciones donde puede asignarla a los grupos que elija. Para obtener ayuda, consulte [Asignación de aplicaciones a grupos](/intune-azure/manage-apps/deploy-apps).


<!--HONumber=Feb17_HO3-->

