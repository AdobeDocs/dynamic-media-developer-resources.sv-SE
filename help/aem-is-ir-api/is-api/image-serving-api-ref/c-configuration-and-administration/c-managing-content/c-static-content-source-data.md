---
description: Datafiler för statisk innehållskälla är bara tillgängliga för plattformsservern.
seo-description: Datafiler för statisk innehållskälla är bara tillgängliga för plattformsservern.
seo-title: Källdata för statiskt innehåll
solution: Experience Manager
title: Källdata för statiskt innehåll
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Källdata för statiskt innehåll{#static-content-source-data}

Datafiler för statisk innehållskälla är bara tillgängliga för plattformsservern.

Sökvägen för datafiler med statiskt innehåll tolkas på följande sätt:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Servern kombinerar sökvägssegment från höger till vänster tills en absolut filsökväg har skapats.

Alla ` *[!DNL rootPath]*` segment kan vara tomma, relativa eller absoluta bansegment.

` *[!DNL catalogPath]*` är antingen en absolut eller relativ sökväg/filnamn. *[!DNL requestPath]* måste vara en relativ sökväg/ett relativt filnamn.

Flera `PS::staticContent.rootPaths` värden kan definieras i [!DNL PlatformServer.conf]. Detta gör att källdatafiler kan distribueras över flera filsystem. Plattformsservern försöker med alternativa sökvägar i den ordning som anges tills datafilen hittas.
