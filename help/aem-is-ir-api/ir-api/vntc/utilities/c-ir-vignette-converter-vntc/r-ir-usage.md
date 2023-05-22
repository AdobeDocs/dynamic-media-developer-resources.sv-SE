---
description: I det här avsnittet beskrivs syntaxen för VNTC-användning.
solution: Experience Manager
title: Användning
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# Användning{#usage}

I det här avsnittet beskrivs syntaxen för VNTC-användning.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* är sökvägen och namnet på filen som ska bearbetas. Kan vara en relativ sökväg till den aktuella arbetskatalogen eller en absolut sökväg. Måste vara en giltig vinjett, ett skåp eller ett fönster som täcker formatfilen och ha något av följande suffix: [!DNL .vnt], [!DNL .vnc], eller [!DNL .vnw]. Obligatoriskt.

*[!DNL destFile]* är sökväg och namn för utdatavvignettningsfilen. Om inget anges placeras utdatafilen i den mapp som anges med `-destpath`. I det här fallet genereras filnamnet automatiskt från indatafilens namn och ett storlekssuffix, avgränsat med strängen som anges med `-separator`. För vinjetteringar är storlekssuffixet pixelbredden för den enupplösta utdatavvinjetteringen, bredden på den första vyn i en flerupplöst utdatavvinjett eller &quot;0&quot; för en pyramidvinjettering. För kabinettformatfiler används utdataupplösningen som filsuffix. *[!DNL destFile]* ignoreras när `-info` har angetts.
