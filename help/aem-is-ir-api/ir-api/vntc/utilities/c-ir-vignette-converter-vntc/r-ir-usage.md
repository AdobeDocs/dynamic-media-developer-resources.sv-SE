---
title: Användning
description: I det här avsnittet beskrivs syntaxen för användning av vntc.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Användning{#usage}

I det här avsnittet beskrivs syntaxen för användning av vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* är sökvägen och namnet på filen som ska bearbetas. Det kan vara en relativ sökväg till den aktuella arbetskatalogen eller en absolut sökväg. Den måste vara en giltig vinjett, ett skåp eller ett fönster som täcker formatfilen och ha något av följande suffix:

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

Obligatoriskt.

*[!DNL destFile]* är sökväg och namn för utdatavvignettningsfilen. Om inget anges placeras utdatafilen i den mapp som anges med `-destpath`. I det här fallet genereras filnamnet automatiskt från indatafilens namn och ett storlekssuffix, avgränsat med strängen som anges med `-separator`. För vinjetteringar är storlekssuffixet pixelbredden för den enupplösta utdatavvinjetteringen, bredden på den första vyn i en flerupplöst utdatavvinjett eller &quot;0&quot; om det finns en pyramidvinjettering. För kabinettformatfiler används utdataupplösningen som filsuffix. *[!DNL destFile]* ignoreras när `-info` har angetts.
