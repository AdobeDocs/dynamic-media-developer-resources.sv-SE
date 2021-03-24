---
description: Datafiler för statisk innehållskälla är bara tillgängliga för plattformsservern.
solution: Experience Manager
title: Källdata för statiskt innehåll
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
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
