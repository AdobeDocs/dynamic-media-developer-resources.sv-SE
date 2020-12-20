---
description: Vinjetteringskonverteraren (vntc) är ett kommandoradsverktyg som används för att förbereda innehåll som skapats med Image Authoring för distribution med Image Rendering.
seo-description: Vinjetteringskonverteraren (vntc) är ett kommandoradsverktyg som används för att förbereda innehåll som skapats med Image Authoring för distribution med Image Rendering.
seo-title: Vinjettkonverterare
solution: Experience Manager
title: Vinjettkonverterare
topic: Scene7 Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Vinjettkonverterare{#vignette-converter}

Vinjetteringskonverteraren (vntc) är ett kommandoradsverktyg som används för att förbereda innehåll som skapats med Image Authoring för distribution med Image Rendering.

[!DNL vntc] finns i [!DNL  *[!DNL install_root]*\ImageServing\bin]. Den har följande funktioner:

* Konverterar primära vinjetteringar till en enda upplösning, flera upplösningar eller pyramidproduktionvinjetteringar (se [Vinjetteringsskalning](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Skapar ett produktionsskåp och ett fönster som täcker formatfiler (se `-resolution` och `-jpegquality`).

* Kan producera olika filversioner av vinjetter, skåp och fönsteromslag för användning med äldre versioner av bildåtergivning.
* Extraherar visningsbilder från vinjetter, antingen med full upplösning eller miniatyrbilder (se `-thumbwidth` och `-image`).
* Extraherar relevanta egenskaper från källfilen (se `-info`) och skickar dem till `stdout` eller en valfri loggfil (se `-log`).

Även om det är valfritt att använda [!DNL vntc] rekommenderas det starkt för bästa serverprestanda. [!DNL vntc] implementerar även omfattande felkontroll och kan förhindra allvarliga serverproblem, inklusive krascher, när de används flitigt.

När du genererar produktionsvinjetteringar läggs pixelbredden för utdatavvinjetteringen (eller 0 om det är en pyramid- eller flerupplösningsvinjettering) till efter namnet på den genererade utdatavvinjettfilen. När du bearbetar kabinettformatfiler läggs utdataupplösningen till i utdatafilens namn. Alla utdatafiler, inklusive miniatyr-, bild- och loggfiler samt produktionsvinjetterings- eller kabinettformatfilen, placeras i samma katalog där *[!DNL sourceFile]* finns (om inte `-destPath` har angetts).

[!DNL vntc] begränsar sig som standard till högst 3 GB minne. När Vntc når den här gränsen avbryts bearbetningen och ett fel genereras. Den här gränsen kan ändras med `-maxmem`.

>[!NOTE]
>
>Vinjetteringsverktyget i Bildredigering kan också användas för att förbereda vinjetter för bildåtergivning. På samma sätt kan innehållsredigeringsverktyget generera kabinettformatfiler för användning med bildåtergivning. Använd [!DNL vntc] om bearbetningen ska automatiseras. Verktygen i Bildredigering har ett grafiskt användargränssnitt, vilket gör det enklare att använda interaktivt.

## Se även {#section-3c756bf17b634543904fdd928adeafb2}

Dokumentation för bildredigering
