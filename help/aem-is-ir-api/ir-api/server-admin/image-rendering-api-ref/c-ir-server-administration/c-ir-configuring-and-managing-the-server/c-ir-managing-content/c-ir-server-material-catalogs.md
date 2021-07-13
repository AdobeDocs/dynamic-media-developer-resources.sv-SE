---
description: Materialkataloger innehåller många konfigurationsinställningar för bildåtergivning.
solution: Experience Manager
title: Materialkataloger
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Materialkataloger{#material-catalogs}

Materialkataloger innehåller många konfigurationsinställningar för bildåtergivning.

Materialkataloger mappar vinjetter och material-ID som används i begäranden till faktiska filsökvägar, kan lagra alla metadata som är associerade med material och tillhandahålla behållare för mallar. De håller reda på ICC-profiler och kommandomakron.

Materialkataloger är bara tillgängliga för Java-komponenten i Image Rendering (tillsammans med Platform Server). Katalogattributfiler måste ha ett [!DNL .ini]-suffix och placeras i den registrerade katalogmappen ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Standardmaterialkatalogen ( [!DNL default.ini]) måste alltid finnas och måste fyllas i med alla attribut för att bildservern ska fungera korrekt.
