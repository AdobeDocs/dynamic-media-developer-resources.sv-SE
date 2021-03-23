---
description: Materialkataloger innehåller många konfigurationsinställningar för bildåtergivning.
seo-description: Materialkataloger innehåller många konfigurationsinställningar för bildåtergivning.
seo-title: Materialkataloger
solution: Experience Manager
title: Materialkataloger
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Materialkataloger{#material-catalogs}

Materialkataloger innehåller många konfigurationsinställningar för bildåtergivning.

Materialkataloger mappar vinjetter och material-ID som används i begäranden till faktiska filsökvägar, kan lagra alla metadata som är associerade med material och tillhandahålla behållare för mallar. De håller reda på ICC-profiler och kommandomakron.

Materialkataloger är bara tillgängliga för Java-komponenten i Image Rendering (tillsammans med Platform Server). Katalogattributfiler måste ha ett [!DNL .ini]-suffix och placeras i den registrerade katalogmappen ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Standardmaterialkatalogen ( [!DNL default.ini]) måste alltid finnas och måste fyllas i med alla attribut för att bildservern ska fungera korrekt.
