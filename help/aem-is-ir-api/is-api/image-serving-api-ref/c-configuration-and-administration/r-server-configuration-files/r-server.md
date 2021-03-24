---
description: Innehåller inställningar för plattformsserver.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
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

