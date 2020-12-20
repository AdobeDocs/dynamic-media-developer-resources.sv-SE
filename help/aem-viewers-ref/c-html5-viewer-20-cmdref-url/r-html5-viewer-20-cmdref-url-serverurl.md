---
description: Parametern är gemensam för alla visningsprogram.
seo-description: Parametern är gemensam för alla visningsprogram.
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
topic: Dynamic media
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# serverUrl{#serverurl}

Parametern är gemensam för alla visningsprogram.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Rotsökväg för relativ eller absolut bildserver. </p> <p> Anger en relativ eller absolut sökväg till Image Serving, från vilken visningsprogrammet hämtar bilder. Om sökvägen inte har något inledande <span class="filepath"> /</span> är det relativt till platsen för visningsprogrammets HTML-sida. Om sökvägen har en inledande <span class="filepath"> /</span> anger den en absolut sökväg på samma server. </p> <p> Använd bara en absolut sökväg om e-postdelningsmodulen är aktiverad i visningsprogrammet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-10ee45d637134e0fbcd943c62578cb78}

Valfritt. Krävs inte för standardanvändning av SaaS (programvara som tjänst).

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Exempel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

