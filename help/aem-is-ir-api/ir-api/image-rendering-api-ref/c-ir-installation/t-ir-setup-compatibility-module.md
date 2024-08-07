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
1. Kopiera innehållet i katalogen [!DNL ir] till katalogen [!DNL `ROOT`].
1. Öppna [!DNL `ROOT/WEB-INF/web.xml`] i en textredigerare.
1. Sök efter raden `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Avkommentera taggarna `<servlet>` och `<servlet-mapping>`.
1. Starta om `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux®-exempel**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Redigera sedan [!DNL `web.xml`] med din favoritredigerare för att avkommentera taggarna `<servlet>` och `<servlet-mapping>`.

**Windows-exempel**

Öppna Explorer och gå till `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Markera alla filer och mappar och kopiera dem i `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Redigera sedan filen `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml` och avkommenterar taggarna `<servlet>` och `<servlet-mapping>`.
