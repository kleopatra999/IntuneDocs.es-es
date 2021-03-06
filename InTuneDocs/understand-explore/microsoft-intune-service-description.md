---
title: "Descripción del servicio | Microsoft Docs"
description: Intune es un servicio basado en la nube que le ayuda a administrar dispositivos Windows, iOS, Mac OS X, Android y Windows Mobile.
keywords: 
author: lindavr
ms.author: lindavr
manager: angrobe
ms.date: 09/22/2016
ms.topic: get-started-article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 40fa5a2e-6c0f-4150-9740-d5ddc0cdbda0
ms.reviewer: cacamp
ms.suite: ems
ms.custom: intune-classic
translationtype: Human Translation
ms.sourcegitcommit: ab6d9b6b296fb4e1fb0aaa9496fede28976728dc
ms.openlocfilehash: 5975ba0219f464c8f5aa1735657ff3d1c186b991
ms.lasthandoff: 04/14/2017


---

# <a name="microsoft-intune-service-description"></a>Descripción del servicio Microsoft Intune

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

Microsoft Intune es un servicio basado en la nube que le ayuda a administrar dispositivos que ejecutan Windows, Mac OS X, iOS, Android y Windows Mobile. Asimismo, Intune le ayudará a proteger los datos y las aplicaciones de su empresa. Puede usar Intune por sí solo o puede integrarlo con System Center Configuration Manager para ampliar sus capacidades de administración.

Microsoft le ofrece los beneficios propios de la incorporación a Intune para aquellos servicios válidos que se encuentren en planes aptos. El beneficio de incorporación le permite trabajar de forma remota con los especialistas de Microsoft para preparar el entorno de Intune para su uso. Para obtener más información sobre el beneficio de incorporación, consulte [Microsoft Intune Onboarding Benefit Description](http://go.microsoft.com/fwlink/?LinkId=619281) (Descripción del beneficio de incorporación de Microsoft Intune).

Puede empezar a usar Intune con una versión de evaluación gratuita de 30 días que incluye 100 licencias de usuario. Para iniciar la versión de prueba gratuita, [vaya a la página de registro de Intune](https://www.microsoft.com/server-cloud/products/microsoft-intune/). Si su organización tiene un contrato Enterprise o un contrato de licencias por volumen equivalente, póngase en contacto con su representante de Microsoft para configurar la versión de evaluación gratuita.

> [!NOTE]
> Si su organización tiene una cuenta profesional o educativa de Microsoft Online Services y es posible que continúe con esta suscripción de Intune en producción una vez finalizado el período de evaluación, elija la opción **Iniciar sesión** de esa página y autentíquese con la cuenta de administrador global de su organización. Esta acción garantizará que su versión de evaluación de Intune se vincula con su cuenta de trabajo o académica existente.

Para obtener una lista de las opciones que puede configurar en los dispositivos móviles, consulte:

-   [Funcionalidades de administración de dispositivos inscritos en Microsoft Intune](/intune/get-started/mobile-device-management-capabilities-in-microsoft-intune)

-   [Administración híbrida de dispositivos móviles (MDM) con System Center Configuration Manager y Microsoft Intune](https://technet.microsoft.com/library/mt627883.aspx)

Para obtener más información sobre System Center Configuration Manager, consulte la [Documentación para System Center Configuration Manager](https://technet.microsoft.com/library/mt346023.aspx).

## <a name="learn-how-intune-service-updates-affect-you"></a>Obtenga información sobre cómo le afectan las actualizaciones del servicio de Intune.
Dado que Intune es un servicio en línea, Microsoft puede actualizarlo de forma periódica.

Use la información de este artículo para obtener información sobre la frecuencia con la que se realizan estas actualizaciones de servicio y las notificaciones que le enviamos cuando una actualización puede afectar a su uso del servicio.

Para conocer más detalles sobre los cambios en el servicio de Intune, consulte [Novedades de Microsoft Intune](/intune/deploy-use/whats-new-in-microsoft-intune). En el [Blog de Microsoft Intune](http://blogs.technet.com/b/microsoftintune/) también se describen los cambios que se realizan en el servicio y se proporcionan sugerencias útiles para permitirle sacar el máximo provecho a Intune.

También se le comunicarán actualizaciones importantes del servicio en el Centro de mensajes del [portal de administración de Office 365](https://portal.office.com/Admin/Default.aspx). Si instala la [aplicación móvil complementaria de Office 365 Admin](https://support.office.com/article/Office-365-Admin-Mobile-App-e16f6421-2a1a-4142-bf9d-9846600a060a), podrá recibir notificaciones en su dispositivo móvil.

> [!NOTE]
> Puede supervisar el mantenimiento del servicio Intune en el [portal de administración de Office 365](https://portal.office.com/Admin/Default.aspx). Elija **Mantenimiento del servicio** en el panel izquierdo.  

Estos son los tipos de notificaciones que Microsoft proporciona sobre el servicio Intune:
-   Para ayudarle a planear los cambios de servicio, le notificamos con un plazo mínimo de entre 30 y 90 días antes de la actualización del servicio, en función de las repercusiones del cambio. Esto ocurrirá al usar canales de comunicación del producto como las alertas del tablón de anuncios. Entre estos cambios pueden incluirse los siguientes:
    * Actualizaciones que podrían tener algún impacto en las disposiciones legales o en su cumplimiento
    * Cambios en la experiencia de usuario, la interfaz de usuario y los flujos de trabajo
    * API nuevas o modificadas: recibirá una notificación indicándole que necesita probar las aplicaciones personalizadas para garantizar la compatibilidad con versiones anteriores
    * Cambios en los requisitos del sistema, por ejemplo, la versión mínima necesaria del explorador
    * Cualquier actualización que requiera que tome medidas para habilitar la característica o para evitar la interrupción del servicio a la función.
-   En la actualización de servicio mensual, Microsoft proporciona información sobre nuevas características, nuevas funciones y mejoras en las características existentes. Por lo general, Microsoft implementa las actualizaciones del servicio a mediados de cada mes. Las actualizaciones se describen en [Novedades de Microsoft Intune](/intune/deploy-use/whats-new-in-microsoft-intune).
    -   En caso de retirada del servicio de Intune, sería notificado con 12 meses de antelación.

## <a name="choose-the-management-solution-thats-right-for-you"></a>Elegir la solución de administración que más le conviene
Puede configurar Intune de diversas maneras para administrar y proteger los dispositivos móviles y los equipos de su empresa (en adelante los denominaremos **dispositivos** en este artículo).

-**Configuración de Intune independiente.** Use la consola de administración basada en web de Intune para administrar los dispositivos de su organización. Intune se puede usar sin una infraestructura de TI local. Si se usa Intune con Active Directory Domain Services, pueden emplearse las cuentas de usuario de dominio que se administran con Domain Services mediante Intune.

-**Intune con System Center Configuration Manager.** Use la consola de administración de Configuration Manager para administrar los equipos y dispositivos móviles de su empresa. Esta configuración puede ayudarle a administrar todos los dispositivos de la organización a través de una única consola, la consola de administración de Configuration Manager. Configuration Manager admite grandes cantidades de dispositivos móviles, servidores y equipos. Para obtener más información sobre Configuration Manager, consulte [Administración híbrida de dispositivos móviles (MDM) con System Center Configuration Manager y Microsoft Intune](https://technet.microsoft.com/library/mt627883.aspx). Para obtener más ayuda para decidir qué enfoque es adecuado para usted, vea [Choose between Microsoft Intune standalone and hybrid mobile device management with Configuration Manager (Elegir entre Microsoft Intune independiente y la administración de dispositivos móviles híbrida con Configuration Manager)](https://technet.microsoft.com/library/mt706478.aspx).


## <a name="learn-more-about-intune"></a>Obtenga más información acerca de Intune
Use estos recursos para obtener más información acerca de Intune:

- En el [Centro de confianza de Microsoft Intune](https://www.microsoft.com/server-cloud/products/intune-trust-center/) se proporciona información sobre las prácticas de seguridad, privacidad y cumplimiento de Intune y se describen algunas certificaciones de Intune.

- [Funcionalidades de administración de dispositivos inscritos en Microsoft Intune](/intune/get-started/mobile-device-management-capabilities-in-microsoft-intune)

### <a name="see-also"></a>Consulte también
[Microsoft Intune](https://docs.microsoft.com/intune/)
[Biblioteca de documentación de System Center 2012 Configuration Manager](https://technet.microsoft.com/library/gg682041.aspx)

[Novedades de Microsoft Intune](/intune/deploy-use/whats-new-in-microsoft-intune)

