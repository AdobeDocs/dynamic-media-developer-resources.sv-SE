---
description: Alla konfigurationsfiler finns i install_folder/conf och kan redigeras med de flesta textredigerare. Servern kan behöva startas om för att ändringarna ska börja gälla.
seo-description: Alla konfigurationsfiler finns i install_folder/conf och kan redigeras med de flesta textredigerare. Servern kan behöva startas om för att ändringarna ska börja gälla.
seo-title: Serverkonfigurationsfiler
solution: Experience Manager
title: Serverkonfigurationsfiler
topic: Scene7 Image Serving - Image Rendering API
uuid: 02905b23-bbf3-4ae7-828d-915b22d8f167
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# Serverkonfigurationsfiler{#server-configuration-files}

Alla konfigurationsfiler finns i install_folder/conf och kan redigeras med de flesta textredigerare. Servern kan behöva startas om för att ändringarna ska börja gälla.

>[!NOTE]
>
>De flesta serverkonfigurationsfiler innehåller ytterligare egenskaper och värden som inte beskrivs i det här dokumentet. Sådana egenskaper är avsedda för intern serveranvändning och får inte ändras om inte Scene7 Tech Support särskilt anger det.

I det här dokumentet behandlas inställningar för följande konfigurationsfiler:

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Konfigurationsfil</b> </th> 
   <th class="entry"> <b>Beskrivning</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath"> SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>Konfiguration av Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Tomcat-konfiguration. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> PlatformServer.conf</span> </p> </td> 
   <td> <p>Konfiguration av plattformsserver. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>Katalogtjänstkonfiguration. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>Konfiguration av serverövervakning. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>Image Server-konfiguration. </p> </td> 
  </tr> 
 </tbody> 
</table>

Konfigurationsfilerna beskrivs mer ingående senare i det här dokumentet.
