---
description: Den här versionen - Image Serving 6.6.1 and Image Rendering 6.6.1 - ersätter Image Serving 6.5.3 och Image Rendering 6.5.3.
seo-description: Den här versionen - Image Serving 6.6.1 and Image Rendering 6.6.1 - ersätter Image Serving 6.5.3 och Image Rendering 6.5.3.
seo-title: Om den här versionen
solution: Experience Manager
title: Om den här versionen
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Om den här versionen{#about-this-release}

Den här versionen - Image Serving 6.6.1 and Image Rendering 6.6.1 - ersätter Image Serving 6.5.3 och Image Rendering 6.5.3.

## Kända fel och beteendeförändringar {#section-9dbc05206187477f926a78e8108a34e1}

* Det går inte längre att använda frågetecknet i resurs-ID:n, även om tecknet är URL-kodat.
* Dynamiska banderollförfrågningar `/xfl/flash/` stöds inte längre och returnerar nu en http 404-felkod.
* W2P `/is/agm/`-begäranden stöds inte längre.
* Vissa felmeddelanden visas inte längre i webbläsaren. Därför måste du granska spårningsloggen för att felsöka.

## Nya funktioner {#section-b1386e36cb4544ebb79766a06b16842d}

* Smart färgruta
* Smart beskärning

## Felkorrigering {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Ett problem har korrigerats där RTF-alternativet `\qc` följt av ett blanksteg orsakade att en begäran inte kunde återges.

