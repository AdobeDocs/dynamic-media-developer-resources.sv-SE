---
description: I den här dokumentationen beskrivs hur du administrerar Dynamic Media Image Rendering-servern.
solution: Experience Manager
title: Översikt över serveradministration
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '168'
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
