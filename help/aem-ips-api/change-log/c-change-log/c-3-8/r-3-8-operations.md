---
description: Beskriver nya och ändrade operationsmetoder för IPS API version 3.8.
solution: Experience Manager
title: Nya och ändrade åtgärder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# Åtgärder: Nytt och ändrat{#operations-new-and-modified}

Beskriver nya och ändrade operationsmetoder för IPS API version 3.8.

Syntax

## Nya åtgärder {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## Ändrade åtgärder {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* Med den valfria parametern `publishState` kan du söka efter resursläget `MarkedForPublish/NotMarkedForPublish`.

**getJobLogs**

* Med den valfria parametern `userHandle` kan du hämta jobbloggar som skickats in av en viss användare.
