---
description: Du måste konfigurera och konfigurera IR 3.x-kompatibilitetsmodulen.
seo-description: Du måste konfigurera och konfigurera IR 3.x-kompatibilitetsmodulen.
seo-title: Konfigurera kompatibilitetsmodulen IR 3.x
solution: Experience Manager
title: Konfigurera kompatibilitetsmodulen IR 3.x
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# Konfigurera kompatibilitetsmodulen IR 3.x{#setup-and-configure-ir-x-compatibility-module}

Du måste konfigurera och konfigurera IR 3.x-kompatibilitetsmodulen.

1. Stanna `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Byt till webbprogramkatalogen för ImageServer.
1. Kopiera innehållet i [!DNL ir] katalogen till [!DNL ROOT] katalogen.
1. Öppna [!DNL ROOT/WEB-INF/web.xml] i en textredigerare.
1. Sök efter raden `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Ta bort kommentarer för `<servlet>` - och `<servlet-mapping>` -taggarna.
1. Starta om `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux-exempel**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Redigera sedan [!DNL web.xml]med din favoritredigerare för att avkommentera `<servlet>` - och `<servlet-mapping>` -taggarna.

**Windows-exempel**

Öppna Utforskaren och gå till `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Markera alla filer och mappar och kopiera dem inuti `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Redigera sedan filen `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`utan att kommentera `<servlet>` - och `<servlet-mapping>` -taggarna.
