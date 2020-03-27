---
description: Inställningarna i det här avsnittet behöver bara beaktas om SVG-återgivning krävs.
seo-description: Inställningarna i det här avsnittet behöver bara beaktas om SVG-återgivning krävs.
seo-title: SVG
solution: Experience Manager
title: SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SVG{#svg}

Inställningarna i det här avsnittet behöver bara beaktas om SVG-återgivning krävs.

## SV::SvgHeapSize - SVG-heap-storlek {#section-59ab17681daa4be8b5d794713e1a504e}

Java-heap-storleken för SVG-renderaren. Standardvärdet är &quot;200m&quot; (200 MB).

## PS::svgProvider.rootPaths - SVG-datarotmappar {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Sökvägen för SVG-källdatafilerna. Kan vara en eller flera absoluta filsökvägar eller sökvägar i förhållande till *[!DNL install_folder]*, avgränsade med semikolon. Vanligtvis inställt på samma värde som `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - maximal SVG-filstorlek {#section-b9c81e3e104642ebbdd9f000843d3256}

Största storlek på SVG-källfil i kBytes. Servern returnerar ett fel när ett försök görs att återge en SVG-fil som är större än denna gräns. Standardvärdet är 1 024 kbit/s.

## IS::SvgMAxRenderRgnPixels - Storleksgräns för SVG-utdatabild {#section-5be1fd9639424d878a5ffd11736d3920}

Begränsar storleken på bilder som SVGRender kan producera. Heltalsvärde som är större än 0 i miljoner pixlar. Ett fel returneras om en återgivningsåtgärd skulle överskrida storleksgränsen. Standardvärdet är 4.

## PS::svgProvider.port - avlyssningsport för plattformsserver {#section-f7e42a96c2dd4523b46f0557c239e659}

Den port som används för SVgRender för att hämta bilder från plattformsservern som ska bäddas in i SVG-återgivningar.

Viktigt För att SVGRender-komponenten ska fungera korrekt måste det här konfigurationsalternativet anges till samma värde som `TC::PsPort`.

## PS::svgProvider.fontRoot - mappen SVG-teckensnittsfiler {#section-a8d45b0d68504945b8780f5eac351b0d}

Anger var SVgRender ska hitta de teckensnittsfiler som behövs för att återge SVG-text. oftast en av sökvägarna som anges i `IS::RootPaths`. Standardvärdet är [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Konfigurerar den port som Image Server och SVGRender-komponenten kommunicerar på.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>För att SVGRender-komponenten ska fungera korrekt måste samma portnummer anges för `SVG::SVGRender.port` och `IS::SVGTcpPort`.

