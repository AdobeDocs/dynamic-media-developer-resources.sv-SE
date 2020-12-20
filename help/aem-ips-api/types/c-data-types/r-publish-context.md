---
description: Definierar ett publiceringsmål för ett företag.
seo-description: Definierar ett publiceringsmål för ett företag.
seo-title: PublishContext
solution: Experience Manager
title: PublishContext
topic: Scene7 Image Production System API
uuid: 62e2ba15-d966-48c7-86dc-373069c3ea46
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# PublishContext{#publishcontext}

Definierar ett publiceringsmål för ett företag.

Syntax

## Parametrar {#section-577d46cc75774c7c8fbdcff203a0d9ac}

Resurserna har en separat markör för varje publiceringsläge och kontext. Ange publiceringstillståndet med [setAssetsContextState](../../operations/c-operations-intro/c-methods/r-set-asset-context-state.md#reference-da96f9caef734f2883fddaf58cd886d7).

<table id="table_1165D5DDC89140CD8222E5A04B39048E">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Namn </th>
   <th colname="col2" class="entry"> Typ </th>
   <th colname="col3" class="entry"> Beskrivning </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextHandle</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:sträng </span></td>
   <td colname="col3"> Hantera publiceringskontexten. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextName</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:sträng</span></td>
   <td colname="col3"> Namnet på publiceringskontexten. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextType</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:sträng</span></td>
   <td colname="col3">Typ av publiceringskontext. Innehåller: 
    <ul id="ul_04CA7C755E5441AA8ABBD0BA3F245A78">
     <li id="li_7F578422D38E40D1A590AB21ADD84E90"><span class="codeph"> ImageServing</span></li>
     <li id="li_C112E12028E44ED7914ED0D3D6B3A45E"><span class="codeph"> ImageRendering</span></li>
     <li id="li_9430D600FA4343F6951F9AE8EA7F9530"><span class="codeph"> Video</span></li>
     <li id="li_4122D853BE1B4ED3B412CFA7B659EB1D"><span class="codeph"> ServerDirectory</span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [Publicera kontext](../../string-constants/c-string-constants/r-publish-context.md#reference-3ade116df0df40deb86154eb0ac7c12a)

