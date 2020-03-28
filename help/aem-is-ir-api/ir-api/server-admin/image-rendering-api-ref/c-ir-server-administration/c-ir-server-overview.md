---
description: I den här dokumentationen beskrivs hur du administrerar Scene7 Image Rendering-servern.
seo-description: I den här dokumentationen beskrivs hur du administrerar Scene7 Image Rendering-servern.
seo-title: Översikt över serveradministration
solution: Experience Manager
title: Översikt över serveradministration
topic: Scene7 Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Översikt över serveradministration{#server-administration-overview}

I den här dokumentationen beskrivs hur du administrerar Scene7 Image Rendering-servern.

Bildåtergivning består av två huvudkomponenter:

* Ett Java-paket distribueras med Image Serving Platform Server och hanterar klientanslutning, cachelagring och materialkataloger.
* En systemspecifik kodmodul distribueras som ett tilläggsbibliotek för Image Server och implementerar huvudfunktionerna för bildåtergivning.

Båda komponenterna kallas tillsammans för *återgivningsservern*.

Bildåtergivning delar många serverfunktioner med Image Serving, och alla alternativ konfigureras genom redigering av en konfigurationsfil. Ytterligare konfigurationsattribut tillhandahålls av standardkatalogen ( [!DNL default.ini]) eller särskilda materialkataloger. Mer information finns i Materialkataloger.

Installationsmappen för bildåtergivning ( *[!DNL install_folder]*) är [!DNL *[!DNL install_root]*/ImageRendering]. I Windows *[!DNL install_root]* är standardinställningen [!DNL C:\Program Files\Scene7]. En annan mapp kan anges under installationen. I Linux måste *[!DNL install_root]* det alltid vara [!DNL /usr/local/scene7]. Symboliska länkar kan användas.

Alla filsökvägar är skiftlägeskänsliga i UNIX och är skiftlägeskänsliga i Windows.
