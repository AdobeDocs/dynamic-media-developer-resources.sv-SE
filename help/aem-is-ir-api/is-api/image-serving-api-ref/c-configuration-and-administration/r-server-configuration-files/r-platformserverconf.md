---
description: Innehåller [!DNL Platform Server] inställningar.
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# PlatformServer.conf{#platformserver-conf}

Innehåller [!DNL Platform Server] inställningar.

Filen är en JAVA-egenskapsfil. Du måste iaktta försiktighet för att följa lämpliga konventioner. Annars kanske [!DNL Platform Server] inte kan startas. Använd ett dubbelt omvänt snedstreck (\\) eller ett enkelt snedstreck (/) i stället för ett omvänt snedstreck (\) i Windows-filsökvägar. Det omvända snedstrecket används som ett escape-tecken i den här filtypen.

Ändringarna i den här filen börjar gälla när filen har sparats.

Endast inställningarna nedan kan ändras i [!DNL PlatformServer.conf]. Om en viss inställning saknas kan den läggas till var som helst i filen. Endast en instans av varje inställning kan finnas.

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Allmänna inställningar för [!DNL Platform Server] </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEnentries=1000000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequsts=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Konfiguration av cachekluster </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Omdirigeringskonfiguration för fel </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVG-konfiguration </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./images </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> svgProvider.port=8080 </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./images </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Medieuppsättningssvar </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10 </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20 </span> </p> </td> 
 </tr> 
</table>
