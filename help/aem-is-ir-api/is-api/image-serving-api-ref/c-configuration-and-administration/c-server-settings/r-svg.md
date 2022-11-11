---
description: Inställningarna i det här avsnittet behöver bara beaktas om återgivning av SVG krävs.
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# SVG{#svg}

Inställningarna i det här avsnittet behöver bara beaktas om återgivning av SVG krävs.

## SV::SvgHeapSize - SVG Heap Size {#section-59ab17681daa4be8b5d794713e1a504e}

Java-stackstorleken för SVG Renderer. Standardvärdet är &quot;200m&quot; (200 MB).

## PS::svgProvider.rootPaths - rotmappar för SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Platsen för källdatafilerna i SVG. Kan vara en eller flera absoluta filsökvägar eller sökvägar i förhållande till *[!DNL install_folder]*, avgränsade med semikolon. Vanligtvis inställt på samma värde som `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - största filstorlek för SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Största filstorlek för källfilen SVG i kBytes. Servern returnerar ett fel när ett försök görs att återge en SVG-fil som är större än denna gräns. Standardvärdet är 1 024 kbit/s.

## IS::SvgMAxRenderRgnPixels - Storleksgräns för utdatamodell i SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Begränsar storleken på bilder som SVGRender kan producera. Heltalsvärde som är större än 0 i miljoner pixlar. Ett fel returneras om en återgivningsåtgärd skulle överskrida storleksgränsen. Standardvärdet är 4.

## PS::svgProvider.port - [!DNL Platform Server] Lyssnarport {#section-f7e42a96c2dd4523b46f0557c239e659}

Porten som används för SvgRender för att hämta bilder från [!DNL Platform Server] som ska bäddas in i SVG-renderingar.

Viktigt! För att SVGRender-komponenten ska fungera korrekt måste det här konfigurationsalternativet anges till samma värde som `TC::PsPort`.

## PS::svgProvider.fontRoot - SVG-mappen för teckensnittsfiler {#section-a8d45b0d68504945b8780f5eac351b0d}

Anger var SVgRender ska hitta de teckensnittsfiler som behövs för att återge SVG-text. oftast en av sökvägarna som anges i `IS::RootPaths`. Standardvärdet är [!DNL  *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Konfigurerar den port som Image Server och SVGRender-komponenten kommunicerar på.

>[!NOTE]
>
>För att SVGRender-komponenten ska fungera korrekt måste samma portnummer anges för `SVG::SVGRender.port` och `IS::SVGTcpPort`.
