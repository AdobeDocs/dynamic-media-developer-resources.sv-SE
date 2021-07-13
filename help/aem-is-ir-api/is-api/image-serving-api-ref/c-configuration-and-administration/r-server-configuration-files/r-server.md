---
description: Innehåller inställningar för plattformsserver.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# server.xml{#server-xml}

Innehåller inställningar för plattformsserver.

När du ändrar den här XML-filen måste du se till att du upprätthåller giltig XML-syntax, annars kanske inte Platform Server startar.

För att ändringarna ska börja gälla måste plattformsservern startas om efter att filen har redigerats.

Följande diagram visar vilka inställningar som kan ändras i den här filen. I motsvarande avsnitt tidigare i det här dokumentet finns en beskrivning av de här inställningarna. Observera att det här diagrammet inte är en fullständig representation av [!DNL server.xml].

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```
