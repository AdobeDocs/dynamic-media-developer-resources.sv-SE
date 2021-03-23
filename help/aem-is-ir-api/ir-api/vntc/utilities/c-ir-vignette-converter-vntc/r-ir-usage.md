---
description: I det här avsnittet beskrivs syntaxen för VNTC-användning.
seo-description: I det här avsnittet beskrivs syntaxen för VNTC-användning.
seo-title: Användning
solution: Experience Manager
title: Användning
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# Användning{#usage}

I det här avsnittet beskrivs syntaxen för VNTC-användning.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* är sökvägen och namnet på filen som ska bearbetas. Kan vara en relativ sökväg till den aktuella arbetskatalogen eller en absolut sökväg. Måste vara en giltig vinjett, ett skåp eller ett fönster som täcker formatfilen och ha något av följande suffix: [!DNL .vnt], [!DNL .vnc] eller [!DNL .vnw]. Obligatoriskt.

*[!DNL destFile]* är sökväg och namn för utdatavvignettningsfilen. Om inget anges placeras utdatafilen i den mapp som anges med `-destpath`. I det här fallet genereras filnamnet automatiskt från indatafilens namn och ett storlekssuffix, avgränsat med strängen som anges med `-separator`. För vinjetteringar är storlekssuffixet pixelbredden för den enupplösta utdatavvinjetteringen, bredden på den första vyn i en flerupplöst utdatavvinjett eller &quot;0&quot; för en pyramidvinjettering. För kabinettformatfiler används utdataupplösningen som filsuffix. *[!DNL destFile]* ignoreras när  `-info` anges.
