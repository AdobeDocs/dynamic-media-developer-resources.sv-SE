---
description: Alla loggfiler skrivs till samma loggmapp som anges med TC-katalogen.
solution: Experience Manager
title: Serverloggning
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Serverloggning{#server-logging}

Alla loggfiler skrivs till samma loggmapp som anges med katalogen TC::directory.

Loggfiler skapas vanligtvis och roteras dagligen. Äldre loggfiler i loggmappen tas automatiskt bort efter ett visst antal dagar ( `TC::maxDays`).

Viktigt! Det måste finnas tillräckligt mycket diskutrymme för loggfiler för att diskutrymmet ska kunna ta slut. 1-2 GB/dag kan behövas för servrar och standardlogginställningar.

Plattformsservern och Image Server skapar de tre typer av loggfiler som beskrivs nedan.

Andra Image Serving-komponenter och vissa andra Dynamic Media-paket, som Dynamic Media Viewer, kan också skapa loggfiler i samma mapp. Loggfilerna är avsedda för Dynamic Media internt bruk och kan begäras av Dynamic Media tekniska support för felsökning.

* [Åtkomstlogg](c-access-log.md)
* [Spårningslogg](c-trace-log.md)
* [Image Server-logg](c-image-server-log.md)

## Se även {#section-5ff5e46031b1461c92de24e632610d6d}

[Åtkomstloggning](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f),  [felsökning/spårningsloggning](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
