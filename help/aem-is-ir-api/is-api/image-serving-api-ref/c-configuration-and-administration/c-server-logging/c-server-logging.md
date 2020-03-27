---
description: Alla loggfiler skrivs till samma loggmapp som anges med TC-katalogen.
seo-description: Alla loggfiler skrivs till samma loggmapp som anges med TC-katalogen.
seo-title: Serverloggning
solution: Experience Manager
title: Serverloggning
topic: Scene7 Image Serving - Image Rendering API
uuid: f6145737-e4c3-4533-9be5-5b5a0202fe33
translation-type: tm+mt
source-git-commit: 5717550d2dea8ec086875e770ff8f200aaa75ff3

---


# Serverloggning{#server-logging}

Alla loggfiler skrivs till samma loggmapp som anges med katalogen TC::directory.

Loggfiler skapas och roteras vanligtvis dagligen. Äldre loggfiler i loggmappen tas automatiskt bort efter ett visst antal dagar ( `TC::maxDays`).

Viktigt! Det måste finnas tillräckligt mycket diskutrymme för loggfiler för att diskutrymmet ska kunna ta slut. 1-2 GB/dag kan behövas för servrar och standardlogginställningar.

Plattformsservern och Image Server skapar de tre typer av loggfiler som beskrivs nedan.

Andra Image Serving-komponenter och vissa andra Scene7-paket, som Scene7 Viewer, kan också skapa loggfiler i samma mapp. Dessa loggfiler är avsedda för Scene7 internt bruk och kan begäras av Scene7 Support för felsökning.

* [Åtkomstlogg](c-access-log.md)
* [Spårningslogg](c-trace-log.md)
* [Image Server-logg](c-image-server-log.md)

## Se även {#section-5ff5e46031b1461c92de24e632610d6d}

[Åtkomstloggning](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [felsökning/spårningsloggning](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
