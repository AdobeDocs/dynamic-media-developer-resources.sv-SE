---
description: Om en begäran inte kan slutföras returnerar servern antingen en felbild eller en annan HTTP-svarsstatus än 200 tillsammans med ett felmeddelande.
solution: Experience Manager
title: Fel
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Fel{#errors}

Om en begäran inte kan slutföras returnerar servern antingen en felbild eller en annan HTTP-svarsstatus än 200 tillsammans med ett felmeddelande.

Svarsstatusvärdet beror på felets typ. För de vanligaste felen är det &quot;403&quot;. Felsvar för förfrågningstyper som inte är avbildningar följer det format som anges med `req=`. (Kan inte implementeras konsekvent just nu.)

Detaljrikedomen i felmeddelandet kan konfigureras med `attribute::ErrorDetail`.

## Felbilder {#section-92e9b20b2507433daa96923abc95f777}

Image Serving kan konfigureras för att returnera felmeddelanden som återges i en bild.

Mer information finns i [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) i bildkatalogsreferensen.

Om felbilden genereras utan fel är HTTP-svarsstatusen 200. Om ett fel inträffar när felbilden bearbetas returneras standardsvaret på HTTP-felet och textmeddelandet till klienten.

## Standardbild {#section-66bf25fe6b434081bfae96d38d9be25e}

Image Serving kan konfigureras så att en bild som saknas ersätts med en standardbild. Standardbilden kan anges antingen med kommandot `attribute::DefaultImage` eller `defaultImage=`.

## Se även {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
