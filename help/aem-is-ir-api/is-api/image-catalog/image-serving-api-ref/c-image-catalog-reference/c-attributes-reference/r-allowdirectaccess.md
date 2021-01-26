---
description: Tillåt direkt åtkomst till sökvägsbaserade resurser.
seo-description: Tillåt direkt åtkomst till sökvägsbaserade resurser.
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

Tillåt direkt åtkomst till sökvägsbaserade resurser.

När det här attributet definieras tillåts eller begränsas sökvägsbaserad åtkomst för de angivna objekttyperna, beroende på om nyckelordet `include` eller `exclude` används.

>[!NOTE]
>
>Om attributet `AllowDirectAccess` inte anges är standardvärdet `exclude`.

* `include` ger åtkomst till de angivna objekttyperna och begränsar åtkomsten för alla andra.
* `exclude` begränsar åtkomsten för de angivna objekttyperna och tillåter åtkomst för alla andra.

Om varken `include` eller `exclude` har angetts antas `include`.

Följande typer kan kontrolleras:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Exempel {#section-4c3765ebaa4245a799b454fc196f9237}

* Tillåt endast direktåtkomst för objekttyperna `IS` och `STATIC`

   `AllowDirectAccess=include:IS,STATIC`

* Tillåt direktåtkomst för alla objekttyper utom `IS` och `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Tillåt direktåtkomst för *inga* objekttyper (d.v.s. inga)

   `AllowDirectAccess=include:`

* Tillåt direktåtkomst för *alla* objekttyper (d.v.s. exkludera ingen)

   `AllowDirectAccess=exclude:`

* Motsvarar `include:IS,STATIC` (om `include`/ `exclude` inte finns antas `include`)

   `AllowDirectAccess=IS,STATIC`

   Observera att är standardvärdet som används om attributet `AllowDirectAccess` inte har angetts för det här företaget.

* Inkludera ingen, vilket motsvarar `include:` (om `include`/ `exclude` inte finns, antas `include`)

   `AllowDirectAccess=`

