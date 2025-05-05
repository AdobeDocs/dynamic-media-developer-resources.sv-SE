---
description: Kommandovärden måste vara http-kodade med %xx escape-sekvenser, så att värdesträngarna inte innehåller de reserverade tecknen '=', '&' och '%'.
solution: Experience Manager
title: Image Serving HTTP encoding
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aec8463f-f72a-4203-89ab-8a4f0ad9d6f9
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 14%

---

# Image Serving HTTP encoding{#image-serving-http-encoding}

Kommandovärden måste vara http-kodade med %xx escape-sekvenser, så att värdesträngarna inte innehåller de reserverade tecknen &#39;=&#39;, &#39;&amp;&#39; och &#39;%&#39;.

Annars gäller standardreglerna för HTTP-kodning. HTTP-specifikationen kräver kodning av de osäkra tecknen samt alla kontrolltecken, till exempel `<return>` och `<tab>`. URL-kodningen för ett tecken består av symbolen %, följt av den tvåsiffriga hexadecimala representationen (skiftlägesokänslig) av tecknets ISO-Latin-kodpunkt. De osäkra tecknen och kodpunkterna är:

<table id="table_D2C01CADB35E477D82D4C27586424625"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Osäkert tecken </th> 
   <th colname="col2" class="entry"> Kodpunkter (hex) </th> 
   <th colname="col3" class="entry"> Kodpunkter (dec) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Blanksteg </p> </td> 
   <td colname="col2"> <p>20 </p> </td> 
   <td colname="col3"> <p>32 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&lt; </p> </td> 
   <td colname="col2"> <p>3C </p> </td> 
   <td colname="col3"> <p>60 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&gt; </p> </td> 
   <td colname="col2"> <p>3E </p> </td> 
   <td colname="col3"> <p>62 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>" </p> </td> 
   <td colname="col2"> <p>22 </p> </td> 
   <td colname="col3"> <p>34 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p># </p> </td> 
   <td colname="col2"> <p>23 </p> </td> 
   <td colname="col3"> <p>35 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>% </p> </td> 
   <td colname="col2"> <p>25 </p> </td> 
   <td colname="col3"> <p>37 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&lbrace; </p> </td> 
   <td colname="col2"> <p>7B </p> </td> 
   <td colname="col3"> <p>123 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&rbrace; </p> </td> 
   <td colname="col2"> <p>7D </p> </td> 
   <td colname="col3"> <p>125 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>| </p> </td> 
   <td colname="col2"> <p>7C </p> </td> 
   <td colname="col3"> <p>124 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>\ </p> </td> 
   <td colname="col2"> <p>5C </p> </td> 
   <td colname="col3"> <p>92 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>^ </p> </td> 
   <td colname="col2"> <p>5E </p> </td> 
   <td colname="col3"> <p>94 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~ </p> </td> 
   <td colname="col2"> <p>7E </p> </td> 
   <td colname="col3"> <p>126 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&lbrack; </p> </td> 
   <td colname="col2"> <p>5B </p> </td> 
   <td colname="col3"> <p>91 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&rbrack; </p> </td> 
   <td colname="col2"> <p>5D </p> </td> 
   <td colname="col3"> <p>93 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&grave; </p> </td> 
   <td colname="col2"> <p>60 </p> </td> 
   <td colname="col3"> <p>96 </p> </td> 
  </tr> 
 </tbody> 
</table>

Reserverade tecken måste också kodas.

<table id="table_A6C808A05EA6420F8125186D3D5C9E33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Reserverat tecken </th> 
   <th colname="col2" class="entry"> Kodpunkter (hex) </th> 
   <th colname="col3" class="entry"> Kodpunkter (dec) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>$ </p> </td> 
   <td colname="col2"> <p>24 </p> </td> 
   <td colname="col3"> <p>36 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp; </p> </td> 
   <td colname="col2"> <p>26 </p> </td> 
   <td colname="col3"> <p>38 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+ </p> </td> 
   <td colname="col2"> <p>2B </p> </td> 
   <td colname="col3"> <p>43 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>, </p> </td> 
   <td colname="col2"> <p>2C </p> </td> 
   <td colname="col3"> <p>44 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>/ </p> </td> 
   <td colname="col2"> <p>2F </p> </td> 
   <td colname="col3"> <p>47 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>: </p> </td> 
   <td colname="col2"> <p>3A </p> </td> 
   <td colname="col3"> <p>58 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>; </p> </td> 
   <td colname="col2"> <p>3B </p> </td> 
   <td colname="col3"> <p>59 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>= </p> </td> 
   <td colname="col2"> <p>3D </p> </td> 
   <td colname="col3"> <p>61 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>? </p> </td> 
   <td colname="col2"> <p>3F </p> </td> 
   <td colname="col3"> <p>63 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>@ </p> </td> 
   <td colname="col2"> <p>40 </p> </td> 
   <td colname="col3"> <p>64 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-b85895e5b6a84b96b7fca987656dd34d}

`…&$text=rate&weight=85% 27#&…`

Om ingen förväxling används måste ovanstående begärandefragment kodas enligt följande:

`…&$text=rate%26weight%3D85%25%2027%23&…`

Om du använder obehörig kodning kan kodningen begränsas till att ta bort tecknen &#39;=&#39;, &#39;&amp;&#39; och &#39;%&#39;:

`…&$text=rate%26weight%3D85%25 27#&…`

## Se även {#section-295476ec34c74973962d07dfa9eb2180}

[Begärandebekräftelse](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [HTTP/1.1-specifikation (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
