---
description: Datafiler för statisk innehållskälla är bara tillgängliga för plattformsservern.
seo-description: Datafiler för statisk innehållskälla är bara tillgängliga för plattformsservern.
seo-title: Källdata för statiskt innehåll
solution: Experience Manager
title: Källdata för statiskt innehåll
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# Källdata för statiskt innehåll{#static-content-source-data}

Datafiler för statisk innehållskälla är bara tillgängliga för plattformsservern.

Sökvägen för datafiler med statiskt innehåll tolkas på följande sätt:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Servern kombinerar sökvägssegment från höger till vänster tills en absolut filsökväg har upprättats.

Alla ` *[!DNL rootPath]*`-segment kan vara tomma, relativa eller absoluta sökvägssegment.

` *[!DNL catalogPath]*` är antingen en absolut eller relativ sökväg/filnamn. *[!DNL requestPath]* måste vara en relativ sökväg/ett relativt filnamn.

Flera `PS::staticContent.rootPaths`-värden kan definieras i [!DNL PlatformServer.conf]. Detta gör att källdatafiler kan distribueras över flera filsystem. Plattformsservern försöker med alternativa sökvägar i den ordning som anges tills datafilen hittas.
