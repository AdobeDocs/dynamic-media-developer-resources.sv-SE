---
description: Tillåt direkt åtkomst till sökvägsbaserade resurser.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Tillåt direkt åtkomst till sökvägsbaserade resurser.

När det här attributet definieras tillåts eller begränsas sökvägsbaserad åtkomst för de angivna objekttyperna, beroende på om nyckelordet `include` eller `exclude` används.

>[!NOTE]
>
>Om attributet `AllowDirectAccess` inte anges är standardvärdet `exclude`.

* `include` tillåter åtkomst för de angivna objekttyperna och begränsar åtkomsten för alla andra.
* `exclude` begränsar åtkomsten för de angivna objekttyperna och tillåter åtkomst för alla andra.

Om varken `include` eller `exclude` anges antas `include`.

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

* Tillåt direktåtkomst för alla objekttyper utom `IS` och `STATIC` `AllowDirectAccess=exclude:IS,STATIC`

* Tillåt direktåtkomst för objekttyperna *no* (d.v.s. ingen)

  `AllowDirectAccess=include:`

* Tillåt direktåtkomst för *alla* objekttyper (d.v.s. exkludera ingen)

  `AllowDirectAccess=exclude:`

* Motsvarar `include:IS,STATIC` (om `include`/ `exclude` inte finns antas `include`)

  `AllowDirectAccess=IS,STATIC`

  Observera att det är standardvärdet som används om attributet `AllowDirectAccess` inte har angetts för det här företaget.

* Inkludera ingen, vilket motsvarar `include:` (om `include`/ `exclude` inte finns antas `include`)

  `AllowDirectAccess=`
