---
description: Den här versionen - Image Serving 6.6.1 and Image Rendering 6.6.1 - ersätter Image Serving 6.5.3 och Image Rendering 6.5.3.
solution: Experience Manager
title: Om den här versionen
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
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

