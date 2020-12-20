---
description: Spelningsloggverktyget kan användas för att förgenerera innehåll för HTTP-svarscachen.
seo-description: Spelningsloggverktyget kan användas för att förgenerera innehåll för HTTP-svarscachen.
seo-title: Verktyget playlog
solution: Experience Manager
title: Verktyget playlog
topic: Scene7 Image Serving - Image Rendering API
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---


# Verktyget playlog{#the-playlog-utility}

Spelningsloggverktyget kan användas för att förgenerera innehåll för HTTP-svarscachen.

Den befintliga Image Serving HTTP-svarscachen är inte garanterat användbar efter en större versionsuppgradering (när den första eller andra siffran i versionsnumret ändras). Om servern ska tas direkt in i fulladdningsförhållanden efter uppgraderingen kan servern bli överbelastad med de första timmarna av cacheminnesbegäranden tills cacheminnet är någorlunda ifyllt och cachens träffhastighet ökar.

För att undvika den här inledande inläsningsökningen kan verktyget `playlog` användas för att förgenerera innehåll för HTTP-svarscachen. `playlog` extraherar HTTP-begäranden från en befintlig åtkomstloggfil och skickar den till servern för att generera cacheposter. För vanliga användningsscenarier räcker det att spela upp en enda åtkomstloggfil som innehåller trafikens hela dag.

Förutom att fylla i HTTP-svarscachen efter uppgraderingsinstallationer, används verktyget även för att förgenerera cacheinnehåll när en ny server läggs till i en belastningsutjämnad miljö. spela bara upp en nyligen använd loggfil från en av de andra servrarna.

`playlog` kan konfigureras för att stödja de flesta åtkomstloggfiler som genererats av tidigare versioner av Image Serving.

## Användning {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p  <span class="varname"> prefix  </span> </span> </p> </td> 
  <td class="stentry"> <p>Rot-URL som ska användas som prepend för begäranden som extraheras från loggfilen. </p> <p>Standard: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>Fältnummer (kolumn) som innehåller begäran i loggposten. 1-baserad. </p> <p>Standard: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s  <span class="varname"> avgränsare  </span> </span> </p> </td> 
  <td class="stentry"> <p>Fältavgränsare; reguljärt uttrycksmönster. </p> <p>Standard: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> markör  </span> </span> </p> </td> 
  <td class="stentry"> <p>Markör för begäran. identifierar förfrågningar i loggfilen som ska spelas upp, reguljärt uttrycksmönster. </p> <p>Standard: <span class="codeph"> Begäran: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x  <span class="varname"> suffix  </span> </span> </p> </td> 
  <td class="stentry"> <p>Tillägg till den begäran som extraherats ur loggfilen. kan användas för att skilja uppspelade begäranden från live-begäranden i loggfilerna, a '?' eller '&amp;'-avgränsare infogas automatiskt, suffixet kan referera till valfritt loggfält efter position inom klammerparentes, standardvärdet motsvarar signaturfältet md5. </p> <p>Standard: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v  </span> </p> </td> 
  <td class="stentry"> <p>I detaljerat läge skrivs de genererade URL:erna för begäran ut till <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>Skriv ut en synkronisering till <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r  </span> </p> </td> 
  <td class="stentry"> <p>request-method - HTTP-begärandemetod som ska användas ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Standard: <span class="codeph"> smart </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o  </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos in log file to capture original method from. </p> <p>Standard: 15 </p> </td> 
 </tr> 
</table>

För Windows är filnamnet [!DNL playlog.bat] och i Linux är det [!DNL playlog.sh].

## Exempel {#section-716e5c35e9fa4ee3a4b0687381fcea40}

I följande exempel spelas alla begäranden upp från en åtkomstloggfil som skapats av Image Serving i Linux:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

Följande kommando spelar upp alla begäranden som finns i en spårningsloggfil som skapats av Image Serving i Windows:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
