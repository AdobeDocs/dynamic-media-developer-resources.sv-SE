---
description: I den här dokumentationen beskrivs hur du administrerar Dynamic Media Image Rendering-servern.
solution: Experience Manager
title: Översikt över serveradministration
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '172'
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
