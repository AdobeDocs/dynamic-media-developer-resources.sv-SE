---
description: Spelningsloggverktyget kan användas för att förgenerera innehåll för HTTP-svarscachen.
solution: Experience Manager
title: Verktyget playlog
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Verktyget playlog{#the-playlog-utility}

Spelningsloggverktyget kan användas för att förgenerera innehåll för HTTP-svarscachen.

Den befintliga Image Serving HTTP-svarscachen är inte garanterat användbar efter en större versionsuppgradering (när den första eller andra siffran i versionsnumret ändras). Om servern ska tas direkt in i fulladdningsförhållanden efter uppgraderingen kan servern bli överbelastad med de första timmarna av cacheminnesbegäranden tills cacheminnet är någorlunda ifyllt och cachens träffhastighet ökar.

För att undvika den här inledande inläsningsökningen kan verktyget `playlog` användas för att förgenerera innehåll för HTTP-svarscachen. `playlog` extraherar HTTP-begäranden från en befintlig åtkomstloggfil och skickar den till servern för att generera cacheposter. För vanliga användningsscenarier räcker det att spela upp en enda åtkomstloggfil som innehåller trafikens hela dag.

Förutom att fylla i HTTP-svarscachen efter uppgraderingsinstallationer används verktyget även för att generera cacheinnehåll i förväg när en ny server läggs till i en belastningsutjämnad miljö. Du behöver bara spela upp en nyligen använd loggfil från en av de andra servrarna.

`playlog` kan konfigureras med stöd för de flesta åtkomstloggfiler som genererats av tidigare versioner av Image Serving.

## Användning {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> prefix </span> </span> </p> </td> 
  <td class="stentry"> <p>Rot-URL som ska användas som prepend för begäranden som extraheras från loggfilen. </p> <p>Standard: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> col </span> </span> </p> </td> 
  <td class="stentry"> <p>Fältnummer (kolumn) som innehåller begäran i loggposten, 1-baserat. </p> <p>Standard: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> separator </span> </span> </p> </td> 
  <td class="stentry"> <p>Fältavgränsare; mönster för reguljära uttryck. </p> <p>Standard: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> markör </span> </span> </p> </td> 
  <td class="stentry"> <p>Begärandemarkör; identifierar begäranden i loggfilen som ska spelas upp; mönster för reguljära uttryck. </p> <p>Standard: <span class="codeph"> Begäran: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> suffix </span> </span> </p> </td> 
  <td class="stentry"> <p>Det suffix som ska läggas till i den begäran som extraheras från loggfilen. Det kan användas för att separera uppspelningsbegäranden från live-begäranden i loggfilerna. Ett ? eller '&amp;'-avgränsaren infogas automatiskt. Suffixet kan referera till valfritt loggfält efter position inom klammerparentes, standardvärdet motsvarar signaturfältet i md5. </p> <p>Standard: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>I detaljerat läge skrivs de genererade begärande-URL:erna ut till <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>Skriv ut en synkronisering till <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method - HTTP-begärandemetod som ska användas ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Standard: <span class="codeph"> smart </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos in log file to capture original method from. </p> <p>Standard: 15 </p> </td> 
 </tr> 
</table>

För Windows är filnamnet [!DNL playlog.bat] och i Linux är det [!DNL playlog.sh].

## Exempel {#section-716e5c35e9fa4ee3a4b0687381fcea40}

I följande exempel spelas alla begäranden upp från en åtkomstloggfil som skapats av Image Serving i Linux:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

Följande kommando spelar upp alla begäranden som finns i en spårningsloggfil som har skapats av Image Serving i Windows:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
