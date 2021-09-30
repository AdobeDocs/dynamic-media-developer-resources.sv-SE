---
title: SocialShare.bearing
description: Konfigurationsattribut för Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

Konfigurationsattribut för Interactive Video Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-ateral</span> </p> </td> 
   <td colname="col2"> <p> Anger riktningen på bildruteanimeringen för knappbehållaren. När den anges till <span class="codeph"> upp</span>, <span class="codeph"> ned</span>, <span class="codeph"> vänster</span> eller <span class="codeph"> höger</span>, rullas panelen ut i den angivna riktningen utan någon ytterligare kontroll av gränserna, vilket kan leda till att panelen klipps av en extern behållare. </p> <p>När komponenten är inställd på <span class="codeph"> fit-vertical</span> flyttas baspanelens position först till slutet av SocialShare. Sedan försöker programmet rulla ut panelen i någon av följande riktningar från en sådan basplats: nerifrån, höger, vänster. För varje försök kontrollerar komponenten om panelen har klippts av en extern behållare. Om alla försök misslyckas försöker komponenten att flytta baspanelens position till toppen och upprepar rolloutförsöken från överkant, höger och vänster riktning. </p> <p>När den är inställd på <span class="codeph"> fit-ateral</span>, använder komponenten en liknande logik, men flyttar basen till höger först och försöker åt höger, nedåt och uppåt. Sedan flyttas basen till vänster och leder fram till vänster, nedåt och uppåt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-1e637b22e8a44d759d588e47576891e6}

Valfritt.

## Standard {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Exempel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
