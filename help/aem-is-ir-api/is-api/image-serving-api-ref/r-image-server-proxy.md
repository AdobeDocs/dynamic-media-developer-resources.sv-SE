---
description: En bildserverproxy kan användas för att ändra storlek på bilder för japanska telefoner.
seo-description: En bildserverproxy kan användas för att ändra storlek på bilder för japanska telefoner.
seo-title: Bildserverproxy
solution: Experience Manager
title: Bildserverproxy
topic: Scene7 Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# Bildserverproxy{#image-server-proxy}

En bildserverproxy kan användas för att ändra storlek på bilder för japanska telefoner.

## URL-format {#section-2e8c40b0547c4f99874cdf502b338940}

URL-formatet för IS-proxyn påminner mycket om vanliga IS-begäranden. Alla IS-modifierare som skickas till proxyn skickas till Image Server. Information om IS-modifierare finns i [HTTP Protocol Reference](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Proxyspecifik modifieringslista {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Anger den procentandel av enhetens användbara bredd som ska användas som bildbredd. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Anger den procentandel av enhetens användbara höjd som ska användas som bildhöjd. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Anger procentandelen av enhetens inbäddade mediaegenskap för minnesbegränsning som svarsstorleken ska begränsas till. Detta gäller endast jpg-svar. Kvaliteten på bilden sänks tills svarsstorleken ligger inom den angivna procentandelen. </p></td> 
 </tr> 
</table>

## Minnesgräns för inbäddad bild {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Om enheten har en gräns för storleken på bilder som kan bäddas in på en webbsida, begränsas bildstorleken till den storleken så länge svarsformatet är jpg. Proxyservern begränsar svaren till 500 MB om enheten inte har någon gräns.

## Backend-bearbetning {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

Proxyn hämtar, verifierar och läser in datafilen för enhetskartan en gång om dagen. Verifieringen tar fram olika egenskaper för olika enheter och jämför dem med förväntade värden innan nya data accepteras.
