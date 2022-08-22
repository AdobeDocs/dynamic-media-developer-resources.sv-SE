---
title: Konfigurera kompatibilitetsmodulen IR 3.x
description: Konfigurera kompatibilitetsmodulen IR 3.x.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# Konfigurera kompatibilitetsmodulen IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Stoppa `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Byt till webbprogramkatalogen för ImageServer.
1. Kopiera innehållet i [!DNL ir] till [!DNL `ROOT`] katalog.
1. Öppna [!DNL `ROOT/WEB-INF/web.xml`] i en textredigerare.
1. Sök efter raden `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Avkommentera `<servlet>` och `<servlet-mapping>` -taggar.
1. Starta om `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux®-exempel**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Redigera sedan [!DNL `web.xml`] använda din favoritredigerare för att avkommentera `<servlet>` och `<servlet-mapping>` -taggar.

**Exempel på Windows**

Öppna Utforskaren och gå till `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Markera alla filer och mappar och kopiera dem inuti `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Redigera sedan filen `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, avkommentera `<servlet>` och `<servlet-mapping>` -taggar.
