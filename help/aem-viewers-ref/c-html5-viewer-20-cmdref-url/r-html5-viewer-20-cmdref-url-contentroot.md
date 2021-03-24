---
description: Parametern är gemensam för alla visningsprogram.
solution: Experience Manager
title: contentUrl
feature: Dynamic Media Classic,visningsprogram,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 1%

---


# contentUrl{#contenturl}

Parametern är gemensam för alla visningsprogram.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Anger grundsökvägen till anpassade CSS-filer, undertextningsinnehåll eller navigeringsinnehåll. </p> <p>Om sökvägen inte har något inledande <span class="filepath"> /</span> är det relativt till platsen för visningsprogrammets HTML-sida. Om sökvägen har en inledande <span class="filepath"> /</span> anger den en absolut sökväg på samma server. </p> <p> Påverkar inte inläsningen av standard-CSS-filen när du inte anger ett formatkommando. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-10ee45d637134e0fbcd943c62578cb78}

Valfritt.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Exempel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```

