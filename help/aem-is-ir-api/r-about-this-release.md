---
description: Den här versionen - Image Serving 6.6.1 and Image Rendering 6.6.1 - ersätter Image Serving 6.5.3 och Image Rendering 6.5.3.
seo-description: Den här versionen - Image Serving 6.6.1 and Image Rendering 6.6.1 - ersätter Image Serving 6.5.3 och Image Rendering 6.5.3.
seo-title: Om den här versionen
solution: Experience Manager
title: Om den här versionen
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Om den här versionen{#about-this-release}

Den här versionen - Image Serving 6.6.1 and Image Rendering 6.6.1 - ersätter Image Serving 6.5.3 och Image Rendering 6.5.3.

## Kända fel och beteendeförändringar {#section-9dbc05206187477f926a78e8108a34e1}

* Det går inte längre att använda frågetecknet i resurs-ID:n, även om tecknet är URL-kodat.
* Dynamiska `/xfl/flash/` bannerförfrågningar stöds inte längre och returnerar nu en http 404-felkod.
* W2P- `/is/agm/` begäranden stöds inte längre.
* Vissa felmeddelanden visas inte längre i webbläsaren. Därför måste du granska spårningsloggen för att felsöka.

## Nya funktioner {#section-b1386e36cb4544ebb79766a06b16842d}

* Smart färgruta
* Smart beskärning

## Felkorrigering {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Ett problem där RTF-alternativet följt av ett blanksteg orsakade att en begäran inte kunde återges har åtgärdats. `\qc`

