---
title: Installera flera Dynamic Media-visningsprogram på samma server
description: Instruktioner för installation av Dynamic Media Viewer API.
solution: Experience Manager
feature: Dynamic Media Classic,visningsprogram,SDK/API
role: Utvecklare,Affärsledare
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
translation-type: tm+mt
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---

# Installera flera visningsprogram på samma server{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instruktioner för installation av API:t för visningsprogram i Dynamic Media.

Installera och testa Image Serving innan du installerar visningsprogrammen för Image Serving.

Kopiera IS Viewer-filerna till hårddisken och distribuera sedan `s7viewers.war`-filen till `../ImageServing/webapps`-katalogen. I dokumentationen för Image Serving finns instruktioner om hur du distribuerar, startar, stoppar och hanterar Image Server.

>[!NOTE]
>
>Det finns ingen uppgradering för visningsprogrammen för Image Serving. Adobe rekommenderar att du säkerhetskopierar alla befintliga Dynamic Media-visningsprogram (s7viewers) innan du fortsätter med installationen.

**Så här installerar du flera visningsprogram på samma server:**

1. Byt namn på visningsprogrammet .war till önskad kontext och distribuera filen till önskad plats.
1. Ange parametern `this.isViewerRoot` i `config.js`.
1. Öppna `config.js` i roten för den nya visningsprogrammappen.
1. Ange parametern `this.isViewerRoot = "/s7viewers"` i kontexten för filen `s7viewers.war`. Exempel, `"/s7viewers-4.0"`.
1. Spara filen och stäng den.
