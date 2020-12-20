---
description: Vidarebefordrar den angivna listan med URL:er till Scene7 CDN-leverantören (Content Distribution Network) för att ogiltigförklara deras befintliga cache för HTTP-svar.
seo-description: Vidarebefordrar den angivna listan med URL:er till Scene7 CDN-leverantören (Content Distribution Network) för att ogiltigförklara deras befintliga cache för HTTP-svar.
seo-title: cdnCacheInvalidation
solution: Experience Manager
title: cdnCacheInvalidation
topic: Scene7 Image Production System API
uuid: 16cf53d4-4101-405c-b008-009b6ac62169
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Vidarebefordrar den angivna listan med URL:er till Scene7 CDN-leverantören (Content Distribution Network) för att ogiltigförklara deras befintliga cache för HTTP-svar.

## cdnCacheInvalidation: Om {#section-4f70d2bc79d64288b961836ab17e9690}

Cacheogiltigförklaring av CDN tvingar alla HTTP-begäranden för dessa URL:er att valideras mot aktuella publicerade data i Scene7-nätverket när denna invalideringsbegäran bearbetas via CDN-nätverket. Alla URL:er som inte är anslutna till Scene7 tjänst-URL-struktur och som direkt matchar Scene7 företags rot-ID som tilldelats när företaget skapas, resulterar i ett API-fel för hela begäran. Om det finns ogiltiga URL:er som CDN inte stöder och som den anser vara ogiltiga resulterar detta även i ett API-fel för hela begäran.

**Användningsfrekvens: Regler**

Reglerna för hur ofta denna funktion ska användas regleras av Scene7 CDN-partners. CDN behåller sin frihet att försämra svarstiden för dessa ogiltigförklaringar för att behålla optimala prestanda för tjänsten för användarna. Om Scene7 får ett meddelande om överanvändning av funktionen måste vi ta till vara att inaktivera funktionen antingen per företag eller helt i tjänsten.

**Bekräftelsemejl**

Bekräftelsemeddelanden från Scene7 CDN-partnern kan skickas till den som skapat listan eller upp till fem andra e-postadresser. API:t skickar en bekräftelse när hela CDN-nätverket har underrättats om att URL:erna som refereras i e-postmeddelandet har rensats. Ett enda anrop till `cdnCacheInvalidation` kan skicka flera e-postmeddelanden om antalet URL:er som anges överstiger det antal som Scene7 kan leverera till CDN-partnern i ett enda meddelande. Detta skulle för närvarande vara om begäran överskrider 100 URL:er, men kan ändras på begäran av CDN-partnern.

**Stöds sedan**

6.0

## Auktoriserade användartyper {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parametrar {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** (  `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Namn</b> </th> 
   <th class="entry"> <b> Typ</b> </th> 
   <th class="entry"> <b> Obligatoriskt</b> </th> 
   <th class="entry"> <b> Beskrivning</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:sträng</span> </p> </td> 
   <td> <p> Ja </p> </td> 
   <td> <p> Handtaget till företaget som är kopplat till URL:erna som ska ogiltigförklaras. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> typer:UrlArray</span> </p> </td> 
   <td> <p> Ja </p> </td> 
   <td> <p> Lista med upp till 1 000 URL:er som ska göras ogiltiga från CDN-cachen. Alla URL:er måste innehålla Scene7-företagets rot-ID för att kunna ogiltigförklaras. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**(  `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Namn</b> </th> 
   <th class="entry"> <b> Typ</b> </th> 
   <th class="entry"> <b> Obligatoriskt</b> </th> 
   <th class="entry"> <b> Beskrivning</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>En referens som refererar till rensningsbegäran. </p> <p>API:t <span class="codeph"> cdnCacheInvalidation</span> gör nu cacheminnet nästan omedelbart ogiltigt (~5 sekunder). Därför behövs vanligtvis inte längre avsökning för ogiltigförklaring. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> measuredSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Beräknade sekunder för slutförande av rensningsbegäran. Klienter bör vänta den här tiden innan avsökningsstatus. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-f414361a58e84dfcbbac30a358d02125}

I det här exemplet begärs fyra URL:er som ska ogiltigförklaras i CDN-cachen. Svaret innehåller en sammanfattning av om åtgärderna har slutförts och en lista med felinformation som har skickats direkt från CDN för att hjälpa klienten att använda den här funktionen.

`getCdnCacheInvalidationStatus` operation.

**Begäran**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**Svar**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```

