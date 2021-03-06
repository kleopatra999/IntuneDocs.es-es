---
title: "Implementar la aplicación Lookout for Work | Microsoft Docs"
description: Configure e implemente aplicaciones Lookout for Work para Android.
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 03/21/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 524c4209-ad57-4d35-955e-a00d796bf858
ms.reviewer: sandera
ms.suite: ems
ms.custom: intune-classic
translationtype: Human Translation
ms.sourcegitcommit: e10453155343bb7fd91a4fd3874d393ef78d0b1a
ms.openlocfilehash: 44429b8694d15006f77a9eb5206293a6bcc8090b
ms.lasthandoff: 04/25/2017


---

# <a name="configure-and-deploy-lookout-for-work-app"></a>Configuración e implementación de aplicaciones Lookout for Work

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

En este artículo se explica cómo configurar e implementar la aplicación Lookout for Work para los dispositivos Android e iOS.

## <a name="android-google-play-store-app"></a>Android (aplicación Google Play Store)

1.    En la [Consola de administrador de Microsoft Intune](https://manage.microsoft.com), vaya a **Aplicaciones** y seleccione **Agregar aplicaciones**.
2.    En la página **Instalación de software** del publicador, seleccione **Vínculo externo** y especifique la dirección URL siguiente: https://play.google.com/store/apps/details?id=com.lookout.enterprise.
  >[!NOTE]
  >No haga clic en el cuadro para exigir un explorador administrado.

3.    En la página **Descripción del software**, rellene la información siguiente:
  * **Publicador:** Lookout Mobile Security
  * **Nombre:** Lookout for Work
  * **Descripción:** Lookout ofrece la mejor protección contra amenazas móviles para proteger el dispositivo. Cuando se instala la aplicación Lookout en el dispositivo, lo protege de amenazas y avisa, tanto a usted como al administrador de la empresa, si detecta alguna.
  * **Categoría:** administración de equipos

4. Una vez finalizado correctamente, aparece un mensaje **La carga de datos en Microsoft Intune se completó correctamente**.

  En la consola de Intune, al hacer clic en **Aplicaciones**, ahora verá la aplicación **Lookout for Work** en la lista ![captura de pantalla de la página de aplicaciones de la consola de administración de Intune con la aplicación Lookout for Work en la lista](../media/mtp/lookout-app-listed-intune-console.png).

5. Implemente la aplicación en los usuarios; para ello, seleccione la aplicación Lookout for Work y pulse **Administrar implementación**.

  Debe seleccionar los mismos usuarios que agregó en la opción Administración de la inscripción en la consola MTP de Lookout.  Vea el paso 3 de la sección [Configurar la suscripción con Lookout MTP](configure-and-deploy-lookout-for-work-apps.md) para obtener información sobre cómo agregar grupos de usuarios a Lookout MTP.

  >[!IMPORTANT]
  > El asistente para la implementación de aplicaciones de Intune no es consciente de los grupos de usuarios de Azure AD y usa los de Intune en su lugar. Por eso debe crear un grupo de usuarios de Intune basado en el de Azure AD que está inscrito en la consola de Lookout MTP, como se describe en [este](plan-your-user-and-device-groups.md) tema.

6. Seleccione la opción **Instalación requerida** para exigir que la aplicación Lookout se instale en el dispositivo del usuario.

## <a name="ios-enterprise-signed-version-of-lookout-app"></a>iOS (versión para empresa de la aplicación Lookout)

1. Asegúrese de que la **administración de iOS** está configurada en el dispositivo. Para saber cómo configurar el dispositivo para la administración de iOS, consulte [Configurar la administración de dispositivos iOS y Mac](set-up-ios-and-mac-management-with-microsoft-intune.md).

2. **Vuelva a firmar** la aplicación Lookout for Work de iOS. Lookout distribuye su aplicación Lookout for Work de iOS fuera de la tienda App Store de iOS. **Antes de distribuir la aplicación**, deberá volver a firmar la aplicación con su certificado de desarrollador empresarial de iOS. Para saber cómo volver a firmar las aplicaciones Lookout for Work de iOS, consulte [el proceso de volver a firmar de la aplicación Lookout for Work de iOS](https://personal.support.lookout.com/hc/articles/114094038714) en el sitio de Lookout.

3. Habilite la autenticación de Azure Active Directory para los usuarios de iOS haciendo lo siguiente:
  1.  Inicie sesión en el [portal de administración de Azure Active Directory](https://manage.windowsazure.com) y vaya a la página de aplicación.
  2.  Agregue la **aplicación Lookout for Work de iOS** como una **aplicación de cliente nativ**.
  ![captura de pantalla del cuadro de diálogo Agregar aplicaciones que muestra la opción de aplicación de cliente nativo](../media/mtp/aad-add-app.png)
  3. Reemplace **com.lookout.enterprise.yourcompanyname** por el ID de agrupación del cliente que ha seleccionado cuando se registró el IPA.
  4.  Agregue un URI de redirección adicional: **&lt;companyportal://code/>** seguido de una versión codificada por URL del URI de redirección original.
  5.  Agregue los **permisos delegados** a la aplicación.

  Para más información, consulte [Configurar una aplicación de cliente nativo](https://azure.microsoft.com/documentation/articles/app-service-mobile-how-to-configure-active-directory-authentication/#optional-configure-a-native-client-application).

4. Cargue el archivo .ipa que ha vuelto a firmar tal como se describe en el tema [Agregar aplicaciones a los dispositivos inscritos en Intune](https://docs.microsoft.com/intune/deploy-use/add-apps-for-mobile-devices-in-microsoft-intune). Establezca la versión mínima del sistema operativo en iOS 8.0 o posterior.

  ![captura de pantalla de la página de aplicaciones de la consola de administrador de Intune con la aplicación Lookout for Work, que se muestran en la lista de aplicaciones](../media/mtp/ios-app-uploaded-intune.png)

5. Cree la directiva de configuración de la aplicación administrada, tal como se describe en el tema [Configurar aplicaciones de iOS con directivas de configuración de aplicaciones móviles en Microsoft Intune](https://docs.microsoft.com/intune/deploy-use/configure-ios-apps-with-mobile-app-configuration-policies-in-microsoft-intune).

  ![captura de pantalla de la creación de un asistente para nueva directiva con la directiva de configuración de aplicación iOS 8.0 o posterior resaltada](../media/mtp/ios-app-config.png)

6. **Para implementar la aplicación en los usuarios**, seleccione la aplicación Lookout for Work y pulse **Administrar implementación**.

  Debe seleccionar los mismos usuarios que ha agregado en la opción Administración de la inscripción en la consola de Lookout.  Vea el paso 3 de la sección [Configurar la suscripción de Lookout](https://docs.microsoft.com/sccm/protect/deploy-use/configure-and-deploy-lookout-for-work-apps) para obtener información sobre cómo agregar grupos de usuarios a Lookout MTP.

  >[!IMPORTANT]
  > El Asistente para implementación de aplicaciones de Intune no es consciente de los grupos de usuarios de Azure AD y usa los de Intune en su lugar, por lo que debe crear un grupo de usuarios de Intune basado en el de Azure AD que está inscrito en la consola de Lookout, como se describe en [este](plan-your-user-and-device-groups.md) tema.

  Seleccione la opción **Instalación requerida** para exigir que la aplicación Lookout se instale en el dispositivo del usuario.

## <a name="what-happens-when-the-deployed-app-is-opened-on-the-device"></a>¿Qué ocurre cuando se abre la aplicación implementada en el dispositivo?
https://github.com/Microsoft/Docs/blob/master/ContributorGuide/index.md Cuando el usuario abre Lookout for Work en el dispositivo, se le pide que active la aplicación y que seleccione la opción Iniciar sesión con Azure Active Directory. En los temas siguientes encontrará un tutorial detallado con el flujo para el usuario final:

* [Se le pide instalar Lookout for Work en un dispositivo Android](https://docs.microsoft.com/intune/enduser/you-are-prompted-to-install-lookout-for-work-android)

* [Debe solucionar una amenaza detectada por Lookout for Work en el dispositivo Android](https://docs.microsoft.com/intune/enduser/you-need-to-resolve-a-threat-found-by-lookout-for-work-android)

## <a name="next-steps"></a>Pasos siguientes
* [Creación de la directiva de cumplimiento de dispositivos de Lookout en Intune](https://docs.microsoft.com/sccm/protect/deploy-use/enable-device-threat-protection-rule-compliance-policy)

