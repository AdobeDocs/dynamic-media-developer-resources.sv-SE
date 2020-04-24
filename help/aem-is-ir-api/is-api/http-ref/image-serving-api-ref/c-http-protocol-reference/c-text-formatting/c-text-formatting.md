---
description: Image Serving innehåller flera alternativ för att återge text, som du kan använda med kommandona text= och textPs=.
seo-description: Image Serving innehåller flera alternativ för att återge text, som du kan använda med kommandona text= och textPs=.
seo-title: Textformatering
solution: Experience Manager
title: Textformatering
topic: Scene7 Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# Textformatering{#text-formatting}

Image Serving innehåller flera alternativ för att återge text, som du kan använda med kommandona text= och textPs=.

`textPs=` ger hög likhet med text som återges med Adobe Photoshop och Illustrator. `text=` är rimligen kompatibelt med text som återges med Windows Wordpad.

>[!NOTE]
>
>Förutom de skillnader som finns listade någon annanstans, `text=` skapas subtila skillnader i den återgivna texten när den jämförs med `textPs=`. Understrykningar har till exempel inte samma tjocklek och position och syntetiserad kursiv återgivning visas i en något annorlunda vinkel. Om texten inte får plats i det tillgängliga utrymmet kan den sista raden beskäras delvis, medan hela rader endast `text=` `textPs=` återges.

Alla textkommandon accepterar formaterad text som är baserad på en delmängd av RTF-specifikationen (Rich Text Format). Varje textlager kan ange ett eget textkommando.

I följande tabell visas de viktigaste funktionerna för varje textkommando:

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Funktion</b> </th> 
   <th class="entry"> <b> text=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Se även</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Photoshop-kompatibel </p> </td> 
   <td> <p> no </p> </td> 
   <td> <p> begränsad </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flöda text i godtyckliga former </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flöda text längs godtyckliga banor </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Kopia </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Copy-passning <p>, <pre>\textpassning</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Textrutemarginaler </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justering av hela stycken </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>justering av sista raden </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Styckeindrag </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Endast versaler och kapitäler </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Färger för bildhantering </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flera kantutjämningslägen </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>text uppifrån/ned/höger-vänster </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Stöd för Photofont® </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>ja </p> </td> 
   <td> Teckensnittshantering </td> 
  </tr> 
  <tr> 
   <td> <p>Anpassa lagrets storlek automatiskt till texten </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Stöd för CMYK </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Teckenflöde från höger till vänster </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Inaktivera automatisk radbrytning </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Skala text automatiskt så att den passar lagret (genom olika upplösning) </p> </td> 
   <td> <p>ja </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF-kompatibla strängar kan sättas samman manuellt eller genom att formatera texten i en textredigerare eller ordbehandlare som kan spara RTF-filer. RTF-filen kan sedan öppnas i en vanlig textredigerare och det aktuella RTF-innehållet i filen kopieras till begärande-URL:en.

Vissa ordbehandlare genererar ganska stora filer, som innehåller viktiga preambler som inte används av Scene7 Image Serving. Vi rekommenderar att du tar bort oanvända RTF-element från strängen innan du skickar strängen till textkommandona.

Språkkodning som bygger på UTF-8 och ISO-standarder stöds i RTF-strängar som ett alternativ till de vanliga RTF-teckenkodningsmekanismerna. Detta gör att program kan skicka icke-engelsk text till servern utan att känna till RTF-kodning.

Alla tecken som inte är HTTP-kompatibla måste escape-konverteras om strängen ska skickas via http. Endast &#39;=&#39;, &#39;&amp;&#39; och &#39;%&#39; behöver escape-konverteras om strängen är inkluderad i `catalog::Modifiers` fältet i en bildkatalogpost. Kontrolltecken, inklusive `<CR>`, `<LF>`och `<TAB>` ska alltid tas bort.

Textmotorerna i Image Serving tolkar en deluppsättning kommandon som definieras av RTF-specifikationen (Rich Text Format), version 1.6. Den här delmängden fokuserar på teckensnitt-/teckenformatering, enkel styckeformatering och stöd för internationella teckensnitt och teckenuppsättningar. Mer avancerade formateringskonstruktioner, som formatmallar och tabeller, stöds inte för närvarande.

Du måste känna till RTF-specifikationen (Rich Text Format) som har publicerats av Microsoft när du försöker konstruera RTF-kodade textsträngar manuellt.

* [Teckensnittshantering](r-font-handling.md)
* [Färghantering](r-color-handling.md)
* [Kopia](r-copy-fitting.md)
* [Textlager](r-text-layers.md)
* [Textplacering](r-text-positioning.md)
* [Reserverade tecken](r-reserved-characters.md)
* [RTF-kommandon och nyckelord som stöds](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Exempel på RTF-kodning](r-rtf-encoding-examples.md)
