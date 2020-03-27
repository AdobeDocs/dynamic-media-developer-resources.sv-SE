---
description: Ersättningssträngselement. Valfritt i <rule>-element.
seo-description: Ersättningssträngselement. Valfritt i <rule>-element.
seo-title: ersättning
solution: Experience Manager
title: ersättning
topic: Scene7 Image Serving - Image Rendering API
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ersättning{#substitution}

Ersättningssträngselement. Valfritt i `<rule>` element.

## Attribut {#section-d955eefc53eb4274861270669c01f9ca}

Ingen.

## Data {#section-a2688866ed6d41279a8478886e511ae3}

Ersättningssträng.

## Beskrivning {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definierar en ersättningssträng för den matchande strängen eller delsträngen i sökvägen eller frågan.

Om mönsteruttrycket innehåller deluttryck (avgränsade med parenteser) ersätts den första matchande delsträngen med ersättningssträngen. Om mönsteruttrycket inte innehåller underuttryck ersätts hela den matchade strängen.

Om `<expression>` är tom eller saknas läggs ersättningssträngen till i sökvägen eller frågan.

Om `<substitution>` är tom tas den matchande strängen eller delsträngen bort. Om `<substitution>` inte anges ändras inte sökvägen eller frågesträngen.

## Anteckning {#section-90fe89bb17a04804b7ff3c93df082892}

Ersättningssträngen får inte innehålla literala &lt;- och &amp;-tecken. Dessa reserverade tecken kan kodas med `&` respektive `<`eller så kan hela strängen omslutas av ett XML- `CDATA` avsnitt:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
