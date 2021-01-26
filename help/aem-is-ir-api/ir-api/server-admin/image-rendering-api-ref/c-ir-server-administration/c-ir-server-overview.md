---
description: I den här dokumentationen beskrivs hur du administrerar Dynamic Media Image Rendering-servern.
seo-description: I den här dokumentationen beskrivs hur du administrerar Dynamic Media Image Rendering-servern.
seo-title: Översikt över serveradministration
solution: Experience Manager
title: Översikt över serveradministration
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Översikt över serveradministration{#server-administration-overview}

I den här dokumentationen beskrivs hur du administrerar Dynamic Media Image Rendering-servern.

Bildåtergivning består av två huvudkomponenter:

* Ett Java-paket distribueras med Image Serving Platform Server och hanterar klientanslutning, cachelagring och materialkataloger.
* En systemspecifik kodmodul distribueras som ett tilläggsbibliotek för Image Server och implementerar huvudfunktionerna för bildåtergivning.

Båda komponenterna kallas tillsammans för *återgivningsservern*.

Bildåtergivning delar många serverfunktioner med Image Serving, och alla alternativ konfigureras genom redigering av en konfigurationsfil. Ytterligare konfigurationsattribut tillhandahålls av standardkatalogen ( [!DNL default.ini]) eller särskilda materialkataloger. Mer information finns i Materialkataloger.

Installationsmappen för bildåtergivning ( *[!DNL install_folder]*) är [!DNL *[!DNL install_root]*/ImageRendering]. I Windows är standard *[!DNL install_root]* `C:\Program Files\Scene7`. En annan mapp kan anges under installationen. I Linux måste *[!DNL install_root]* alltid vara [!DNL /usr/local/scene7]. Symboliska länkar kan användas.

Alla filsökvägar är skiftlägeskänsliga i UNIX och är skiftlägeskänsliga i Windows.
