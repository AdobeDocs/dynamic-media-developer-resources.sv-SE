---
description: Parametern är gemensam för alla visningsprogram.
seo-description: Parametern är gemensam för alla visningsprogram.
seo-title: config
solution: Experience Manager
title: config
topic: Dynamic media
uuid: 9e9bb580-a33a-4405-b05c-56962d702145
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# config{#config}

Parametern är gemensam för alla visningsprogram.

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span></span> </p> </td> 
   <td colname="col2"> <p>Katalog/ID för visningsprogramkonfigurationen. </p> <p> Anger en bildkatalogspost som innehåller visningsprogrammets konfigurationsegenskaper i <span class="codeph"> katalogen::UserData </span>. När det här kommandot finns skickar visningsprogrammet ett <span class="codeph"> req=userdata- </span> kommando för <span class="codeph"> configId </span> till servern och extraherar egenskaper från svaret. Egenskaperna används för att initiera visningsprogrammet. Om URL-strängen anger samma egenskaper åsidosätter de värdena från <span class="codeph"> katalog::UserData </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alla visningsprogramkommandon som kan anges i `catalog::UserData` Expect `asset`, `serverUrl`, `contentUrl`, `searchServerUrl`och `config` sig själv.

## Egenskaper {#section-10ee45d637134e0fbcd943c62578cb78}

Valfritt.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Ingen.

## Exempel 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

En bildkatalog med namnet 2020 innehåller posten `preset-oct`. Fältet `catalog::UserData` för den här katalogposten innehåller följande data:

```
style=customStyle.css
```

Läs in visningsprogrammet med följande kommando:

```
config=2020/preset-oct
```

Detta motsvarar följande kommandon som anges explicit i URL:en:

```
style=customStyle.css
```

## Exempel 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

En bildkatalog med namnet 2019 innehåller posten `spin-oct`. Fältet `catalog::UserData` för den här katalogposten innehåller följande data:

```
zoomStep=3 
maxZoom=200
```

Läs in visningsprogrammet med följande kommando:

```
config=2019/spin-oct
```

Detta motsvarar följande kommandon som anges explicit i URL:en:

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

Detta motsvarar följande kommandon som anges explicit i URL:en:

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

Detta motsvarar följande kommandon som anges explicit i URL:en:

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## Exempel 5 {#section-19b988551d1d492a9079948e0b04b38f}

En visningsförinställning med namnet `Carousel_Dotted_light` följande data:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

Läs in visningsprogrammet med följande kommando:

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

Detta motsvarar följande kommandon som anges explicit i URL:en:

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

