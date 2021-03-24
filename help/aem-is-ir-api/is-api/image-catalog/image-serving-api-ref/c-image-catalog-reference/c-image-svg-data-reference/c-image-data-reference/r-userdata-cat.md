---
description: Användardata. Servern returnerar innehållet i det här fältet till klienten som svar på req=userdata.
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Användardata{#userdata}

Användardata. Servern returnerar innehållet i det här fältet till klienten som svar på req=userdata.

## Egenskaper {#section-06f2002b77d54a64be07f12fff54ad13}

Textsträngsvärde. Du bör använda [egenskapsdata](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md)-formatering. Om egenskapsdataformatering inte används får textsträngen inte innehålla tecknet &#39;=&#39;.

Klienterna i visningsprogrammet för zoomning, rotation och broschyrer antar att det här fältet använder formatering av egenskapsdata. Dessa klienter använder det här fältet för konfiguration och anpassning av visningsprogram. Mer information finns i dokumentationen för visningsprogrammet.

Det här fältet deltar i textsträngslokalisering. Mer information finns i [Lokalisering av textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) i *HTTP-protokollreferens*.

## Standard {#section-7ee879762130467199745f2abc662f1e}

Ingen.

## Se även {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , lokalisering av  [textsträng](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
