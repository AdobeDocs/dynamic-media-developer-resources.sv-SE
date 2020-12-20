---
description: Bildåtergivningens källdatafiler innehåller vinjettfiler, materialfiler (bilder för repeterbara texturer och dekorationer samt skåp och fönster som täcker formatfiler) och ICC-profiler.
seo-description: Bildåtergivningens källdatafiler innehåller vinjettfiler, materialfiler (bilder för repeterbara texturer och dekorationer samt skåp och fönster som täcker formatfiler) och ICC-profiler.
seo-title: Källdata
solution: Experience Manager
title: Källdata
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# Källdata{#source-data}

Bildåtergivningens källdatafiler innehåller vinjettfiler, materialfiler (bilder för repeterbara texturer och dekorationer samt skåp och fönster som täcker formatfiler) och ICC-profiler.

Alla källdatafiler måste vara tillgängliga för den systemspecifika kodkomponenten för bildåtergivning (tillsammans med bildservern).

Om det finns en materialkatalog i katalogen kommer den fil som anges i materialkatalogen (med `vignette::Path`, `catalog::Path` eller `icc::ProfilePath`) att slås upp av återgivningsservern enligt följande:

* Om sökvägen är absolut används den som den är.
* Om sökvägen är relativ är den angiven med `catalog::RootPath` (från en namngiven materialkatalog).
* Om sökvägen är absolut används den. i annat fall har det prefixet `default::RootPath` (från standardkatalogen).
* Om sökvägen är absolut används den. I annat fall kombineras den med sökvägen som anges i [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Om sökvägen nu är absolut används den. I annat fall antas den vara relativ till [!DNL *[!DNL install_folder]*].

Om ingen bildkatalog är inblandad kombineras sökvägen med `default::RootPath` och bearbetas sedan enligt ovan.

Den fysiska platsen för källdatafiler anges vanligtvis med [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Flera värden kan anges för att tillåta att källdatafiler distribueras över flera filsystem. Återgivningsservern kommer att försöka med varje sökväg i den ordning som anges tills datafilen hittas.

Nya datafiler kan läggas till när som helst utan att servern stoppas.
