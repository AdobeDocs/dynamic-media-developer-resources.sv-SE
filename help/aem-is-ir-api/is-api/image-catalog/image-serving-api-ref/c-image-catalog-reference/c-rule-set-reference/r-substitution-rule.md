---
description: Ersättningssträngselement. Valfritt i <rule>-element.
seo-description: Ersättningssträngselement. Valfritt i <rule>-element.
seo-title: ersättning
solution: Experience Manager
title: ersättning
uuid: e5730559-0512-4416-927d-a7faf9180741
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# ersättning{#substitution}

Ersättningssträngselement. Valfritt i `<rule>`-element.

## Attribut {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Ingen.

## Data {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Ersättningssträng.

## Beskrivning {#section-4a64a93f5e1a4d04a2db19166578bf76}

Definierar en ersättningssträng för den matchande strängen eller delsträngen i sökvägen eller frågan.

Om mönsteruttrycket innehåller deluttryck (avgränsade med parenteser) ersätts den första matchade delsträngen med ersättningssträngen. Om mönsteruttrycket inte innehåller underuttryck ersätts hela den matchade strängen.

Om `<expression>` är tom eller saknas läggs ersättningssträngen till i sökvägen eller frågan.

Om `<substitution>` är tom tas den matchande strängen eller delsträngen bort. Om `<substitution>` inte anges ändras inte sökvägen eller frågesträngen.

>[!NOTE]
>
>Alla matchningar i indatasträngen ersätts när `replace="all"` anges i `<rule>`-elementet som det här `<substitution>`-elementet tillhör. Som standard ersätts bara den första matchningen med ersättningssträngen.

## Anteckning {#section-cedf2adabaaf441c9f598fb0ea180246}

Ersättningssträngen får inte innehålla literala &lt;- och &amp;-tecken. Dessa reserverade tecken kan kodas med `&` respektive `<`, eller så kan hela strängen omslutas av ett XML CDATA-avsnitt:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
