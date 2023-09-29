---
title: header
description: HTTP-svarsrubrikelement. Valfritt i <rule> -element.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# header{#header}

HTTP-svarsrubrikelement. Valfritt i `<rule>` -element.

## Attribut {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Obligatoriskt. Anger namnet på HTTP-huvudet.

**`Action`= &quot;set&quot; |`"add"`**: Valfritt. Standard är `"set"`, som ersätter alla aktuella rubrikvärden. Ange `"add"` så att du kan lägga till rubrikvärdet, avgränsat med kommatecken.

## Data {#section-a387f541396c49d99c29692a38032914}

Huvudvärde.

## Beskrivning {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Tillåter att nya HTTP-svarshuvuden läggs till och att värden för fördefinierade huvuden läggs till eller ersätts. Namn och värden måste följa HTTP-standarder. Ingen ytterligare kodning används.

Image Serving-ersättningsvariabler kan användas i rubriknamnet och i rubrikvärdet. På så sätt kan du styra båda strängarna från begäran.

## Exempel {#section-cb5b738b9b93407cb2f4d35af3e59c02}

I följande regel används en anpassad rubrik när rubrikvärdet anges som en variabel i begäran:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Den här regeln aktiveras av följande begäran, och HTTP-svarshuvudet anges `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
