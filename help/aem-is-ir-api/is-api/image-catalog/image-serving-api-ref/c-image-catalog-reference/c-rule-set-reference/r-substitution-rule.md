---
description: Ersättningssträngselement. Valfritt i <rule>-element.
solution: Experience Manager
title: substitutioner
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# substitutioner{#substitution}

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
>Alla matchningar i indatasträngen ersätts när `replace="all"` anges i elementet `<rule>` som det här `<substitution>`-elementet tillhör. Som standard ersätts bara den första matchningen med ersättningssträngen.

## Anteckning {#section-cedf2adabaaf441c9f598fb0ea180246}

Ersättningssträngen får inte innehålla literala &lt;- och &amp;-tecken. Dessa reserverade tecken kan kodas med `&` respektive `<`, eller så kan hela strängen omslutas av ett XML CDATA-avsnitt:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
