---
# required metadata

title: Requisitos de la infraestructura de red | Microsoft Intune
description:
keywords:
author: Staciebarker
manager: jeffgilb
ms.date: 04/28/2016
ms.topic: get-started-article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 074de65b-84a5-4a01-a824-18ffd838eab0

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: jeffgilb
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Requisitos de la infraestructura de red para Microsoft Intune
Antes de configurar Microsoft Intune, repase este tema y los requisitos que aparecen en [What to know before you start Microsoft Intune](what-to-know-before-you-start-microsoft-intune.md) (Información necesaria antes de iniciar Microsoft Intune)..

En este tema se incluyen los requisitos que permiten que la infraestructura de red apruebe las comunicaciones entre los dispositivos que usted administra y usa para administrar la suscripción de Intune y los sitios web de Internet que usa el servicio basado en la nube.

No se requiere el uso de una infraestructura local (como un servidor donde se deba instalar el software) pero hay opciones para utilizar la infraestructura local, incluidas las herramientas de sincronización de Active Directory y Exchange.

Para administrar los equipos que están detrás de firewalls y servidores proxy, debe configurar los firewalls y los servidores proxy de modo que permitan las comunicaciones de Intune.

## Requisitos de los firewalls, puertos y dominios
Los dispositivos administrados requieren configuraciones que dejen acceder a **Todos los usuarios** a diversos servicios a través de firewalls.

En la tabla siguiente se enumeran los puertos y los servicios a los que accede el cliente de Intune.


|**Dominio**|**Puertos**|**Dirección IP**|
|------|----|
|manage.microsoft.com<br>a.manage.microsoft.com<br>admin.manage.microsoft.com<br>enterpriseenrollment.manage.microsoft.com<br>enterpriseenrollment-s.manage.microsoft.com<br>i.manage.microsoft.com<br>m.manage.microsoft.com<br>p.manage.microsoft.com<br>portal.manage.microsoft.com<br>r.manage.microsoft.com|80 y 443|134.170.168.254<br>134.170.51.126
|account.manage.microsoft.com|80 y 443|157.56.13.59
|fef.msua01.manage.microsoft.com|80 y 443|138.91.243.97
|fef.msua02.manage.microsoft.com|80 y 443|23.96.112.46
|fef.msua04.manage.microsoft.com|80 y 443|23.96.112.28
|fef.msua05.manage.microsoft.com|80 y 443|138.91.244.151
|fef.msub01.manage.microsoft.com|80 y 443|137.135.128.214
|fef.msub02.manage.microsoft.com|80 y 443|137.135.130.29
|fef.msub03.manage.microsoft.com|80 y 443|23.97.165.17
|fef.msub05.manage.microsoft.com|80 y 443|23.97.166.52
|fef.msuc01.manage.microsoft.com|80 y 443|207.46.225.1
|fef.msuc02.manage.microsoft.com|80 y 443|23.98.66.118
|fef.msuc03.manage.microsoft.com|80 y 443|23.101.0.100
|fef.msuc05.manage.microsoft.com|80 y 443|207.46.154.33
|fef.msua06.manage.microsoft.com|80 y 443|104.42.188.1
|fei.msua01.manage.microsoft.com|80 y 443|138.91.240.131
|fei.msua02.manage.microsoft.com|80 y 443|23.96.112.143
|fei.msua04.manage.microsoft.com|80 y 443|23.96.112.147
|fei.msua05.manage.microsoft.com|80 y 443|138.91.240.163
|fei.msub01.manage.microsoft.com|80 y 443|137.135.130.85
|fei.msub02.manage.microsoft.com|80 y 443|137.135.132.149
|fei.msub03.manage.microsoft.com|80 y 443|23.97.160.232
|fei.msub05.manage.microsoft.com|80 y 443|23.97.162.250
|fei.msuc01.manage.microsoft.com|80 y 443|207.46.224.73
|fei.msuc02.manage.microsoft.com|80 y 443|23.98.66.194
|fei.msuc03.manage.microsoft.com|80 y 443|23.101.2.105
|fei.msuc05.manage.microsoft.com|80 y 443|207.46.147.126
|fei.msua06.manage.microsoft.com|80 y 443|138.91.149.190
|m.fei.msua01.manage.microsoft.com|80 y 443|138.91.240.131
|m.fei.msua02.manage.microsoft.com|80 y 443|23.96.112.143
|m.fei.msua04.manage.microsoft.com|80 y 443|23.96.112.147
|m.fei.msua05.manage.microsoft.com|80 y 443|138.91.240.163
|m.fei.msub01.manage.microsoft.com|80 y 443|137.135.130.85
|m.fei.msub02.manage.microsoft.com|80 y 443|137.135.132.149
|m.fei.msub03.manage.microsoft.com|80 y 443|23.97.160.232
|m.fei.msub05.manage.microsoft.com|80 y 443|23.97.162.250
|m.fei.msuc01.manage.microsoft.com|80 y 443|207.46.224.73
|m.fei.msuc02.manage.microsoft.com|80 y 443|23.98.66.194
|m.fei.msuc03.manage.microsoft.com|80 y 443|23.101.2.105
|m.fei.msuc05.manage.microsoft.com|80 y 443|207.46.147.126
|m.fei.msua06.manage.microsoft.com|80 y 443|138.91.149.190
|m.msua01.manage.microsoft.com|80 y 443|157.55.50.182
|m.msua02.manage.microsoft.com|80 y 443|134.170.49.121
|m.msua04.manage.microsoft.com|80 y 443|134.170.49.126
|m.msua05.manage.microsoft.com|80 y 443|157.55.240.190
|m.msua06.manage.microsoft.com|80 y 443|134.170.49.114
|m.msub01.manage.microsoft.com|80 y 443|94.245.121.50
|m.msub02.manage.microsoft.com|80 y 443|94.245.121.58
|m.msub03.manage.microsoft.com|80 y 443|94.245.121.56
|m.msub05.manage.microsoft.com|80 y 443|157.56.113.123
|m.msuc01.manage.microsoft.com|80 y 443|104.44.84.187
|m.msuc02.manage.microsoft.com|80 y 443|104.44.84.188
|m.msuc03.manage.microsoft.com|80 y 443|104.44.84.189
|m.msuc05.manage.microsoft.com|80 y 443|111.221.76.60
|msua01.manage.microsoft.com|80 y 443|157.55.50.182
|msua02.manage.microsoft.com|80 y 443|134.170.49.121
|msua04.manage.microsoft.com|80 y 443|134.170.49.126
|msua05.manage.microsoft.com|80 y 443|157.55.240.190
|msub01.manage.microsoft.com|80 y 443|94.245.121.50
|msub02.manage.microsoft.com|80 y 443|94.245.121.58
|msub03.manage.microsoft.com|80 y 443|94.245.121.56
|msub05.manage.microsoft.com|80 y 443|157.56.113.123
|msuc01.manage.microsoft.com|80 y 443|104.44.84.187
|msuc02.manage.microsoft.com|80 y 443|104.44.84.188
|msuc03.manage.microsoft.com|80 y 443|104.44.84.189
|msuc05.manage.microsoft.com|80 y 443|111.221.76.60
|msua06.manage.microsoft.com|80 y 443|134.170.49.114
|ncufun.account.manage.microsoft.com|80 y 443|157.55.252.224
|neufun.account.manage.microsoft.com|80 y 443|65.52.229.134
|portal.fei.msua01.manage.microsoft.com|80 y 443|138.91.240.131
|portal.fei.msua02.manage.microsoft.com|80 y 443|23.96.112.143
|portal.fei.msua04.manage.microsoft.com|80 y 443|23.96.112.147
|portal.fei.msua05.manage.microsoft.com|80 y 443|138.91.240.163
|portal.fei.msub01.manage.microsoft.com|80 y 443|137.135.130.85
|portal.fei.msub02.manage.microsoft.com|80 y 443|137.135.132.149
|portal.fei.msub03.manage.microsoft.com|80 y 443|23.97.160.232
|portal.fei.msub05.manage.microsoft.com|80 y 443|23.97.162.250
|portal.fei.msuc01.manage.microsoft.com|80 y 443|207.46.224.73
|portal.fei.msuc02.manage.microsoft.com|80 y 443|23.98.66.194
|portal.fei.msuc03.manage.microsoft.com|80 y 443|23.101.2.105
|portal.fei.msuc05.manage.microsoft.com|80 y 443|207.46.147.126
|portal.fei.msua06.manage.microsoft.com|80 y 443|138.91.149.190
|portal.msua01.manage.microsoft.com|80 y 443|157.55.50.182
|portal.msua02.manage.microsoft.com|80 y 443|134.170.49.121
|portal.msua04.manage.microsoft.com|80 y 443|134.170.49.126
|portal.msua05.manage.microsoft.com|80 y 443|157.55.240.190
|portal.msub01.manage.microsoft.com|80 y 443|94.245.121.50
|portal.msub02.manage.microsoft.com|80 y 443|94.245.121.58
|portal.msub03.manage.microsoft.com|80 y 443|94.245.121.56
|portal.msub05.manage.microsoft.com|80 y 443|157.56.113.123
|portal.msuc01.manage.microsoft.com|80 y 443|104.44.84.187
|portal.msuc02.manage.microsoft.com|80 y 443|104.44.84.188
|portal.msuc03.manage.microsoft.com|80 y 443|104.44.84.189
|portal.msuc05.manage.microsoft.com|80 y 443|111.221.76.60
|portal.msua06.manage.microsoft.com|80 y 443|134.170.49.114
|ssu2.manage.microsoft.com|80 y 443|157.55.99.181
|status.manage.microsoft.com|80 y 443|157.55.99.170
|swda01.manage.microsoft.com<br>swda02.manage.microsoft.com<br>swdb01.manage.microsoft.com<br>swdb02.manage.microsoft.com<br>swdc01.manage.microsoft.com<br>swdc02.manage.microsoft.com|80 y 443|93.184.215.200
|*.microsoftonline-p.com|80 y 443||
|*.microsoftonline-p.net|80 y 443||
|*.portal.office.com|80 y 443||
|*.spynet2.microsoft.com|443||
|c.microsoft.com|80 y 443||
|c1.microsoft.com|80 y 443||
|blob.core.windows.net|80 y 443||
|ajax.aspnetcdn.com|80 y 443||
|*.googleapis.com<br>Este dominio es necesario para la compatibilidad con JQuery cuando se utiliza el sitio web del portal de empresa.|80 y 443||
|wustat.microsoft.com|80 y 443||
|Servicios de Microsoft Update|\*.update.microsoft.com<br>download.microsoft.com<br>update.microsoft.com<br>\*.download.windowsupdate.com<br>download.windowsupdate.com<br>\*.windowsupdate.com<br>windowsupdate.microsoft.com<br>ntservicepack.microsoft.com|80 y 443|
|Solicitudes de búsqueda de DNS|manage.microsoft.com.nsatc.net|80|
|Comunicación de dispositivos de Samsung KNOX a través del firewall|Si desea habilitar dispositivos Samsung KNOX para que contacten con servidores KNOX a través del firewall, siga las instrucciones de Preguntas frecuentes de Samsung KNOX.||
|Documentación, ayuda y soporte técnico:</br></br>*.livemeeting.com<br>\*.microsoftonline.com<br>\*.social.technet.microsoft.com<br>blogs.technet.com<br>go.microsoft.com<br>onlinehelp.Microsoft.com<br>www.microsoft.com|80|||



## Requisitos de los servidores proxy
Para administrar los equipos que están detrás de un servidor proxy, tenga en cuenta que:

-   El servidor proxy debe ser compatible con **HTTP** y **HTTPS**, ya que los clientes de Intune usan ambos protocolos.

-   Intune es compatible con servidores proxy no autenticados.

Puede modificar la configuración del servidor proxy o los equipos cliente individuales, o bien usar la configuración de la directiva de grupo para cambiar de todos los equipos cliente que se encuentran detrás de un servidor proxy especificado.

También puede usar un servidor proxy que almacene en caché el contenido para [reducir el ancho de banda de red](network-bandwidth-use.md) usado por los clientes de Intune.



## Requisitos de Service to Service Connector
Service to Service Connector solo admite Exchange basado en la nube y no requiere infraestructura local.

Para usar este conector deben cumplirse las siguientes condiciones:

-   Tiene una suscripción a Office 365 con un inquilino de Exchange Server 2013. Siempre que el inquilino sea Exchange Server 2013, el conector admite Exchange Server 2010 en ese mismo entorno.

-   La cuenta de usuario usada para instalar On-Premises Connector debe ser un administrador de inquilinos de Intune y un administrador en el inquilino de Exchange con una licencia para usar Exchange Server 2013.

### Consulte también
[What to know before you start Microsoft Intune (Información necesaria antes de iniciar Microsoft Intune)](what-to-know-before-you-start-microsoft-intune.md)


<!--HONumber=May16_HO1-->

