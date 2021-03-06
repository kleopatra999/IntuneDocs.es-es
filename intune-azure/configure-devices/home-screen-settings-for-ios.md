---
title: "Configuración de diseño de pantalla principal de Intune para dispositivos iOS"
titleSuffix: Intune Azure preview
description: "Versión preliminar de Azure de Intune: conozca la configuración que puede usar para personalizar la pantalla principal y la base de los dispositivos iOS."
keywords: 
author: robstackmsft
ms.author: robstack
manager: angrobe
ms.date: 4/12/2017
ms.topic: article
ms.prod: 
ms.service: microsoft-intune
ms.technology: 
ms.assetid: 6aba4491-afb9-43cd-9ccc-14e6a2a5a3b1
ms.reviewer: karanda
ms.suite: ems
ms.custom: intune-azure
translationtype: Human Translation
ms.sourcegitcommit: e5dd7cb5b320df7f443b52a1b502027fa3c4acaf
ms.openlocfilehash: 72bfde93389a060ed52062be0f2692b8bc35543a
ms.lasthandoff: 04/19/2017


---

# <a name="intune-home-screen-layout-settings-for-ios-devices"></a>Configuración de diseño de pantalla principal de Intune para dispositivos iOS

[!INCLUDE[azure_preview](../includes/azure_preview.md)]

Use estos valores para configurar el diseño de aplicaciones, carpetas e imágenes web en la base y la pantalla principal de todos los dispositivos iOS a los que asigna la directiva.

iOS devices to which you assign the profile must be in supervised mode and running iOS 9.3 or later.

1. En la hoja **Características del dispositivo**, elija **Diseño de pantalla principal (solo supervisado)**.
2. En la hoja **Diseño de pantalla principal (solo supervisado**, elija si desea configurar los diseños de **Base** o **Páginas**.

## <a name="add-items-to-the-dock"></a>Agregar elementos a la base

En la hoja **Base**, puede agregar hasta 6 elementos o carpetas a la base que se encuentra en la parte inferior de la pantalla iOS. Sin embargo, muchos dispositivos admiten menos elementos; por ejemplo, los dispositivos iPhone admiten hasta 4 elementos. En este caso, en el dispositivo se mostrarán solo los primeros cuatro elementos que configuró.

1. Elija **Agregar** para agregar un elemento a la base.
2. En la hoja **Agregar fila**, elija si desea agregar una **aplicación** o una **carpeta**.
3. Use la información que se encuentra en las secciones **Cómo agregar una aplicación a la lista** y **Cómo agregar una carpeta a la lista** de este tema para configurar las aplicaciones y carpetas que desea que aparezcan en la base.
4. Siga agregando elementos. Cuando termine, haga clic en **Aceptar** en cada hoja hasta que vuelva a la hoja **Crear perfil**. Elija **Crear**.

>[!TIP]
> Puede arrastrar y soltar elementos en cualquier lista de las páginas de la pantalla principal para reordenarlos. 

### <a name="example"></a>Ejemplo

En este ejemplo, se configuró la pantalla de la base para mostrar solo las aplicaciones Safari, Correo y Acciones. En la imagen siguiente, se selecciona la aplicación Correo para mostrar sus propiedades:

![Configuración de base de iOS de ejemplo](http://i.imgur.com/FfFiUcP.png)

Cuando asigna la directiva a un dispositivo iPhone, el resultado será una base similar a la siguiente:

![Diseño de base de iOS de ejemplo en iPhone](http://i.imgur.com/bAgCe8F.png)

## <a name="add-home-screen-pages"></a>Agregar páginas de pantalla principal

Agregue las páginas que desee que aparezcan en la pantalla principal y las aplicaciones que aparecerán en cada página. Las aplicaciones que agrega a una página se organizan de izquierda a derecha, según el orden especificado en la lista. Si agrega más aplicaciones que las que caben en una página, se moverán a una página subsiguiente.


1. En la hoja **Páginas**, elija **Agregar**.
2. En la hoja **Agregar fila**, escriba un **Nombre de página**. Este se usa como referencia en el portal de Intune y *no se muestra* en el dispositivo iOS.
3. Elija **Agregar** y, luego, elija si desea agregar una **aplicación** o una **carpeta** a la página.
4. Use la información que se encuentra en las secciones **Cómo agregar una aplicación a la lista** y **Cómo agregar una carpeta a la lista** de este tema para configurar las aplicaciones y carpetas que desea que aparezcan en la página.

### <a name="example"></a>Ejemplo

En este ejemplo, configuró una página nueva llamada **Contoso**. En esta página solo se muestran las aplicaciones Buscar amigos y Configuración. En la imagen siguiente, se selecciona la aplicación Configuración para mostrar sus propiedades:

![Ejemplo de configuración de pantalla principal de iOS](http://i.imgur.com/Jc2OxyX.png)

Cuando asigna la directiva a un dispositivo iPhone, el resultado será una página similar a la siguiente:

![Dispositivo iOS con la pantalla principal modificada](http://i.imgur.com/Bd37PHa.png)

## <a name="how-to-add-an-app-to-the-list"></a>Cómo agregar una aplicación a la lista

1. Escriba el **nombre de la aplicación**. Este se usa como referencia en el portal de Intune y *no se muestra* en el dispositivo iOS.
2. Escriba el **Identificador del lote de aplicaciones** de la aplicación que quiere mostrar. Consulte **Bundle ID reference for built-in iOS apps** (Referencia de identificador de lote para aplicaciones iOS integrada) más adelante en este tema para obtener ayuda.
3. Haga clic en **Aceptar** y, luego, siga agregando hasta un máximo de **6** elementos en la base del dispositivo y **60** para una página del dispositivo.
4. Cuando haya terminado, haga clic en **Aceptar**.

## <a name="how-to-add-a-folder-to-the-list"></a>Cómo agregar una carpeta a la lista

Las aplicaciones que agrega a una página en una carpeta se organizan de izquierda a derecha, según el orden especificado en la lista. Si agrega más aplicaciones que las que caben en una página, se moverán a una página subsiguiente.

1. Escriba el **nombre de la carpeta**. Este aparecerá en el dispositivo de los usuarios.
2. Elija **Agregar** para crear una página en la carpeta. Puede agregar hasta 20 páginas.
3. En la hoja **Agregar fila**, escriba un nombre para la página. Este se usa como referencia en el portal de Intune y *no se muestra* en el dispositivo iOS.
3. Escriba el **nombre de la aplicación**. Este se usa como referencia en el portal de Intune y *no se muestra* en el dispositivo iOS.
2. Escriba el **Identificador del lote de aplicaciones** de la aplicación que quiere mostrar. Consulte **Cómo agregar una aplicación a la lista** para obtener ayuda.
3. Seleccione **Agregar**. Puede agregar hasta 60 elementos.
4. Cuando haya terminado, haga clic en **Aceptar**.


## <a name="bundle-id-reference-for-built-in-ios-apps"></a>Referencia de identificador de lote para aplicaciones iOS integradas

En esta lista se muestra el identificador de lote de algunas aplicaciones iOS comunes integradas. Póngase en contacto con el proveedor de software para encontrar el identificador de lote de otras aplicaciones. 

|||
|-|-|
|Nombre de la aplicación|Identificador de lote|
|Tienda de aplicaciones|com.apple.AppStore|
|Calculadora|com.apple.calculator|
|Calendario|com.apple.mobilecal|
|Cámara|com.apple.camera|
|Reloj|com.apple.mobiletimer|
|Brújula|com.apple.compass|
|Contactos|com.apple.MobileAddressBook|
|FaceTime|com.apple.facetime|
|Buscar amigos|com.apple.mobileme.fmf1|
|Buscar mi iPhone|com.apple.mobileme.fmip1|
|Centro de juegos|com.apple.gamecenter|
|GarageBand|com.apple.mobilegarageband|
|Mantenimiento|com.apple.Health|
|iBooks|com.apple.iBooks|
|iTunes Store|com.apple.MobileStore|
|iTunes U|com.apple.itunesu|
|Keynote|com.apple.Keynote|
|Mail|com.apple.mobilemail|
|Asignaciones|com.apple.Maps|
|Mensajes|com.apple.MobileSMS|
|Música|com.apple.Music|
|Noticias|com.apple.news|
|Notas|com.apple.mobilenotes|
|Números|com.apple.Numbers|
|Páginas|com.apple.Pages|
|Photo Booth|com.apple.Photo-Booth|
|Fotos|com.apple.mobileslideshow|
|Podcasts|com.apple.podcasts|
|Recordatorios|com.apple.reminders|
|Safari|com.apple.mobilesafari|
|Configuración|com.apple.Preferences|
|Acciones|com.apple.stocks|
|Sugerencias|com.apple.tips|
|Vídeos|com.apple.videos|
|VoiceMemos|com.apple.VoiceMemos|
|Wallet|com.apple.Passbook|
|Inspección|com.apple.Bridge|
|Clima|com.apple.weather|


