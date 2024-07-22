---
title: config
description: Parametern är gemensam för alla visningsprogram.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# config{#config}

Parametern är gemensam för alla visningsprogram.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span> </span> </p> </td> 
   <td colname="col2"> <p>Katalog/ID för visningsprogramkonfigurationen. </p> <p> Anger en bildkatalogspost som innehåller visningsprogrammets konfigurationsegenskaper i <span class="codeph">-katalogen::UserData </span>. När det här kommandot finns skickar visningsprogrammet ett <span class="codeph"> req=userdata </span> -kommando för <span class="codeph"> configId </span> till servern och extraherar egenskaper från svaret. Egenskaperna används för att initiera visningsprogrammet. Om URL-strängen anger samma egenskaper åsidosätter de värdena från <span class="codeph">-katalogen::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alla visningsprogramkommandon som kan anges i `catalog::UserData` förväntar sig själva `asset`, `serverUrl`, `contentUrl`, `searchServerUrl` och `config`.

## Egenskaper {#section-10ee45d637134e0fbcd943c62578cb78}

Valfritt.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Ingen.

## Exempel 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

En bildkatalog med namnet 2020 innehåller posten `preset-oct`. Fältet `catalog::UserData` i den här katalogposten innehåller följande data:

```
style=customStyle.css
```

Läs in visningsprogrammet med följande kommando:

```
config=2020/preset-oct
```

Det här exemplet motsvarar följande kommando som anges explicit i URL:en:

```
style=customStyle.css
```

## Exempel 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

En bildkatalog med namnet 2019 innehåller posten `spin-oct`. Fältet `catalog::UserData` i den här katalogposten innehåller följande data:

```
zoomStep=3 
maxZoom=200
```

Läs in visningsprogrammet med följande kommando:

```
config=2019/spin-oct
```

Det här exemplet motsvarar följande kommando som anges explicit i URL:en:

```
zoomStep=3&maxZoom=200
```

## Exempel 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

En visningsförinställning med namnet `Shoppable_Banner` innehåller följande data:

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

Läs in visningsprogrammet med följande kommando:

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

Det här exemplet motsvarar följande kommandon som anges explicit i URL:en:

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Exempel 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

En visningsförinställning med namnet `Shoppable_Video_Dark` innehåller följande data:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

Läs in visningsprogrammet med följande kommando:

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

Det här exemplet motsvarar följande kommandon som anges explicit i URL:en:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Exempel 5 {#section-19b988551d1d492a9079948e0b04b38f}

En visningsförinställning med namnet `Carousel_Dotted_light` och följande data:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Läs in visningsprogrammet med följande kommando:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Det här exemplet motsvarar följande kommandon som anges explicit i URL:en:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
