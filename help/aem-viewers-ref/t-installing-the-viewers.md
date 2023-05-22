---
title: Installera flera Dynamic Media-visningsprogram på samma server
description: Instruktioner för installation av Dynamic Media Viewer API.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Installera flera visningsprogram på samma server{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Instruktioner för installation av API:t för visningsprogram i Dynamic Media.

Installera och testa Image Serving innan du installerar visningsprogrammen för Image Serving.

Kopiera IS Viewer-filerna till hårddisken och distribuera sedan `s7viewers.war` till `../ImageServing/webapps` katalog. I dokumentationen för Image Serving finns instruktioner om hur du distribuerar, startar, stoppar och hanterar Image Server.

>[!NOTE]
>
>Det finns ingen uppgradering för visningsprogrammen för Image Serving. Adobe rekommenderar att du säkerhetskopierar alla befintliga Dynamic Media-visningsprogram (s7viewers) innan du fortsätter med installationen.

**Så här installerar du flera visningsprogram på samma server:**

1. Byt namn på visningsprogrammet .war till önskad kontext och distribuera filen till önskad plats.
1. Ange `this.isViewerRoot` parameter in `config.js`.
1. Öppna `config.js` i roten för den nya visningsmappen.
1. Ange parameter `this.isViewerRoot = "/s7viewers"` mot bakgrund av `s7viewers.war` -fil. Till exempel: `"/s7viewers-4.0"`.
1. Spara filen och stäng den.
