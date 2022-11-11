---
description: Datafiler för statisk innehållskälla är bara tillgängliga för [!DNL Platform Server].
solution: Experience Manager
title: Källdata för statiskt innehåll
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Källdata för statiskt innehåll{#static-content-source-data}

Datafiler för statisk innehållskälla är bara tillgängliga för [!DNL Platform Server].

Sökvägen för datafiler med statiskt innehåll tolkas på följande sätt:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Servern kombinerar sökvägssegment från höger till vänster tills en absolut filsökväg har upprättats.

Alla ` *[!DNL rootPath]*` segment kan vara tomma, relativa eller absoluta bansegment.

` *[!DNL catalogPath]*` är antingen en absolut eller relativ sökväg/filnamn. *[!DNL requestPath]* måste vara en relativ sökväg/ett relativt filnamn.

Flera `PS::staticContent.rootPaths` värden kan definieras i [!DNL PlatformServer.conf]. Detta gör att källdatafiler kan distribueras över flera filsystem. The [!DNL Platform Server] kommer att försöka med alternativa sökvägar i den ordning som anges tills datafilen hittas.
