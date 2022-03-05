---
description: Bildåtergivning stöder konvertering av färgrymder baserat på färgrymdsprofiler som uppfyller ICC-specifikationen (International Color Consortium).
solution: Experience Manager
title: Färghantering för bildåtergivning *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Färghantering för bildåtergivning *{#image-rendering-color-management}

Bildåtergivning stöder konvertering av färgrymder baserat på färgrymdsprofiler som uppfyller ICC-specifikationen (International Color Consortium).

**Begränsningar**

För närvarande stöds endast färgrymderna CMYK, RGB och gråskala.

Kabinettformatfiler (.vnc) och fönsteromslagsformatfiler ( [!DNL .vnw]) är inte färghanterade och antas finnas i arbetsfärgrymden.

**Se även**

[International Color Consortium](https://www.color.org/index.xalter) , [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , ICC-profilkartor

## Standardfärgrymder {#section-8ce27edf42e746febe4654f8f19b9c0c}

Varje bildkatalog (och standardkatalogen) kan definiera en uppsättning ICC-profiler. Dessa profiler utgör standardfärgrymderna för den här katalogen - en indata- och en utdataprofil för gråskale-, RGB- och CMYK-data ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`och `attribute::IccProfileSrcCmyk`).

Standardfärgrymden för en viss bild eller ett annat objekt väljs från katalogstandardprofilerna utifrån bildens pixeltyp.

## Färgrymd för indata {#section-660f661a7e954df4b451e34134195276}

Materialbilder kan bädda in ICC-profiler för att definiera indatafärgrymden. Om ingen profil är inbäddad i en källbild `attribute::IccProfileSrc*` av den tillämpliga bildkatalog som motsvarar källbildens pixeltyp används. Om attributet inte är definierat i bildkatalogen, `attribute::IccProfile*` används. Om det katalogattributet inte heller är definierat färghanteras inte bilden och endast naiva omformningar används.

## Arbetsfärgrymd {#section-645d9cfa5b0347a190a0ece218f5b5e1}

Vanligtvis definieras arbetsfärgrymden av ICC-färgprofilen som är inbäddad i vinjetteringen. Om vinjetteringen inte innehåller någon profil används standardprofilen för RGB ( `attribute::IccProfileSrcRgb` av sessionskatalogen) används för arbetsfärgrymden.

Alla återgivningsåtgärder utförs i arbetsfärgrymden.

**Viktigt:** ICC-profilen för arbetsfärgrymden måste ha stöd för in- och utdataomformningar. Om en profil med enbart utdata används som arbetsfärgrymd kan IR inte konvertera material till den. En sådan färgprofil kan fortfarande användas om materialet finns i samma arbetsfärgrymd. Försök att använda material i andra färgrymder kommer att misslyckas.

## Explicit färgvärden {#section-31727bf1b23e477ca92572fbbf422d2f}

RGB-färgvärden som anges med `color=`, `bgc=`, `catalog::BgColor`och `catalog::Color` antas finnas i den aktuella arbetsfärgrymden.

## Materialdatafiler {#section-33f7a170a6664c02b8479fb89cc0aea3}

Materialbildfiler (textur- och dekala bilder) kan ha RGB, gråskala eller CMYK-pixeltyp och kan bädda in en färgprofil. Om ingen färgprofil är inbäddad kopplas bildens standardfärgmodell (t.ex. färgprofilen från materialkatalogen som motsvarar bildens pixeltyp).

Materialbilder som hämtas från kapslad bildserver eller begäran om bildåtergivning innehåller vanligtvis en färgprofil. Om så inte är fallet associeras bilderna med den standardfärgrymd för indata som motsvarar pixeltypen.

Om färgrymden i bildfilen skiljer sig från arbetsfärgrymden, används korrekt färgkonvertering för att konvertera till arbetsfärgrymden. Tidigare typkonvertering används när ingen profil är inbäddad och ingen standardindataprofil är definierad.

Andra materialdatafiler, t.ex. kabinettformatfiler ( [!DNL .vnc]) eller fönster som täcker filer ( [!DNL .vnw]) bäddar inte in färgprofiler och antas alltid finnas i arbetsfärgrymden.

## Färgrymd för utdata {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Alla återgivningsåtgärder utförs i arbetsfärgrymden. Om begäran anger en annan färgprofil med `icc=` konverteras data till den färgrymden precis innan de kodas och returneras till klienten. När färghanteringen är inaktiverad används vid behov en naiv konvertering för att konvertera till gråskala eller CMYK.

## Inbäddade färgprofiler {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Den färgprofil som är associerad med den återgivna bilden kan bäddas in i svarsbilden genom att ange `iccEmbed=` för begäran.

If `icc=` har inte angetts bäddas ICC-profilen för arbetsfärgrymden in. Ingen profil är inbäddad om färghanteringen är inaktiverad och ingen profil har angetts med `icc=`.

## ICC-profiler {#section-afeb76068b5042adb83261638e450140}

Alla färgprofiler som används av servern måste överensstämma med ICC-specifikationen. ICC-profilfiler har vanligtvis en [!DNL .icc] eller [!DNL .icm] filsuffix och finns tillsammans med materialdatafiler.

Utdataprofiler kan anges med filsökväg/namn i `icc=` rekommenderar vi att du registrerar alla profilfiler i ICC-profilkartan för standardkatalogen eller en viss materialkatalog och använder genvägsidentifierare ( `icc::Name`) istället för filsökvägar.

Arbetsprofiler måste registreras i ICC-profilkartan för materialkatalogen eller standardkatalogen.
