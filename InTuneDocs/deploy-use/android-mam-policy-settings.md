---
title: "Opciones de configuración de directiva de MAM de Android | Microsoft Docs"
description: "En este tema se describe la configuración de directiva de administración de aplicaciones móviles para dispositivos Android."
keywords: 
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 04/18/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 5dbb702a-1df5-4637-95c9-77a5f0b1a0e3
ms.reviewer: andcerat
ms.suite: ems
ms.custom: intune-classic
ms.translationtype: Human Translation
ms.sourcegitcommit: 33febef8787887401960592d95356347f6917681
ms.openlocfilehash: 017c316ce102b71b3ef9552d8fe69181b79473de
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---

# <a name="android-app-protection-policy-settings-in-microsoft-intune"></a>Configuración de directivas de protección de aplicaciones Android en Microsoft Intune

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

La configuración de directivas de aplicaciones que se describe en este tema se puede [configurar](create-and-deploy-mobile-app-management-policies-with-microsoft-intune.md) en la hoja **Configuración** de Azure Portal.
Existen dos categorías de configuración de directiva: configuración de acceso y configuración de reubicación de datos. En este tema, el término _**aplicaciones administradas por directivas**_ hace referencia a las aplicaciones que están configuradas con directivas de protección de aplicaciones.

##  <a name="data-relocation-settings"></a>Configuración de reubicación de datos

| Configuración | Cómo se usa | Valores predeterminados |
|------|------|------|
| **Impedir copias de seguridad de Android** | Pulse **Sí** para impedir que esta aplicación realice copias de seguridad de datos profesionales o educativos en el [Servicio de copia de seguridad de Android](https://developer.android.com/google/backup/index.html). Pulse **No** para permitir que esta aplicación realice copias de seguridad de datos profesionales o educativos.| Sí |
| **Permitir que la aplicación transfiera datos a otras aplicaciones** | Especifique qué aplicaciones pueden recibir datos de esta aplicación: <ul><li> **Aplicaciones administradas por directivas**: permite las transferencias solo para otras aplicaciones administradas por directivas.</li> <li>**Todas las aplicaciones**: permite la transferencia a cualquier aplicación. </li> <li>**Ninguna**: no permite la transferencia de datos a ninguna aplicación, incluidas otras aplicaciones administradas por directivas.</li></ul> <p>Hay aplicaciones y servicios exentos a los que Intune puede permitir la transferencia de datos. Consulte [Exenciones de transferencia de datos](#Data-transfer-exemptions) para ver una lista completa de aplicaciones y servicios.| Todas las aplicaciones |
| **Permitir que la aplicación reciba datos de otras aplicaciones** | Especifique qué aplicaciones pueden transferir datos a esta aplicación: <ul><li>**Aplicaciones administradas por directivas**: permite las transferencias solo desde otras aplicaciones administradas por directivas.</li><li>**Todas las aplicaciones**: permite la transferencia de datos desde cualquier aplicación.</li><li>**Ninguna**: no permite la transferencia de datos desde ninguna aplicación, incluidas otras aplicaciones administradas por directivas. </li></ul> <p>Hay aplicaciones y servicios exentos desde los que Intune puede permitir la transferencia de datos. Consulte [Exenciones de transferencia de datos](#Data-transfer-exemptions) para ver una lista completa de aplicaciones y servicios. | Todas las aplicaciones |
| **Impedir "Guardar como"** | Pulse **Sí** para deshabilitar el uso de la opción Guardar como en esta aplicación. Elija **No** si quiere permitir el uso de Guardar como. <p><br>**Seleccione en qué servicios de almacenamiento se pueden guardar datos empresariales** <br>Los usuarios pueden guardar en los servicios seleccionados (OneDrive para la Empresa, SharePoint y almacenamiento local). El resto de servicios se bloquearán.</p> | No <br><br> 0 servicios seleccionados |
| **Restringir cortar, copiar y pegar con otras aplicaciones** | Especifique cuándo pueden usarse las acciones de cortar, copiar y pegar con esta aplicación. Elija de entre las siguientes opciones: <ul><li>**Bloqueado**: no permite las acciones de cortar, copiar y pegar entre esta aplicación y cualquier otra.</li><li>**Aplicaciones administradas por directivas**: permite las acciones de cortar, copiar y pegar entre esta aplicación y otras aplicaciones administradas por directivas.</li><li>**Aplicaciones administradas por directivas con pegar**: permite cortar o copiar entre esta aplicación y otras aplicaciones administradas por directivas. Permite que los datos de cualquier aplicación se peguen en esta aplicación.</li><li>**Cualquier aplicación**: no se aplican restricciones a las acciones de cortar, copiar y pegar para y desde esta aplicación. | Cualquier aplicación |
|**Restringir contenido web para mostrar en Managed Browser** | Pulse **Sí** para aplicar los vínculos web en la aplicación que se va a abrir en la aplicación Managed Browser. <br><br> En el caso de los dispositivos que no estén inscritos en Intune, los vínculos web en aplicaciones administradas por directivas solo se pueden abrir en la aplicación Managed Browser. <br><br> Si usa Intune para administrar los dispositivos, vea [Administrar el acceso a Internet mediante directivas de explorador administrado con Microsoft Intune](manage-internet-access-using-managed-browser-policies.md). | No |
| **Cifrar datos de aplicación** | Pulse **Sí** para habilitar el cifrado de datos profesionales o educativos en esta aplicación. Intune usa un esquema de cifrado AES de 128 bits de OpenSSL junto con el sistema del almacén de claves Android para cifrar los datos de la aplicación de manera segura. Los datos se cifran de forma sincrónica durante las tareas de E/S de archivo. El contenido del almacenamiento del dispositivo estará siempre cifrado. <br><br> El método de cifrado **no** está certificado mediante FIPS 140-2.  | Sí |
| **Deshabilitar la sincronización de contactos** | Pulse **Sí** para impedir que la aplicación guarde datos en la aplicación nativa Contactos del dispositivo. Si pulsa **No**, la aplicación puede guardar datos en la aplicación Contactos nativa del dispositivo. <br><br>Cuando realiza un borrado selectivo para quitar los datos profesionales o educativos de la aplicación, se quitan los contactos sincronizados directamente desde la aplicación a la aplicación nativa Contactos. No se pueden borrar los contactos sincronizados desde la libreta de direcciones nativa en otro origen externo. Actualmente esto se aplica únicamente para la aplicación Microsoft Outlook. | No |
| **Deshabilitar la impresión** | Pulse **Sí** para impedir que la aplicación imprima datos profesionales o educativos. | No |

  >[!NOTE]
  >El método de cifrado de la opción de configuración **Cifrar datos de aplicación** **no** está certificado mediante FIPS 140-2.


  ## <a name="data-transfer-exemptions"></a>Exenciones de transferencia de datos

  La directiva de protección de aplicaciones de Intune puede permitir la transferencia de datos desde y hacia algunas aplicaciones y servicios de plataforma. Por ejemplo, todas las aplicaciones habilitadas para Intune en Android deben poder transferir datos desde y hacia la función Texto a voz de Google, de forma que se pueda leer en voz alta el texto que aparezca en la pantalla del dispositivo móvil. Esta lista está sujeta a cambios y refleja los servicios y las aplicaciones que se consideran útiles para una productividad segura.

  ### <a name="full-exemptions"></a>Exenciones completas

  En estas aplicaciones y servicios se permite totalmente la transferencia de datos desde y hacia aplicaciones administradas por Intune.

  |Nombre de aplicación/servicio | Descripción |
  | ------ | ---- |
  | com.android.phone | Aplicación de teléfono nativa
  | com.android.vending | Google Play Store |
  | com.android.documentsui | Selector de documentos de Android|
  | com.google.android.webview | [WebView](https://developer.android.com/reference/android/webkit/WebView.html), necesario para muchas aplicaciones, incluido Outlook |
  | com.android.webview |[WebView](https://developer.android.com/reference/android/webkit/WebView.html), necesario para muchas aplicaciones, incluido Outlook|
  | com.google.android.tts | Texto a voz de Google |
  | com.android.providers.settings | Configuración del sistema Android |
  | com.azure.authenticator | Aplicación Azure Authenticator, necesaria para una autenticación correcta en muchos escenarios |
  | com.microsoft.windowsintune.companyportal | Intune Portal de empresa|

  ### <a name="conditional-exemptions"></a>Exenciones condicionales
  En estas aplicaciones y servicios solo se permite la transferencia de datos desde y hacia aplicaciones administradas por Intune en determinadas condiciones.

  |Nombre de aplicación/servicio | Descripción | Condición de exención|
  | ------ | ---- | --- |
  | com.android.chrome | Explorador Google Chrome | Chrome se utiliza para algunos componentes de WebView en Android 7.0 y versiones posteriores, y nunca está oculto. No obstante, el flujo de datos desde y hacia la aplicación siempre está restringido.
  | com.skype.raider | Skype | La aplicación Skype solo se permite para determinadas acciones que dan lugar a una llamada telefónica. |
  | com.android.providers.media | Proveedor de contenido multimedia de Android | El proveedor de contenido multimedia solo se permite para la selección de tono. |
  | com.google.android.gms; com.google.android.gsf | Paquetes de Servicios de Google Play | Estos paquetes se permiten para acciones de Google Cloud Messaging, como las notificaciones de inserción. |



##  <a name="access-settings"></a>Configuración de acceso

| Configuración | Cómo se usa | Valores predeterminados |
|------|------|------|
| **Requerir PIN para acceder** | Pulse **Sí** para requerir un PIN para usar esta aplicación. Se pedirá al usuario que configure este PIN la primera vez que ejecute la aplicación en un contexto profesional o educativo. Valor predeterminado = **Sí**.<br><br> Configure las siguientes opciones para la intensidad del PIN: <ul><li>**Número de intentos antes del restablecimiento del PIN**: especifique el número de veces que el usuario tiene que escribir correctamente el PIN antes de que deba restablecerlo. Valor predeterminado = **5**.</li><li> **Permitir el PIN simple**: pulse **Sí** para permitir que los usuarios usen secuencias de PIN simples como 1234 o 1111. Pulse **No** para impedir que usen secuencias simples. Valor predeterminado = **Sí**. </li><li> **Longitud del PIN**: especifique el número mínimo de dígitos en una secuencia de PIN. Valor predeterminado = **4**. </li><li> **Permitir desbloqueo mediante huellas digitales en lugar de mediante PIN (Android 6.0+)**: pulse **Sí** para permitir que el usuario use la [autenticación con huella digital](https://developer.android.com/about/versions/marshmallow/android-6.0.html#fingerprint-authentication) en lugar de un PIN para el acceso a la aplicación. Valor predeterminado = **Sí**.</li></ul> En dispositivos Android, puede permitir que el usuario demuestre su identidad con la [autenticación con huella digital de Android](https://developer.android.com/about/versions/marshmallow/android-6.0.html#fingerprint-authentication) en lugar de usar un PIN. Cuando el usuario intenta usar esta aplicación con su cuenta profesional o educativa, se le solicita que indique su identidad mediante huella digital en lugar de escribir un PIN. </li></ul>| Requerir PIN: Sí <br><br> Intentos de restablecimiento del PIN: 5 <br><br> Permitir PIN simple: Sí <br><br> Longitud del PIN: 4 <br><br> Permitir huella digital: Sí |
| **Requerir credenciales corporativas en acceso** | Pulse **Sí** para requerir que el usuario inicie sesión con su cuenta profesional o educativa en lugar de escribir un PIN para el acceso a la aplicación. Si se establece en **Sí**, se reemplazarán los requisitos de introducción de un PIN o un Touch ID.  | No |
| **Bloquear la ejecución de aplicaciones administradas en dispositivos descodificados o descifrados** |Pulse **Sí** para impedir que esta aplicación se ejecute en dispositivos descodificados o descifrados. El usuario seguirá siendo capaz de usar esta aplicación para las tareas personales, pero tendrá que usar un dispositivo distinto para tener acceso a los datos profesionales o educativos de esta aplicación. | Sí |
| **Volver a comprobar los requisitos de acceso después de (minutos)** | Configure las siguientes opciones: <ul><li>**Tiempo de espera**: es el número de minutos antes de que se vuelvan a comprobar los requisitos de acceso (definidos anteriormente en la directiva). Por ejemplo, un administrador activa el PIN en la directiva, un usuario abre una aplicación MAM y debe escribir un PIN. Cuando se usa esta opción, el usuario no tendría que escribir un PIN en ninguna aplicación MAM durante **30 minutos** (valor predeterminado).</li><li>**Período de gracia sin conexión**: es el número de minutos que las aplicaciones MAM pueden ejecutarse sin conexión, especifique el tiempo (en minutos) que debe transcurrir antes de que se vuelvan a comprobar los requisitos de acceso de la aplicación. Valor predeterminado = **720** minutos (12 horas). Una vez transcurrido este período, la aplicación requerirá la autenticación de usuario en AAD para poder seguir ejecutándose.</li></ul>| Tiempo de espera: 30 <br><br> Sin conexión: 720 |
| **Intervalo sin conexión antes de que se borren los datos de la aplicación (días)** | Después de este número de días (definido por el administrador) de ejecución sin conexión, la propia aplicación realizará un borrado selectivo. Este borrado selectivo es el mismo que el que puede iniciar el administrador en el flujo de trabajo de borrado MAM. <br><br> | 90 días |
| **Bloquear captura de pantalla y Asistente para Android (Android 6.0+)** | Pulse **Sí** para bloquear las características de captura de pantalla y **Asistente para Android** del dispositivo cuando se usa esta aplicación. Al pulsar **Sí** también se desenfocará la imagen de vista previa de las últimas aplicaciones si se usa esta aplicación con una cuenta profesional o educativa. | No |
| **Deshabilitar el PIN de aplicación cuando se administra el PIN del dispositivo** | Elija **Sí** para deshabilitar el PIN de aplicación cuando se detecta un bloqueo de dispositivo en un dispositivo inscrito. | No |

