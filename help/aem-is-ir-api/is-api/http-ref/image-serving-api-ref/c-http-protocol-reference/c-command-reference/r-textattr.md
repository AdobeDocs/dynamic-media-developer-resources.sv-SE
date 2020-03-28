---
description: Textlagerattribut. Anger ytterligare attribut för textlager som inte är tillgängliga som rtf-kommandon.
seo-description: Textlagerattribut. Anger ytterligare attribut för textlager som inte är tillgängliga som rtf-kommandon.
seo-title: textAttr
solution: Experience Manager
title: textAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 07b3d263-2ed6-4363-83e1-3b841e9967c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# textAttr{#textattr}

Textlagerattribut. Anger ytterligare attribut för textlager som inte är tillgängliga som rtf-kommandon.

` textAttr= *``*[, *``*[, *``*[, *`resantiAliasingresModewordWrap`*]]]`

<table id="simpletable_0072BF7DF52B4959A14EDEF60A6EBDEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> res </span></span> </p> </td> 
  <td class="stentry"> <p>Ett sätt att skala textlagret utan att ändra teckensnittsstorlek. Högre upplösningsvärden ökar storleken på den återgivna texten i förhållande till arbetsytans storlek. mindre värden minskar textstorleken. Textupplösning i punkter per tum (int större än 0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> kantutjämning </span></span> </p> </td> 
  <td class="stentry"> <p>Styr det kantutjämningsläge som används av textåtergivningsmotorn. </p> <p> <span class="codeph"> av| norm| klar| skarp| stark| utjämnad </span> </p> <p> 
    <table id="simpletable_AE2331118FCA4BC7877233E287CED6A4"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> av </span> </p> </td> 
      <td class="stentry"> <p>Inaktivera kantutjämning av text. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> norm </span> </p> </td> 
      <td class="stentry"> <p>Aktivera kantutjämning av standardtext (standard). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> skarp </span> </p> </td> 
      <td class="stentry"> <p>Välj kantutjämningsläget i Photoshop <span class="codeph"> skarpt </span> (endast <span class="codeph"> textPs= </span> ). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> skarp </span> </p> </td> 
      <td class="stentry"> <p>Välj kantutjämningsläget i Photoshop <span class="codeph"> skarpt </span> ( <span class="codeph"> textPs= </span> enbart). </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> stark </span> </p> </td> 
      <td class="stentry"> <p>Välj <span class="codeph"> starkt kantutjämningsläge i Photoshop </span> ( <span class="codeph"> textPs= </span> enbart). </p> </td> 
     </tr> 
    </table> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> resMode </span></span> </p> </td> 
  <td class="stentry"> <p>Styr hur upplösningen används vid återgivning av texten </p> <p> <span class="codeph"> fixedRes| autoRes| maxRes </span> </p> <p> 
    <table id="simpletable_2CFC06DB37154C7C92614FDF7A818DB5"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> fixedRes </span> </p> </td> 
      <td class="stentry"> <p>Använd angiven upplösning. </p> <p>Använd det här alternativet om texten ska återges i exakt storlek i förhållande till den sammansatta arbetsytan. Texten kan beskäras till lagerstorleken (om den anges) om textrutan är för liten. Det här är det enda <span class="varname"> alternativet förMode </span> som stöds av <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> autoRes </span> </p> </td> 
      <td class="stentry"> <p>Justera upplösningen automatiskt så att lagerrektangeln bäst fylls med texten. </p> <p>Använd för att automatiskt justera textstorleken så att textrutan fylls så mycket som möjligt, utan risk för trunkering. Om automatisk radbrytning är aktiverat kan texten radbrytas med den slutliga upplösningen. <span class="varname"> res </span> ignoreras om <span class="codeph"> autoRes </span> markeras. Stöds inte av <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> maxRes </span> </p> </td> 
      <td class="stentry"> <p>Använd angiven upplösning. minska den om det behövs för att förhindra att texten trunkeras till lagerrektangeln. </p> <p>Används för att återge text med exakt angiven upplösning, så länge som inget urklipp inträffar. Vid bortfall minskas upplösningen automatiskt så att all text finns helt inuti textrutan. Om automatisk radbrytning är aktiverat kan texten radbrytas med den slutliga upplösningen. Stöds inte av <span class="codeph"> textPs= </span>. </p> </td> 
     </tr> 
    </table> </p> <p>Om textlagrets storlek inte anges med size= eller om bara bredden anges, ignoreras inställningarna autoRes och maxRes och den angivna upplösningen används för att återge texten. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> wordWrap </span></span> </p> </td> 
  <td class="stentry"> <p>Anger figursättningsläget. </p> <p> <span class="codeph"> bryt| noWrap| nbWrap </span> </p> <p> 
    <table id="simpletable_FF2510E029EC41E29BC30D9FC2923EA3"> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> noWrap </span> </p> </td> 
      <td class="stentry"> <p>Inaktivera automatisk radbrytning. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> bryt </span> </p> </td> 
      <td class="stentry"> <p>Aktivera automatisk radbrytning. </p> <p>Bryter vid behov långa ord. <span class="codeph"> textPs= </span> stöder endast <span class="codeph"> radbrytning </span>. </p> </td> 
     </tr> 
     <tr class="strow"> 
      <td class="stentry"> <p> <span class="codeph"> nbWrap </span> </p> </td> 
      <td class="stentry"> <p>Aktivera fast radbrytning. </p> <p>Bryter aldrig ett ord, även om det kortas av i slutet. Används vanligtvis tillsammans med <span class="codeph"> autoRes </span> eller <span class="codeph"> maxRes </span> för att säkerställa att långa ord aldrig bryts. </p> </td> 
     </tr> 
    </table> </p> <p>Svep <span class="codeph"> och </span> lägg <span class="codeph"> </span> in automatisk radbrytning vid ordgränser och bindestreck. </p> </td> 
 </tr> 
</table>

## Egenskaper {#section-114ca0b8585b403c873e2251478ad1d5}

Textlagerattribut. Ignoreras med bild, heltäckande färg och effektlager. Gäller för `layer=0` om det anges för `layer=comp`.

## Standard {#section-855230f5330b4afc8a933f00a1ed4612}

`textAttr=72,norm,fixedRes,wrap`

## Se även {#section-68b0d2e2d0474e2097a9331ae272c224}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
