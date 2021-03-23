---
description: Innehåller inställningar för plattformsserver.
seo-description: Innehåller inställningar för plattformsserver.
seo-title: server.xml
solution: Experience Manager
title: server.xml
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
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

