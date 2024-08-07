---
title: Serverkonfigurationsfiler
description: Alla konfigurationsfiler finns i install_folder/conf och kan redigeras med de flesta textredigerare. Starta om servern för att ändringarna ska börja gälla.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Serverkonfigurationsfiler{#server-configuration-files}

Alla konfigurationsfiler finns i `install_folder/conf` och kan redigeras med de flesta textredigerare. Starta om servern för att ändringarna ska börja gälla.

>[!NOTE]
>
>De flesta serverkonfigurationsfiler innehåller ytterligare egenskaper och värden som inte beskrivs i det här dokumentet. Sådana egenskaper är avsedda för intern serveranvändning och får inte ändras om inte Dynamic Media tekniska support ger anvisningar om det.

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
   <td> <p>[!DNL Platform Server] konfiguration. </p> </td> 
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
