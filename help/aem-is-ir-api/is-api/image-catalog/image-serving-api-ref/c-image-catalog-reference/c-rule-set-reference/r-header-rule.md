---
description: Rubrikelement för HTTP-svar. Valfritt i <rule>-element.
seo-description: Rubrikelement för HTTP-svar. Valfritt i <rule>-element.
seo-title: header
solution: Experience Manager
title: header
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# header{#header}

Rubrikelement för HTTP-svar. Valfritt i `<rule>`-element.

## Attribut {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Obligatoriskt. Anger namnet på HTTP-huvudet.

**`Action`= &quot;set&quot; |`"add"`**: Valfritt. Standardvärdet är `"set"`, som ersätter alla aktuella rubrikvärden. Ange `"add"` för att lägga till rubrikvärdet, avgränsat med kommatecken.

## Data {#section-a387f541396c49d99c29692a38032914}

Huvudvärde.

## Beskrivning {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Tillåter att nya HTTP-svarshuvuden läggs till eller ersätts av fördefinierade rubrikvärden. Namn och värden måste följa HTTP-standarder. Ingen ytterligare kodning kommer att användas.

Image Serving-ersättningsvariabler kan användas i rubriknamnet och rubrikvärdet. På så sätt kan du styra båda strängarna från begäran.

## Exempel {#section-cb5b738b9b93407cb2f4d35af3e59c02}

I följande regel används en anpassad rubrik när rubrikvärdet anges som en variabel i begäran:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Den här regeln aktiveras av följande begäran, och HTTP-svarshuvudet `Edge-Control::no-store` anges:

`http://server/is/image/cat/id?$Edge-Control=no-store`
