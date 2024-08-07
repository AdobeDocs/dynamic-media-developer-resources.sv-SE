---
title: substitutioner
description: Ersättningssträngselement. Valfritt i <rule>-element.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# substitutioner{#substitution}

Ersättningssträngselement. Valfritt i `<rule>`-element.

## Attribut {#section-d955eefc53eb4274861270669c01f9ca}

Ingen.

## Data {#section-a2688866ed6d41279a8478886e511ae3}

Ersättningssträng.

## Beskrivning {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definierar en ersättningssträng för den matchande strängen eller delsträngen i sökvägen eller frågan.

Om mönsteruttrycket innehåller deluttryck (avgränsade med parenteser) ersätts den första matchade delsträngen med ersättningssträngen. Om mönsteruttrycket inte innehåller underuttryck ersätts hela den matchade strängen.

Om `<expression>` är tom eller saknas läggs ersättningssträngen till i sökvägen eller frågan.

Om `<substitution>` är tom tas den matchande strängen eller delsträngen bort. Om `<substitution>` inte anges ändras inte sökvägen eller frågesträngen.

## Anteckning {#section-90fe89bb17a04804b7ff3c93df082892}

Ersättningssträngen får inte innehålla literala &lt;- och &amp;-tecken. Dessa reserverade tecken kan kodas med `&` respektive `<`, eller så kan hela strängen omslutas av ett XML `CDATA` -avsnitt:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
