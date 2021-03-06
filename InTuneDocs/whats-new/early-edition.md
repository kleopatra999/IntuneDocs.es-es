---
title: "Edición anticipada | Microsoft Docs"
description: 
keywords: 
author: mtillman
ms.author: mtillman
manager: angrobe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: f49650f4-31fa-406c-a4da-d8c9a4a8384d
ROBOTS: NOINDEX,NOFOLLOW
ms.reviewer: cacampbell
ms.suite: ems
ms.custom: intune-classic
ms.translationtype: Human Translation
ms.sourcegitcommit: 5f172290d493717308446c4f9e2313a03ba8f3aa
ms.openlocfilehash: d7f25657fc7cfb9298809f76f198810718e58c39
ms.contentlocale: es-es
ms.lasthandoff: 04/27/2017


---


# <a name="the-early-edition-for-microsoft-intune---april-2017"></a>Edición anticipada para Microsoft Intune - Abril de 2017

La **edición anticipada** proporciona una lista de características que se incluirán en las próximas versiones de Microsoft Intune. Esta información se proporciona conforme al acuerdo de confidencialidad en una base extremadamente limitada y está vinculada a cambios. Algunas de las características enumeradas aquí corren el riesgo de no cumplir las fechas límite y pueden retrasarse hasta una versión futura. Otras características se están probando en una prueba piloto (distribución de paquetes piloto) para asegurarse de que están preparadas para el cliente. Póngase en contacto con su persona conocida de Intune o PM si tiene alguna pregunta o problema.

Esta página se actualiza periódicamente. Compruebe si hay actualizaciones adicionales.

> [!Note]
> Los siguientes cambios están en fase de desarrollo de Intune. Todas estas funciones se admitirán finalmente para las implementaciones de los clientes híbridos (Configuration Manager con Intune). Para obtener más información sobre las nuevas funciones híbridas, consulte nuestra [página Novedades](https://docs.microsoft.com/sccm/mdm/understand/whats-new-in-hybrid-mobile-device-management).

## <a name="new-capabilities"></a>Nuevas funcionalidades

### <a name="improved-app-install-status-for-the-windows-10-company-portal-app---676495--"></a>Mejora del estado de instalación de la aplicación para la aplicación Portal de empresa de Windows 10 <!--676495-->

La aplicación Portal de empresa de Windows 10 ahora proporcionará la barra de progreso de instalación de la aplicación para todas las instalaciones de aplicaciones modernas iniciadas desde el Portal de empresa. Puede ver los nuevos mensajes de estado de la aplicación Portal de empresa para Windows 10 en la [página de novedades de la interfaz de usuario de la aplicación Intune](whats-new-in-intune-app-ui.md).

### <a name="improved-status-messaging-in-the-company-portal-app-for-ios---744866--"></a>Mejora de la mensajería de estado en la aplicación Portal de empresa para iOS<!--744866-->

Mensajes de error nuevos y más específicos que se mostrarán dentro de la aplicación Portal de empresa para iOS para proporcionar información más accesible sobre lo que sucede en los dispositivos. Estos casos de error anteriormente se incluían en un mensaje de error general titulado "Portal de empresa no disponible temporalmente". Además, si un usuario inicia el Portal de empresa en iOS cuando no tiene una conexión a Internet, ahora aparecerá una barra de estado persistente en la página principal con el mensaje "No hay conexión a Internet".

### <a name="myapps-available-for-managed-browser---822308-822303--"></a>MyApps está disponible para Managed Browser <!--822308, 822303-->

Ahora, Microsoft MyApps ofrece una mejor compatibilidad con Managed Browser. Los usuarios de Managed Browser que no estén destinados a la administración se redirigirán directamente al servicio MyApps, donde podrán acceder a sus aplicaciones de SaaS aprovisionadas por el administrador. Los usuarios destinados a la administración de Intune seguirán teniendo acceso a MyApps desde el marcador de Managed Browser integrado.

### <a name="new-icons-for-the-managed-browser-and-the-company-portal---918433-918431--"></a>Nuevos iconos para Managed Browser y Portal de empresa <!--918433, 918431-->

Managed Browser recibirá iconos actualizados para la versión de la aplicación de Android y la de iOS. El nuevo icono contendrá la notificación de Intune actualizada para que sea más coherente con otras aplicaciones de Enterprise Mobility + Security (EM+S). Puede ver el icono nuevo de Managed Browser en la [página de novedades de la UI de la aplicación de Intune](whats-new-in-intune-app-ui.md).

Portal de empresa también recibirá iconos actualizados para las versiones de Windows, iOS y Android de la aplicación a fin de mejorar la coherencia con otras aplicaciones de EM+S. Estos iconos se lanzarán gradualmente en las distintas plataformas desde abril hasta finales de mayo.

### <a name="single-sign-on-support-from-the-company-portal-for-ios-to-outlook-for-ios---834012--"></a>Compatibilidad del inicio de sesión único desde Portal de empresa para iOS a Outlook para iOS <!--834012-->

Los usuarios ya no tienen que iniciar sesión en la aplicación Outlook si han iniciado sesión en la aplicación Portal de empresa para iOS en el mismo dispositivo con la misma cuenta. Cuando los usuarios inician la aplicación Outlook, podrán seleccionar su cuenta e iniciar sesión automáticamente. También estamos trabajando para agregar esta funcionalidad para otras aplicaciones de Microsoft.

### <a name="sign-in-progress-indicator-in-android-company-portal---953374--"></a>Indicador de progreso de inicio de sesión en Portal de empresa para Android <!--953374-->

Una actualización de la aplicación Portal de empresa para Android muestra un indicador de progreso de inicio de sesión cuando el usuario inicia o reanuda la aplicación. El indicador avanza por los nuevos estados, desde "Conectando..." e "Iniciando sesión..." hasta "Comprobando los requisitos de seguridad...", antes de permitir que el usuario acceda a la aplicación. Puede ver las nuevas pantallas de la aplicación Portal de empresa para Android en la [página de novedades de la UI de la aplicación Intune](whats-new-in-intune-app-ui.md).


## <a name="notices"></a>Notificaciones

### <a name="apple-to-require-updates-for-application-transport-security---748318--"></a>Apple requiere actualizaciones para su funcionalidad de seguridad de transporte de aplicaciones <!--748318-->

A partir de la primavera de 2017, Apple ha anunciado que exigirán requisitos específicos para la seguridad de transporte de aplicaciones (ATS). ATS se utiliza para exigir una seguridad más estricta en todas las comunicaciones de aplicación a través de HTTPS. Este cambio afecta a los clientes de Intune que usan aplicaciones de Portal de empresa para iOS. Revise nuestro [blog de soporte técnico de Intune](https://aka.ms/compportalats) para más detalles.

### <a name="direct-access-to-apple-enrollment-scenarios---951869--"></a>Acceso directo a escenarios de inscripción de Apple <!--951869-->

Para las cuentas de Intune creadas después de enero de 2017, Intune ha habilitado el acceso directo a los escenarios de inscripción de Apple mediante la carga de trabajo Inscribir los dispositivos en el Portal de vista previa de Azure. Anteriormente, solo se podía acceder a la versión preliminar de inscripción de Apple desde los vínculos del portal clásico de Intune. Las cuentas de Intune creadas antes de enero de 2017 requerirán una migración única antes de que estas características estén disponibles en Azure. Aún no se ha anunciado la programación para la migración, pero pronto habrá detalles disponibles. Se recomienda encarecidamente crear una cuenta de prueba para probar la nueva experiencia si su cuenta existente no puede acceder a la versión preliminar.

### <a name="whats-coming-for-appx-in-intune-on-azure----1000270---"></a>Novedades para Appx en Intune en Azure<!-- 1000270 -->

Como parte de la migración a Intune en Azure, vamos a llevar a cabo tres cambios en appx:

1. Incorporación de un nuevo tipo de aplicación appx en la consola clásica de Intune que solo se puede implementar en dispositivos inscritos en MDM.
2. Reutilización del tipo de aplicación appx existente para que solo se dirija a equipos administrados a través del agente de PC de Intune.
3. Conversión de todos los appx existentes en appx MDM con la migración.

#### <a name="how-does-this-affect-me"></a>¿Cómo me afecta esto ahora?

Esto no afectará a ninguna de sus implementaciones actuales en dispositivos administrados a través del agente de PC de Intune. Sin embargo, tras la migración, no podrá implementar esos appx migrados a ningún dispositivo nuevo que se administre a través del agente de PC de Intune que estuviera establecido como destino previamente.

#### <a name="what-action-do-i-need-to-take"></a>Qué acción necesito realizar

Tras la migración, debe volver a cargar el appx de nuevo como un appx de PC si desea hacer nuevas implementaciones de PC. Para más información, consulte [Appx changes in Intune on Azure](https://aka.ms/appxchange) (Cambios de appx en Intune en Azure) en el blog del equipo de soporte técnico de Intune.  


## <a name="public-preview-of-the-new-intune-admin-experience-on-azure---736542--"></a>Versión preliminar pública de la nueva experiencia de administración de Intune en Azure <!--736542-->

A principios de 2017, migraremos nuestra experiencia de administración completa a Azure, lo que permitirá una administración versátil e integrada de los flujos de trabajo de EMS principales en una plataforma de servicio moderna extensible mediante API Graph.

Los nuevos inquilinos de prueba comenzarán a ver la versión preliminar pública de la nueva experiencia de administración en Azure Portal este mes. Mientras se esté en el estado de versión preliminar, las funcionalidades y la paridad con la consola de Intune existente se entregarán de forma iterativa.

La experiencia de administración de Azure Portal usará la nueva funcionalidad de agrupación y destino ya anunciadas; cuando el inquilino existente se migra a la nueva experiencia de agrupación, también se migra a la versión preliminar la nueva experiencia de administración en el inquilino. Mientras tanto, si desea probar o consultar cualquiera de las nuevas funcionalidades hasta que se migre el inquilino, regístrese para una nueva cuenta de prueba de Intune o consulte la [nueva documentación](https://docs.microsoft.com/intune-azure/introduction/what-is-microsoft-intune).

### <a name="support-for-managed-configuration-options-for-android-apps----621621---"></a>Compatibilidad con las opciones de configuración administrada para aplicaciones Android <!-- 621621 -->

Las aplicaciones Android de Google Play Store que admiten opciones de configuración administrada se puede configurar mediante Intune.  Esta característica permite a TI ver la lista de valores de configuración que admite una aplicación y proporciona una interfaz de usuario guiada y de primera clase que permite configurar esos valores.

### <a name="remote-assistance-for-android-devices----675418---"></a>Asistencia remota para dispositivos Android <!-- 675418 -->

Intune usará el software [TeamViewer](https://www.teamviewer.com), adquirido por separado, para que pueda ofrecer asistencia remota a los usuarios que ejecutan dispositivos Android.

### <a name="new-android-policy-for-complex-pins----722069---"></a>Nueva directiva de Android para PIN complejos <!-- 722069 -->

Puede establecer un tipo de serie numérica de contraseña requerido en un perfil de dispositivo Android para dispositivos que ejecutan Android 5.0 y versiones posteriores.  Utilice esta opción para impedir que los usuarios de dispositivos creen un PIN que contenga números repetidos o consecutivos, como 1111 o 1234.

### <a name="additional-support-for-android-for-work-devices"></a>Soporte adicional para dispositivos Android for Work

- **Administración de la configuración de contraseñas y perfiles profesionales** <!-- 612808 -->

  Hemos agregado una nueva directiva de restricción de dispositivos Android for Work que permite administrar la configuración de contraseñas y perfiles profesionales en dispositivos Android for Work que administra.

- **Permiso del uso compartido de datos entre perfiles profesionales y personales** <!-- 1045102 -->

  Hemos actualizado la opción de configuración **Uso compartido de datos entre el perfil profesional y el personal** en un perfil de restricción de dispositivos Android for Work con nuevas opciones para ayudarle a configurar el uso compartido de datos entre perfiles profesionales y personales.

- **Restricción de copia y pegado entre perfiles profesionales y personales** <!-- 1046094 -->

  Cuando administra dispositivos Android for Work con Intune, se permiten acciones de copiar y pegar entre aplicaciones profesionales y personales. Ahora hemos agregado un perfil de dispositivo personalizado para dispositivos Android for Work que permite restringir si se permiten acciones de copiar y pegar entre aplicaciones profesionales y personales.

### <a name="assign-lob-apps-to-ios-and-android-devices----1057568---"></a>Asignación de aplicaciones de línea de negocio a dispositivos iOS y Android <!-- 1057568 -->

Puede asignar aplicaciones de línea de negocio para iOS (archivos .ipa) y Android (archivos .apk) a usuarios o dispositivos.

###  <a name="new-policies-for-ios-devices----723774-723815-723826-723830-723832---"></a>Nuevas directivas para dispositivos iOS <!-- 723774, 723815, 723826, 723830, 723832 -->

- **Aplicaciones en la pantalla de inicio**: puede utilizar una directiva de dispositivo para controlar qué aplicaciones ven los usuarios en la pantalla de inicio de su dispositivo iOS. Esta directiva cambia el diseño de la pantalla de inicio, pero no implementa ninguna aplicación que haya especificado que no se instale.

- **Conexiones con dispositivos AirPrint**: puede utilizar una directiva de dispositivo de Intune para controlar a qué dispositivos AirPrint (impresoras de red) se pueden conectar los usuarios finales de dispositivos iOS.

- **Conexiones con dispositivos AirPlay**: puede utilizar una directiva de dispositivo de Intune para controlar a qué dispositivos AirPlay (como Apple TV) se pueden conectar los usuarios finales de dispositivos iOS.

- **Mensaje personalizado de la pantalla de bloqueo**: puede configurar un mensaje personalizado que los usuarios verán en la pantalla de bloqueo de su dispositivo iOS, que reemplaza al mensaje de la pantalla de bloqueo predeterminado.

- **Filtro de contenido web**: puede controlar qué sitios web pueden visitar los usuarios de dispositivos iOS mediante uno de los dos métodos siguientes:

  - Agregar direcciones URL permitidas y bloqueadas utilizando un filtro de contenido web integrado de Apples.
  - Permitir que el explorador Safari solo pueda acceder a sitios web especificados. Se crearán marcadores en Safari para cada sitio que especifique.


### <a name="restrict-push-notifications-for-ios-apps----723767---"></a>Restringir las notificaciones de inserción para aplicaciones iOS<!-- 723767 -->

En un perfil de restricción de dispositivos de Intune, puede definir la siguiente configuración de notificación para dispositivos iOS:

- Activar o desactivar totalmente la notificación para una aplicación especificada.
- Activar o desactivar la notificación en el centro de notificaciones para una aplicación especificada.
- Especificar el tipo de alerta, ya sea **None** (Ninguna), **Banner** (Mensaje emergente) o **Modal Alert** (Alerta modal).
- Especificar si se permiten los distintivos para esta aplicación.
- Especificar si se permiten los sonidos de notificaciones.

### <a name="configure-ios-apps-to-run-in-single-app-mode-autonomously----737837---"></a>Configurar aplicaciones iOS para que se ejecuten en el modo de aplicación única de forma autónoma <!-- 737837 -->

Puede usar un perfil de dispositivo de Intune para configurar dispositivos iOS de modo que ejecuten aplicaciones especificadas en modo de aplicación única autónoma. Cuando se configura este modo y se ejecuta la aplicación, el dispositivo se bloquea para que solo pueda ejecutar esa aplicación. Un ejemplo es cuando se configura una aplicación que permite a los usuarios hacer una prueba en el dispositivo. Cuando se completan las acciones de la aplicación, o quita esta directiva, el dispositivo vuelve a su estado normal.

### <a name="configure-trusted-domains-for-email-and-web-browsing-on-ios-devices----723765---"></a>Configurar dominios de confianza para el correo electrónico y la exploración web en dispositivos iOS <!-- 723765 -->

Desde un perfil de restricción de dispositivos iOS, puede configurar los valores de dominio siguientes:

- **Dominios de correo electrónico sin marcar**: los correos electrónicos que el usuario envía o recibe y no coinciden con los dominios que especifique aquí se marcarán como que no son de confianza.

- **Dominios web administrados**: los documentos que se descargan de las direcciones URL que especifique aquí se considerarán administrados (solo en Safari).  

- **Dominios de relleno automático de contraseña de Safari**: los usuarios pueden guardar en Safari las contraseñas solo de las direcciones URL que coincidan con los patrones que especifique aquí. Para usar esta opción, el dispositivo debe estar en modo supervisado y no estar configurado para varios usuarios. (iOS 9.3 y versiones posteriores)


### <a name="vpp-apps-available-in-ios-company-portal----748782---"></a>Aplicaciones de PCV disponibles en el Portal de empresa de iOS <!-- 748782 -->

Puede asignar aplicaciones de compras por volumen (PCV) de iOS como instalaciones **Disponibles** para usuarios finales. Los usuarios finales necesitarán una cuenta de Apple Store para instalar la aplicación.

### <a name="synchronize-ebooks-from-apple-vpp-store----800878---"></a>Sincronizar libros electrónicos de la tienda de compras por volumen de Apple <!-- 800878 -->

Puede sincronizar los libros que haya adquirido a través de la tienda del programa de compras por volumen de Apple con Intune y asignarlos a los usuarios.

### <a name="multi-user-management-for-samsung-knox-standard-devices----971988---"></a>Administración de varios usuario para dispositivos Samsung KNOX Standard<!-- 971988 -->

Intune ahora es compatible con dispositivos que ejecutan Samsung KNOX Standard para la administración de varios usuarios. Esto significa que los usuarios finales pueden iniciar y cerrar sesión en el dispositivo con sus credenciales de Azure Active Directory, y que el dispositivo se administra centralmente tanto si está en uso como si no.  Cuando los usuarios finales inician sesión, tienen acceso a aplicaciones, además de las directivas aplicadas a ellas. Cuando los usuarios cierran sesión, se borran todos los datos de la aplicación.

### <a name="additional-windows-device-restriction-settings----818566---"></a>Configuración adicional de restricción de dispositivos Windows <!-- 818566 -->

Hemos agregado compatibilidad con opciones de configuración adicionales de restricción de dispositivos Windows, como la compatibilidad adicional con el explorador Edge, la personalización de la pantalla de bloqueo del dispositivo, las personalizaciones del menú Inicio, el papel tapiz del conjunto de búsqueda de Contenido destacado de Windows y la configuración de proxy.

### <a name="multi-user-support-for-windows-10-creators-update----822547---"></a>Compatibilidad con varios usuarios para Windows 10 Creators Update <!-- 822547 -->

Hemos agregado compatibilidad para la administración de varios usuarios en dispositivos que ejecutan Windows 10 Creators Update y están unidos al dominio de Azure Active Directory. Esto significa que cuando varios usuarios estándar inicien sesión en el dispositivo con sus credenciales de Azure AD, recibirán las aplicaciones y las directivas que se hayan asignado a sus nombres de usuario. Actualmente, los usuarios no puede usar Portal de empresa para escenarios de autoservicio, como la instalación de aplicaciones.

### <a name="fresh-start-for-windows-10-pcs---1004830---"></a>Fresh Start para equipos con Windows 10<!-- 1004830 -->

En esta versión, hay disponible una nueva acción de dispositivo Fresh Start para equipos Windows 10.  Cuando se lleva a cabo esta acción, se quitan las aplicaciones que hubiera instaladas en el equipo y este se actualiza automáticamente a la versión más reciente de Windows. Esto puede servir para ayudar a quitar las aplicaciones de OEM preinstaladas que a menudo se entregan con los nuevos equipos. Puede configurar si se conservan los datos de usuario cuando se lleva a cabo esta acción de dispositivo.

### <a name="additional-windows-10-upgrade-paths----903672---"></a>Rutas de actualización adicionales de Windows 10 <!-- 903672 -->

Ahora puede crear una directiva de actualización de edición para actualizar los dispositivos a las siguientes ediciones adicionales de Windows 10:

- Windows 10 Professional
- Windows 10 Professional N
- Windows 10 Professional Education
- Windows 10 Professional Education N

### <a name="bulk-enroll-windows-10-devices----747607---"></a>Inscripción masiva de dispositivos Windows 10 <!-- 747607 -->

Ahora puede unir grandes cantidades de dispositivos que ejecutan Windows 10 Creator Update a Azure Active Directory e Intune con el Diseñador de configuración de Windows (WCD). Para habilitar la inscripción masiva de MDM para el inquilino de Azure AD, cree un paquete de aprovisionamiento que una dispositivos al inquilino de Azure AD a través del Diseñador de configuración de Windows y aplique el paquete a los dispositivos corporativos que desea inscribir y administrar de forma masiva. Una vez que el paquete se aplica a los dispositivos, se unirán a Azure AD, se inscribirán en Intune y estarán listos para que los usuarios de Azure AD inicien sesión.  Los usuarios de Azure AD son usuarios estándar en estos dispositivos y reciben las aplicaciones requeridas y las directivas asignadas. En este momento, no se admiten los escenarios de autoservicio ni de Portal de empresa.

### <a name="new-mam-settings-for-pin-and-managed-storage-locations----58112-736644---"></a>Nueva configuración de MAM para PIN y ubicaciones de almacenamiento administrado <!-- 58112, 736644 -->

Hay disponibles dos nuevas opciones de configuración de aplicaciones que le ayudarán con los escenarios de administración de aplicaciones móviles (MAM):

- **Disable app PIN when device PIN is managed (Deshabilitar el PIN de aplicación cuando se administra el PIN del dispositivo)**: detecta si hay un PIN de dispositivo en el dispositivo inscrito y, si es así, omite el PIN de aplicación desencadenado por las directivas de protección de aplicaciones. Esta configuración permitirá reducir el número de veces que se muestra una solicitud de PIN a los usuarios que abran una aplicación habilitada para MAM en un dispositivo inscrito. Esta característica está disponible para iOS y Android.

- **Seleccione en qué servicios de almacenamiento se puede guardar datos empresariales**: permite especificar en qué ubicaciones de almacenamiento quiere guardar los datos corporativos. Los usuarios pueden guardar en los servicios de ubicación de almacenamiento seleccionados, lo que implica que se bloquearán todos los demás servicios de ubicación de almacenamiento no indicados.

  Lista de servicios de ubicación de almacenamiento admitidos:

  - OneDrive
  - Business SharePoint Online
  - Almacenamiento local


### <a name="see-also"></a>Consulte también
Consulte [Novedades de Microsoft Intune](whats-new-in-microsoft-intune.md) para más información sobre los desarrollos recientes.

