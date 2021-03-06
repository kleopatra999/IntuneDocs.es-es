---
title: "Protección de los datos de la aplicación mediante directivas de MAM | Microsoft Docs"
description: "En este tema se explica cómo pueden ayudar las directivas de administración de aplicaciones móviles a proteger los datos de su empresa, evitar la pérdida de datos y separar la información personal y profesional."
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 11/14/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: ab6cd622-b738-4a63-9c91-56044aaafa6d
ms.reviewer: joglocke
ms.suite: ems
ms.custom: intune-classic
ms.translationtype: Human Translation
ms.sourcegitcommit: 33febef8787887401960592d95356347f6917681
ms.openlocfilehash: 9959e9f757e83c7aa4274b7e7b9df949fff022cc
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---

# <a name="protect-app-data-using-app-protection-policies-with-microsoft-intune"></a>Proteger datos de aplicaciones mediante directivas de protección de aplicaciones con Microsoft Intune

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

## <a name="how-you-can-protect-app-data"></a>Cómo puede proteger los datos de la aplicación
Los empleados usan dispositivos móviles para tareas personales y de trabajo. Mientras se asegura de que los empleados pueden ser productivos, también puede evitar la pérdida de datos, ya sea intencional o involuntaria.  Además, desea tener la capacidad de proteger datos de la compañía a los que los empleados obtienen acceso mediante el uso de dispositivos que no administra.

Puede usar las directivas de protección de aplicaciones de Intune para ayudar a proteger los datos de su empresa. Dado que las directivas de protección de aplicaciones de Intune se pueden usar **independientemente de cualquier solución de administración de dispositivos móviles (MDM)**, puede usar MAM para proteger los datos de la empresa con o sin la inscripción de los dispositivos en una solución de administración de dispositivos. Mediante la implementación de **directivas de nivel de aplicación**, puede restringir el acceso a los recursos de la empresa y mantener los datos dentro del ámbito del departamento de TI.

Se pueden configurar directivas de protección de aplicaciones para aplicaciones que se ejecutan en dispositivos que estén:

-   **Inscritos en Microsoft Intune:** los dispositivos de esta categoría son normalmente dispositivos corporativos.

-   **Inscritos en una solución MDM de terceros:** los dispositivos de esta categoría son normalmente dispositivos corporativos.

      > [!NOTE]
      > No se recomienda utilizar directivas de protección de aplicaciones con soluciones de contenedor seguras o administración de aplicaciones móviles de terceros.

-   **No inscritos en ninguna solución MDM:** los dispositivos de esta categoría normalmente son dispositivos de empleados no administrados ni inscritos en Intune ni en ninguna otra solución MDM.

> [!IMPORTANT]
> Puede crear directivas de protección de aplicaciones para aplicaciones móviles de Office que se conectan a servicios de Office 365. Las directivas de protección de aplicaciones no son compatibles con las aplicaciones que se conectan a los servicios locales de Exchange, SharePoint o Skype Empresarial.

## <a name="benefits-of-using-app-protection-policies"></a>Ventajas del uso de directivas de protección de aplicaciones

-   **Ayudan a proteger los datos de su compañía a nivel de aplicación.** Puesto que la administración de aplicaciones móviles no requiere la administración de dispositivos, puede proteger los datos de la empresa en dispositivos administrados y no administrados. La administración se centra en la identidad del usuario, lo que elimina la necesidad de administrar dispositivos.

-   **La productividad del usuario no se ve afectada y no se aplican las directivas cuando se usa la aplicación en un contexto personal.** Las directivas se aplican solo en un contexto de trabajo, lo que le ofrece la capacidad de proteger los datos de la compañía sin tocar los datos personales.

Hay otras ventajas derivadas del uso de MDM con directivas de protección de aplicaciones, y las empresas pueden usar MAM con y sin MDM al mismo tiempo. Por ejemplo, un empleado puede usar un teléfono de la compañía, así como una tableta personal. En este caso, el teléfono de la empresa está inscrito en MDM y está protegido por directivas de protección de aplicaciones, mientras que el dispositivo personal está protegido únicamente por directivas de protección de aplicaciones.

- **MDM garantiza que el dispositivo esté protegido.** Por ejemplo, puede solicitar un PIN para acceder al dispositivo o puede implementar aplicaciones administradas en el dispositivo. También puede implementar aplicaciones en dispositivos a través de la solución MDM para proporcionarle más control sobre la administración de aplicaciones.

- **Las directivas de protección de aplicaciones garantizan que las protecciones de la capa de aplicaciones estén establecidas.** Por ejemplo, puede tener una directiva que requiera un PIN para abrir una aplicación en un contexto de trabajo, evitar que los datos se compartan entre aplicaciones o evitar que los datos de la aplicación de la compañía se guarden en una ubicación de almacenamiento personal.

## <a name="devices-that-support-mam"></a>Dispositivos que admiten MAM
Actualmente, las directivas de protección de aplicaciones son compatibles con:
-   iOS 8.1 o posterior
-   Android 4 o posterior

>[!NOTE]
>Los dispositivos de Windows no se admiten en MAM sin el escenario de inscripción. En cambio, cuando inscribe los dispositivos Windows 10 en Intune, puede usar Windows Information Protection, ya que ofrece una funcionalidad similar. Para obtener más información, vea [Protege los datos de su empresa con Windows Information Protection (WIP)](https://technet.microsoft.com/itpro/windows/keep-secure/protect-enterprise-data-using-wip).


##  <a name="how-app-protection-policies-protect-app-data"></a>Protección de datos de una aplicación con directivas de protección de aplicaciones

###  <a name="apps-without-app-protection-policies"></a>Aplicaciones sin directivas de protección de aplicaciones

![Imagen que muestra cómo los datos se pueden mover libremente entre aplicaciones cuando no hay ninguna directiva de protección de aplicaciones establecida](../media/Apps_without_MAM_policies.png)

Cuando use aplicaciones sin restricciones, se pueden entremezclar los datos empresariales y personales. Los datos de la compañía podrían acabar en ubicaciones como el almacenamiento personal o transferidas a aplicaciones fuera de su ámbito, lo cual provocaría una pérdida de datos. Las flechas del diagrama muestran el movimiento sin restricciones de los datos entre aplicaciones (personales y corporativas) y hacia ubicaciones de almacenamiento.

### <a name="data-protection-with-app-protection-policies"></a>Protección de datos con directivas de protección de aplicaciones

![Imagen que muestra cómo se protegen los datos de la empresa cuando se aplican directivas de protección de aplicaciones](../media/Apps_with_mobile_app_policies.png)

Puede usar directivas de protección de aplicaciones para evitar que los datos de la empresa se guarden en el almacenamiento local del dispositivo y para restringir el movimiento de datos a otras aplicaciones que no estén protegidas por estas directivas. La configuración de directivas de protección de aplicaciones incluye:
- Directivas de reubicación de datos como **Impedir "Guardar como"**, **Restringir cortar, copiar y pegar**.
- Opciones de directivas de acceso como **Requerir PIN sencillo para el acceso**, **Bloquear las aplicaciones administradas para que no se ejecuten en dispositivos con jailbreak o rooting**.

### <a name="data-protection-with-app-protection-on-devices-that-are-managed-by-a-mdm-solution"></a>Protección de datos con directivas de protección de aplicaciones en dispositivos administrados por una solución MDM

![Imagen que muestra cómo funcionan las directivas de protección de aplicaciones en los dispositivos Bring Your Own Devices (BYOD)](../media/MAM_BYOD_November.png)

**Para los dispositivos inscritos en una solución MDM:** en el diagrama anterior se muestran las capas de protección que las directivas MDM y de protección de aplicaciones ofrecen juntas.

La solución MDM:

-   Inscribe el dispositivo.

-   Implementa las aplicaciones en el dispositivo.

-   Proporciona administración y conformidad continua de los dispositivos.

**Las directivas de protección de aplicaciones agregan valor porque:**

-   Ayudan a evitar la fuga de datos de la compañía a aplicaciones y servicios de consumidor.

-   Aplican restricciones (Guardar como, Portapapeles, PIN, etc.) a las aplicaciones móviles.

-   Borran datos de compañía de las aplicaciones sin borrar esas aplicaciones del dispositivo.


### <a name="data-protection-with-app-protection-policies-for-devices-without-enrollment"></a>Protección de datos con directivas de protección de aplicaciones para dispositivos sin inscripción

![Imagen que muestra cómo funcionan las directivas de protección de aplicaciones en dispositivos administrados](../media/MAM_ManagedDevices_November.png)

En el diagrama anterior se muestra cómo funcionan las directivas de protección de datos en el nivel de aplicación sin MDM.

En dispositivos BYOD no inscritos en ninguna solución MDM, las directivas de protección de aplicaciones pueden ayudar a proteger los datos de la compañía a nivel de aplicación.

Sin embargo, existen algunas limitaciones que se deben tener en cuenta:

-   No se puede implementar aplicaciones en el dispositivo. El usuario debe obtener las aplicaciones del almacén.

-   No se puede proporcionar perfiles de certificados en estos dispositivos.

-   No se puede establecer configuraciones de Wi-Fi y VPN de compañía en estos dispositivos.


## <a name="multi-identity"></a>Varias identidades

Las aplicaciones que admiten varias identidades permiten usar diferentes cuentas (profesionales y personales) para obtener acceso a las mismas aplicaciones, aunque las directivas de protección de aplicaciones se aplican solo cuando las aplicaciones se usen en el contexto laboral.  

Por ejemplo, cuando el usuario inicia la aplicación OneDrive con su cuenta profesional, no puede mover los archivos a una ubicación de almacenamiento personal. Sin embargo, cuando usa OneDrive con su cuenta personal, puede copiar y mover los datos de su OneDrive personal sin restricciones.  

- Obtenga más información sobre las aplicaciones que admiten [MAM y varias identidades](https://www.microsoft.com/cloud-platform/microsoft-intune-apps) con Intune.

##  <a name="next-steps"></a>Pasos siguientes
- [Preparativos para la configuración de directivas de protección de aplicaciones](get-ready-to-configure-mobile-app-management-policies-with-microsoft-intune.md)

- [Creación e implementación de directivas de protección de aplicaciones con Microsoft Intune](create-and-deploy-mobile-app-management-policies-with-microsoft-intune.md)

