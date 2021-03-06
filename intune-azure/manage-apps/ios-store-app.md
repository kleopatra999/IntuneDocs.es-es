---
title: "Adición de aplicaciones de la tienda iOS a Intune | Microsoft Docs"
titleSuffix: Intune Azure preview
description: "Versión preliminar de Intune Azure: aprenda sobre cómo agregar aplicaciones iOS de la tienda a Intune."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: c59514d7-1256-4576-9380-e7a0b85a0378
ms.reviewer: mghadial
ms.suite: ems
ms.custom: intune-azure
ms.translationtype: Human Translation
ms.sourcegitcommit: 3758df744311392528be01c826527c2a9d879975
ms.openlocfilehash: 011f33d1d8569a079f73baaca6ba2a665131691d
ms.contentlocale: es-es
ms.lasthandoff: 05/10/2017

---

# <a name="how-to-add-ios-store-apps-to-microsoft-intune"></a>Adición de aplicaciones de la tienda iOS a Microsoft Intune

[!INCLUDE[azure_preview](../includes/azure_preview.md)]

## <a name="before-you-start"></a>Antes de empezar

Solo se pueden asignar aplicaciones mediante este método si son gratuitas en la tienda de aplicaciones. Si desea asignar aplicaciones de pago mediante Intune, considere usar el [programa de compra por volumen de iOS](ios-vpp-apps.md).


## <a name="step-1---search-for-the-app-in-the-store"></a>Paso 1: Búsqueda de la aplicación en la tienda

1. Inicie sesión en el portal de Azure.
2. Elija **More Services** >  (Más servicios) **Supervisión y administración** > **Intune**.
3. En la hoja **Intune**, elija **Administrar aplicaciones**.
4. En la carga de trabajo **Mobile Apps**, elija Administrar > **Aplicaciones**.
5. Encima de la lista de aplicaciones, elija **Agregar**.
6. En la hoja **Agregar aplicación**, elija **Buscar en App Store**.
7. En la hoja **App Store de Apple**, escriba el nombre (o parte de él) en el cuadro de búsqueda. Intune busca en la tienda y devuelve una lista de resultados pertinentes.
8. En la lista, elija la aplicación que desee y haga clic en **Aceptar**.

## <a name="step-2---configure-app-information"></a>Paso 2: Configuración de la información de la aplicación

1. En la hoja **Agregar aplicación**, elija **Información de la aplicación**.
2. En la hoja **Editar aplicación**, configure la siguiente información. Cuando haya terminado, haga clic en **Aceptar**. Dependiendo de la aplicación que haya elegido, algunos de los valores de esta hoja pueden haber sido rellenados automáticamente:
- **Nombre de la aplicación**: escriba el nombre de la aplicación tal como se mostrará en el Portal de empresa. Asegúrese de que todos los nombres de aplicación que usa son únicos. Si el mismo nombre de aplicación existe dos veces, solo se mostrará a los usuarios una de las aplicaciones en el portal de empresa.
    - **Descripción de la aplicación**: escriba una descripción de la aplicación. Se mostrará a los usuarios en el portal de empresa.
- **Editor:** escriba el nombre del editor de la aplicación.
- **URL de la tienda de aplicaciones**: escriba la dirección URL de la tienda de aplicaciones de la aplicación que quiere crear.
- **Sistema operativo mínimo**: en la lista, elija la versión mínima del sistema operativo en la que se puede instalar la aplicación. Si la aplicación se asigna a un dispositivo con un sistema operativo anterior, no se instalará.
- **Categoría** (opcional). Seleccione una o más de las categorías de aplicaciones integradas, o una categoría que haya creado. Así les resultará más fácil a los usuarios encontrar la aplicación cuando exploren el portal de empresa.
- **Mostrar como aplicación destacada en el Portal de empresa**: la aplicación se muestra de forma destacada en la página principal del Portal de empresa cuando los usuarios buscan aplicaciones.
- **Dirección URL de información**: opcionalmente, escriba la dirección URL de un sitio web que contenga información sobre esta aplicación. La dirección URL se mostrará a los usuarios en el portal de empresa.
- **Dirección URL de privacidad**: opcionalmente, escriba la dirección URL de un sitio web que contenga información de privacidad sobre esta aplicación. La dirección URL se mostrará a los usuarios en el portal de empresa.
- **Desarrollador**: opcionalmente, escriba el nombre del desarrollador de la aplicación.
- **Propietario**: opcionalmente,, escriba un nombre para el propietario de esta aplicación, por ejemplo, **departamento de Recursos Humanos**.
- **Notas**: escriba notas que le gustaría asociar a esta aplicación.
- **Cargar icono**: carga un icono que se asociará a la aplicación. Será el icono que se muestre con la aplicación cuando los usuarios examinen el portal de empresa.
3. Cuando haya terminado, en la hoja **Agregar aplicación**, elija **Guardar**.

La aplicación que ha creado se muestra en la lista de aplicaciones donde puede asignarla a los grupos que elija. Para obtener ayuda, consulte [Asignación de aplicaciones a grupos](deploy-apps.md).

