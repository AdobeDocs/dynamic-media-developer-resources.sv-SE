---
description: Tillåt direkt åtkomst till sökvägsbaserade resurser.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Tillåt direkt åtkomst till sökvägsbaserade resurser.

När det här attributet är definierat tillåts eller begränsas sökvägsbaserad åtkomst för de angivna objekttyperna, beroende på om `include` eller `exclude` nyckelord används.

>[!NOTE]
>
>Om `AllowDirectAccess` inget attribut har angetts, standardvärdet är `exclude`.

* `include` ger åtkomst till de angivna objekttyperna och begränsar åtkomsten för alla andra.
* `exclude` begränsar åtkomsten för de angivna objekttyperna och tillåter åtkomst för alla andra.

Om ingen `include` eller `exclude` anges, `include` antas.

Följande typer kan kontrolleras:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Exempel {#section-4c3765ebaa4245a799b454fc196f9237}

* Tillåt endast direktåtkomst för `IS` och `STATIC` objekttyper

   `AllowDirectAccess=include:IS,STATIC`

* Tillåt direktåtkomst för alla objekttyper utom `IS` och `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Tillåt direktåtkomst för *no* objekttyper (d.v.s. include none)

   `AllowDirectAccess=include:`

* Tillåt direktåtkomst för *alla* objekttyper (d.v.s. exkludera ingen)

   `AllowDirectAccess=exclude:`

* Motsvarar `include:IS,STATIC` (om `include`/ `exclude` inte finns, `include` antas)

   `AllowDirectAccess=IS,STATIC`

   Observera att det är standardvärdet som används om `AllowDirectAccess` inget attribut har angetts för det här företaget.

* Inkludera ingen, motsvarar `include:` (om `include`/ `exclude` inte finns, `include` antas)

   `AllowDirectAccess=`
