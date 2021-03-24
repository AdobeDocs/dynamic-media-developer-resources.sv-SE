---
description: I det här avsnittet beskrivs syntaxen för VNTC-användning.
solution: Experience Manager
title: Användning
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# Användning{#usage}

I det här avsnittet beskrivs syntaxen för VNTC-användning.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* är sökvägen och namnet på filen som ska bearbetas. Kan vara en relativ sökväg till den aktuella arbetskatalogen eller en absolut sökväg. Måste vara en giltig vinjett, ett skåp eller ett fönster som täcker formatfilen och ha något av följande suffix: [!DNL .vnt], [!DNL .vnc] eller [!DNL .vnw]. Obligatoriskt.

*[!DNL destFile]* är sökväg och namn för utdatavvignettningsfilen. Om inget anges placeras utdatafilen i den mapp som anges med `-destpath`. I det här fallet genereras filnamnet automatiskt från indatafilens namn och ett storlekssuffix, avgränsat med strängen som anges med `-separator`. För vinjetteringar är storlekssuffixet pixelbredden för den enupplösta utdatavvinjetteringen, bredden på den första vyn i en flerupplöst utdatavvinjett eller &quot;0&quot; för en pyramidvinjettering. För kabinettformatfiler används utdataupplösningen som filsuffix. *[!DNL destFile]* ignoreras när  `-info` anges.
