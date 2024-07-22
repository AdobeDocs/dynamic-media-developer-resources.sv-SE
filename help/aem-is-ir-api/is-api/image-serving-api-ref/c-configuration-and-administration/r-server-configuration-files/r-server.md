---
description: Innehåller inställningar för plattformsserver.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# server.xml{#server-xml}

Innehåller inställningar för plattformsserver.

När du ändrar den här XML-filen måste du se till att behålla giltig XML-syntax, annars kanske [!DNL Platform Server] inte kan startas.

För att ändringarna ska börja gälla måste [!DNL Platform Server] startas om efter att filen har redigerats.

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
