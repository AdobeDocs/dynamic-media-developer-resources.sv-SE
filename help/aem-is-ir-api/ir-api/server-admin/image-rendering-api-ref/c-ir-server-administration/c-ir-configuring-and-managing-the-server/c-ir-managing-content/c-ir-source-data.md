---
description: Bildåtergivningens källdatafiler innehåller vinjettfiler, materialfiler (bilder för repeterbara texturer och dekorationer samt skåp och fönster som täcker formatfiler) och ICC-profiler.
solution: Experience Manager
title: Källdata
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Källdata{#source-data}

Bildåtergivningens källdatafiler innehåller vinjettfiler, materialfiler (bilder för repeterbara texturer och dekorationer samt skåp och fönster som täcker formatfiler) och ICC-profiler.

Alla källdatafiler måste vara tillgängliga för den systemspecifika kodkomponenten för bildåtergivning (tillsammans med bildservern).

Om en materialkatalog ingår, den fil som anges i materialkatalogen (med `vignette::Path`, `catalog::Path`, eller `icc::ProfilePath`) slås upp av Renderingsservern enligt följande:

* Om sökvägen är absolut används den som den är.
* Om sökvägen är relativ är den prefix med `catalog::RootPath` (från en namngiven materialkatalog).
* Om sökvägen är absolut används den, i annat fall anges den med prefixet `default::RootPath` (från standardkatalogen).
* Om sökvägen är absolut används den, annars kombineras den med sökvägen som anges i [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Om sökvägen nu är absolut används den, annars antas den vara relativ till [!DNL  *[!DNL install_folder]*].

Om ingen bildkatalog är inblandad kombineras sökvägen med `default::RootPath` och bearbetas enligt ovan.

Den fysiska platsen för källdatafiler anges vanligtvis med [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). Flera värden kan anges för att tillåta att källdatafiler distribueras över flera filsystem. Återgivningsservern testar varje sökväg i den ordning som anges tills datafilen hittas.

Nya datafiler kan läggas till när som helst utan att servern stoppas.
