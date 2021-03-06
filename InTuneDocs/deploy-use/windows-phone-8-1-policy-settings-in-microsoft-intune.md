---
title: "Configuración de directivas de Windows Phone 8.1 | Microsoft Docs"
description: "Intune proporciona una variedad de opciones generales integradas que puede configurar en los dispositivos Windows Phone 8.1. Además, puede especificar valores OMA-URI para crear una configuración personalizada que no esté disponible en Intune."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 10/11/2016
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 83f7469c-272e-43f2-8139-b0d7bc34f43f
ms.reviewer: heenamac
ms.suite: ems
ms.custom: intune-classic
translationtype: Human Translation
ms.sourcegitcommit: ab6d9b6b296fb4e1fb0aaa9496fede28976728dc
ms.openlocfilehash: 65d3b454531084008bdbb01dd17f5ce34ef5890f
ms.lasthandoff: 04/14/2017


---

# <a name="windows-phone-81-policy-settings-in-microsoft-intune"></a>Configuración de directivas de Windows 8.1 en Microsoft Intune

[!INCLUDE[classic-portal](../includes/classic-portal.md)]

Intune proporciona una variedad de opciones generales integradas que puede configurar en los dispositivos Windows Phone 8.1. Además, puede especificar valores Open Mobile Alliance Uniform Resource Identifier (OMA-URI, identificador uniforme de recursos de Open Mobile Alliance) para crear una configuración personalizada que no esté disponible en Intune.

## <a name="general-configuration-settings"></a>Opciones generales de configuración

Use la **directiva de configuración general de Windows Phone (Windows Phone 8.1 y posterior)** de Microsoft Intune para configurar las opciones siguientes para dispositivos Windows Phone 8.1:

-   **Configuración de seguridad de dispositivos móviles** : elija entre una lista de configuraciones predefinidas que permiten controlar una variedad de características y la funcionalidad en el dispositivo.

-   **Aplicaciones compatibles y no compatibles**: especifique una lista de las aplicaciones compatibles y no compatibles de su compañía. Los dispositivos Windows Phone pueden bloquear o permitir la instalación de estas aplicaciones.

### <a name="applicability-settings"></a>Configuración de aplicabilidad

|Nombre de la configuración|Detalles|
|----------------|----------------------------------|
|**Aplicar todas las configuraciones a Windows 10**|Permite aplicar la configuración de esta directiva en dispositivos Windows 10 Mobile y en dispositivos Windows Phone 8.1.|

### <a name="password-settings"></a>Configuración de contraseña

|Nombre de la configuración|Detalles|
|----------------|------|
|**Requerir una contraseña para desbloquear dispositivos móviles**|Especifica si los usuarios deben escribir una contraseña para obtener acceso a los dispositivos.|
|**Tipo de contraseña obligatoria**|Especifica el tipo de contraseña que será necesario, como solo numérica o alfanumérica.|
|**Tipo de contraseña requerida: número mínimo de conjuntos de caracteres**|Especifica cuántos juegos de caracteres diferentes deben incluirse en la contraseña. Hay cuatro juegos de caracteres: letras minúsculas, letras mayúsculas, símbolos y números. En cambio, para dispositivos iOS, especifica el número de símbolos que deben incluirse en la contraseña.|
|**Longitud mínima de contraseña**|Especifica el número mínimo de caracteres que son necesarios en la contraseña.|
|**Permitir contraseñas sencillas**|Especifica que pueden usarse contraseñas sencillas como "0000" y "1234".|
|**Número de errores de inicio de sesión repetidos que se permiten antes de que se borre el dispositivo**|Especifica el número de veces que se puede escribir una contraseña incorrecta antes de que se borre el dispositivo.|
|**Minutos de inactividad antes de que se apague la pantalla**|Especifica la cantidad de tiempo que un dispositivo debe permanecer inactivo antes de que se bloquee automáticamente la pantalla.|
|**Expiración de contraseña (días)**|Especifica el número de días antes de que se deba cambiar la contraseña del dispositivo.|Sí|Sí|
|**Recordar el historial de contraseñas**|Especifica si se recuerdan las contraseñas usadas anteriormente para impedir que el usuario vuelva a usarlas.|
|**Recordar historial de la contraseña** : **Impedir la reutilización de contraseñas anteriores**|Especifica cuántas contraseñas usadas anteriormente se recuerdan.|

### <a name="encryption-settings"></a>Configuración de cifrado

|Nombre de la configuración|Detalles|
|----------------|------|
|**Requerir cifrado en dispositivo móvil**|Requiere que se cifren los datos en los dispositivos móviles compatibles.|

### <a name="system-settings"></a>Configuración del sistema

|Nombre de la configuración|Detalles|
|----------------|-----|
|**Permitir captura de pantalla**|Permite al usuario capturar el contenido de la pantalla como un archivo de imagen.|
|**Permitir el envío de datos de diagnóstico**|Permite que el dispositivo envíe información de diagnóstico a Microsoft.|

### <a name="cloud-settings--accounts-and-synchronization"></a>Configuración de nube: cuentas y sincronización

|Nombre de la configuración|Detalles|
|----------------|------|
|**Permitir cuenta de Microsoft**|Permite vincular una cuenta Microsoft al dispositivo.|

### <a name="email-settings"></a>Configuración de correo electrónico

|Nombre de la configuración|Detalles|
|----------------|-----|
|**Permitir cuentas de correo electrónico personalizadas**|Permite que el dispositivo se conecte a cuentas de correo electrónico que no son de Microsoft.|

### <a name="application-settings---browser"></a>Configuración de la aplicación: explorador

|Nombre de la configuración|Detalles|
|----------------|-----|
|**Permitir explorador web**|Permite o bloquea el explorador web integrado en los dispositivos.|

### <a name="application-settings---apps"></a>Configuración de la aplicación: aplicaciones

|Nombre de la configuración|Detalles|
|----------------|-----|
|**Permitir almacén de aplicaciones**|Permite a los usuarios conectarse a la tienda de aplicaciones desde el dispositivo.|

### <a name="device-capabilities-settings---hardware"></a>Configuración de funcionalidades del dispositivo: hardware

|Nombre de la configuración|Detalles|
|----------------|-----|
|**Permitir cámara**|Permite o bloquea la cámara del dispositivo.|
|**Permitir almacenamiento extraíble**|Permite que el dispositivo use un almacenamiento extraíble, como las tarjetas SD.|
|**Permitir Wi-Fi**|Habilita o deshabilita la funcionalidad de Wi-Fi del dispositivo.|
|**Permitir Wi-Fi Tethering**|Permite el uso de Tethering Wi-Fi en el dispositivo.|
|**Permitir la conexión automática a zonas Wi-Fi gratuitas**|Permite que el dispositivo se conecte automáticamente a zonas Wi-Fi gratuitas y acepte automáticamente las condiciones de uso.|
|**Permitir informar de zonas Wi-Fi**|Envía información sobre las conexiones Wi-Fi para ayudar al usuario a detectar conexiones cercanas.|
|**Permitir geolocalización**|Permite que el dispositivo use información de ubicación.|
|**Permitir NFC**|Permite las operaciones que usan la transmisión de datos en proximidad.|
|**Permitir Bluetooth**|Habilita o deshabilita la funcionalidad de Bluetooth del dispositivo.|

### <a name="device-capabilities-settings---features"></a>Configuración de funcionalidades del dispositivo: características

|Nombre de la configuración|Detalles|
|----------------|----|
|**Permitir copiar y pegar**|Permite la funcionalidad de copiar y pegar en los dispositivos.|

### <a name="settings-for-allowed-and-blocked-apps"></a>Configuración de aplicaciones permitidas y bloqueadas
En la lista **Aplicaciones permitidas y bloqueadas**, especifique una lista de aplicaciones que quiera permitir o bloquear mediante la siguiente información:

> [!NOTE]
> Una sola directiva únicamente puede contener una lista de aplicaciones permitidas o bloqueadas. No se pueden especificar ambas en la misma directiva.

|Nombre de la configuración|Detalles|
|----------------|--------------------|
|**Bloquear dispositivos para que no abran las aplicaciones de la lista**|Enumera las aplicaciones que no se administran mediante Intune y que los usuarios no pueden instalar ni ejecutar.|
|**Permitir que los dispositivos instalen solo las aplicaciones de la lista**|Enumera las aplicaciones que los usuarios pueden instalar. Los usuarios no pueden instalar ninguna otra aplicación. Las aplicaciones que se administran mediante Intune están permitidas automáticamente.|
|**Agregar**|Agrega una aplicación a la lista seleccionada. Especifique un nombre de su elección, la dirección URL de la aplicación en la tienda de aplicaciones y el publicador de la aplicación (opcional). Consulte Cómo especificar las direcciones URL de tiendas de aplicaciones más adelante en este tema para obtener más ayuda.
|**Importar aplicaciones**|Importa la lista de las aplicaciones que ha especificado en un archivo de valores separados por comas. Utilice el formato, nombre de la aplicación, editor, dirección URL de la aplicación en el archivo.|
|**Editarar**|Permite editar el nombre, el editor y la dirección URL de la aplicación seleccionada.|
|**Eliminar**|Elimina la aplicación seleccionada de la lista.|
> [!IMPORTANT]
> Si especifica una lista de aplicaciones permitidas para dispositivos de Windows Phone 8.1, debe agregar la aplicación Portal de empresa a esta lista o se bloqueará.


### <a name="reference-information-for-allowed-and-blocked-apps"></a>Información de referencia para aplicaciones permitidas y bloqueadas

#### <a name="how-to-specify-urls-to-app-stores"></a>Cómo especificar las direcciones URL de tiendas de aplicaciones
Para especificar la dirección URL de una aplicación en la lista de aplicaciones permitidas y bloqueadas, use el siguiente formato:

Desde la página de [aplicaciones y juegos para Windows Phone](http://www.windowsphone.com/store/overview), busque la aplicación que quiere usar.

Abra la página de la aplicación y copie la dirección URL en el Portapapeles. Ya puede usarla como dirección URL en una la lista de aplicaciones permitidas o bloqueadas.

**Ejemplo:** Busque la aplicación Skype en la Tienda. La dirección URL que use será **http://www.windowsphone.com/es-es/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51**.

## <a name="custom-policy-settings"></a>Configuración de directivas personalizadas
Use la **directiva de configuración personalizada de Windows Phone** de Microsoft Intune para implementar las opciones de configuración de OMA-URI, que pueden usarse para controlar características en **dispositivos Windows Phone 8.1**. Se trata de una configuración estándar que muchos fabricantes de dispositivos móviles usan para controlar las características del dispositivo.

Esta funcionalidad le permite implementar la configuración de Windows Phone que no se puede configurar con una directiva de configuración general de Intune. Para obtener más información sobre las opciones que se pueden configurar con estas directivas, vea [Administrar la configuración y las características de los dispositivos con directivas de Microsoft Intune](manage-settings-and-features-on-your-devices-with-microsoft-intune-policies.md).

Para obtener ayuda acerca de cómo crear la configuración de OMA-URI para dispositivos Windows Phone, consulte [Windows Phone 8.1 MDM protocol documentation](http://technet.microsoft.com/library/dn499787.aspx).

### <a name="general-settings"></a>Configuración general

|Nombre de la configuración|Detalles|
|----------------|--------------------|
|**Nombre**|Escriba un nombre único para la directiva que le ayude a identificarla en la consola de Intune.|
|**Descripción**|Proporcione una descripción general de la directiva y otra información relevante que le ayude a encontrarla.|

### <a name="oma-uri-settings"></a>Configuración de OMA-URI

En la sección **Configuración OMA-URI**, haga clic en **Agregar** para agregar un valor. También puede editar o eliminar un valor existente.

En el cuadro de diálogo **Agregar o editar configuración OMA-URI**, especifique la siguiente información:

|Nombre de la configuración|Detalles|
    |--------|--------------------|
    |**Nombre de la configuración**|Escriba un nombre único para el valor OMA-URI que le ayude a identificarlo en la lista de valores de configuración.|
    |**Descripción del valor**|Proporcione una descripción que ofrezca una visión general del valor y otra información relevante que le ayude a encontrarlo.|
    |**Tipo de datos**|Seleccione el tipo de fecha en que especificará este valor OMA-URI. Elija de entre las siguientes opciones:<br /><br />-   **Cadena**<br />-   **Cadena (XML)**<br />-   **Fecha y hora**<br />-   **Entero**<br />-   **Punto flotante**<br />-   **Booleano**|
    |**OMA-URI (distingue mayúsculas de minúsculas)**|Especifique el OMA-URI para el que quiere proporcionar un valor.|
    |**Valor**|Especifique el valor asociado con el OMA-URI especificado anteriormente.|

### <a name="see-also"></a>Consulte también
[Administrar la configuración y las características de los dispositivos con directivas de Microsoft Intune](manage-settings-and-features-on-your-devices-with-microsoft-intune-policies.md)

