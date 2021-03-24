---
description: Om en begäran inte kan slutföras returnerar servern antingen en felbild eller en annan HTTP-svarsstatus än 200 tillsammans med ett felmeddelande.
solution: Experience Manager
title: Fel
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Fel{#errors}

Om en begäran inte kan slutföras returnerar servern antingen en felbild eller en annan HTTP-svarsstatus än 200 tillsammans med ett felmeddelande.

Svarsstatusvärdet beror på felets typ. för de vanligaste felen är det &quot;403&quot;. Felsvar för förfrågningstyper som inte är avbildningar följer det format som anges med `req=`. (Kan inte implementeras konsekvent just nu.)

Detaljrikedomen i felmeddelandet kan konfigureras med `attribute::ErrorDetail`.

**Felbilder**

Image Serving kan konfigureras för att returnera felmeddelanden som återges i en bild. Mer information finns i `attribute::ErrorImage` i bildkatalogsreferensen. Om felbilden genereras utan fel är HTTP-svarsstatusen 200. Om ett fel inträffar när felbilden bearbetas returneras standardsvaret på HTTP-felet och textmeddelandet till klienten.

**Se även**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
