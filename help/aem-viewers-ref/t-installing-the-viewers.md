---
description: Instruktioner för installation av Scene7 Viewer API.
seo-description: Instruktioner för installation av Scene7 Viewer API.
seo-title: Installera flera visningsprogram på samma server
solution: Experience Manager
title: Installera flera visningsprogram på samma server
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Installera flera visningsprogram på samma server{#installing-multiple-viewers-on-the-same-server}

Instruktioner för installation av Scene7 Viewer API.

Installera och testa Image Serving innan du installerar visningsprogrammen för Image Serving.

Kopiera IS Viewer-filerna till hårddisken och distribuera sedan `s7viewers.war` filen till `../ImageServing/webapps` katalogen. I dokumentationen för Image Serving finns instruktioner om hur du distribuerar, startar, stoppar och hanterar Image Server.

>[!NOTE]
>
>Det finns ingen uppgradering för visningsprogrammen för Image Serving. Adobe rekommenderar att du säkerhetskopierar alla befintliga visningsprogramkataloger för Scene7 innan du fortsätter med installationen.

**Installera visningsprogrammen på samma server**

1. Byt namn på visningsprogrammet .war till önskad kontext och distribuera filen till önskad plats.
1. Ange `this.isViewerRoot` parametern i `config.js`.
1. Öppna `config.js` i roten för den nya visningsprogrammappen.
1. Ange parametern `this.isViewerRoot = "/s7viewers"` till `s7viewers.war` filens kontext. Exempel, `"/s7viewers-4.0"`. Spara och stäng filen.
1. Spara filen och stäng den.
