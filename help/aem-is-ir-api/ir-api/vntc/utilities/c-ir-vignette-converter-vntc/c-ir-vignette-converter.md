---
title: Vinjettkonverterare
description: Vinjetteringskonverteraren (vntc) är ett kommandoradsverktyg som används för att förbereda innehåll som skapats med Image Authoring för distribution med Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Vinjettkonverterare{#vignette-converter}

Vinjetteringskonverteraren (vntc) är ett kommandoradsverktyg som används för att förbereda innehåll som skapats med Image Authoring för distribution med Image Rendering.

[!DNL vntc] finns i [!DNL *[!DNL install_root]*\ImageServing\bin]. Den har följande funktioner:

* Konverterar primära vinjetteringar till enupplösning, flerupplösning eller pyramidproduktionvinjetteringar (se [Vinjettskalning](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Skapar ett produktionsskåp och ett fönster som täcker formatfiler (se `-resolution` och `-jpegquality`).

* Producera olika filversioner av vinjetter, skåp och fönsteromslag för användning med äldre versioner av bildåtergivning.
* Extraherar visningsbilder från vinjetter, antingen med full upplösning eller miniatyrbilder (se `-thumbwidth` och `-image`).
* Extraherar relevanta egenskaper från källfilen (se `-info`) och skickar dem till `stdout` eller en valfri loggfil (se `-log`).

Även om det är valfritt att använda [!DNL vntc] rekommenderar Adobe att den används för bästa serverprestanda. Vinjetteringskonverteraren utför även omfattande felkontroll och kan förhindra allvarliga serverproblem, inklusive krascher, när de används flitigt.

När du genererar produktionsvinjetteringar läggs pixelbredden för utdatavvignetten (eller 0 om pyramid eller flerupplösta vinjetteringar) till efter namnet på den genererade utdatavvinjettfilen. När du bearbetar kabinettformatfiler läggs utdataupplösningen till i utdatafilens namn. Alla utdatafiler, inklusive miniatyrbilds-, bild- och loggfiler och formatfilen för produktionsvinjettering eller skåp placeras i samma katalog där *[!DNL sourceFile]* finns (om inte `-destPath` anges).

Vinjettkonverteraren begränsar sig som standard till högst 3 GB minne. När vntc når denna gräns avbryts bearbetningen och ett fel uppstår. Den här gränsen kan ändras med `-maxmem`.

>[!NOTE]
>
>Vinjetteringsverktyget i Bildredigering kan också användas för att förbereda vinjetter för bildåtergivning. På samma sätt kan verktyget Innehållsredigering generera kabinettformatfiler som kan användas med bildåtergivning. Använd [!DNL vntc] om bearbetningen ska automatiseras. Verktygen i Bildredigering har ett grafiskt användargränssnitt, vilket gör det enklare att använda interaktivt.

## Se även {#section-3c756bf17b634543904fdd928adeafb2}

Dokumentation för bildredigering
