---
description: Visa skrivarmärken. Anger hur skrivarmärkena ska visas.
seo-description: Visa skrivarmärken. Anger hur skrivarmärkena ska visas.
seo-title: printerMark
solution: Experience Manager
title: printerMark
topic: Scene7 Image Serving - Image Rendering API
uuid: 3e5699ce-3ccd-4f85-91dd-c40c252a758d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# printerMark{#printermark}

Visa skrivarmärken. Anger hur skrivarmärkena ska visas.

` printerMark= *`trimma`*, *`markörutfallsmärken`*, *`passmärkes`*, *`färgstrecksspage`*, *`information`*, *``*, *`formatlinjebreddlager`*, *`bädda in`*`

De olika märkena kan stängas av eller slås på. Du kan också styra skrivarmärkenas format.

Följande värden är giltiga:

<table id="simpletable_C84560940CAC46D8BE9D0EFEE5EBF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p>ytmärken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Standardvärdet är 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>utfallsmärken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Standardvärdet är 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>passmärken= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Standardvärdet är 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>färgremsor= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Standardvärdet är 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>sidinformation= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Standardvärdet är 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>style= </p></td> 
  <td class="stentry"> <p>Standard </p> <p>InDesignJ1 </p> <p>InDesignJ2 </p> <p>Illustrator </p> <p>IllustratorJ </p> <p>QuarkXPress </p> </td> 
  <td class="stentry"> <p>Standard är Standard </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>linjebredd= </p></td> 
  <td class="stentry"> <p>Alla värden i intervallet 0,125-2,0, båda värdena inkluderade. </p></td> 
  <td class="stentry"> <p>Standardvärdet är 0,25. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>layer embed= </p></td> 
  <td class="stentry"> <p>0|1 </p></td> 
  <td class="stentry"> <p>Standardvärdet är 1. </p></td> 
 </tr> 
</table>

## Exempel {#section-d2e394ddabe14f4ea63af6dab233a163}

`&printerMark=1,1,1,1,1,Illustrator,.25,1`
