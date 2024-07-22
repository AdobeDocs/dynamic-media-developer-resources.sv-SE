---
description: I den här typen är fältet pageReset användbart för bildresurstyperna RenderSet och Catalog
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 4c598afb-a80c-4fac-997f-ef1c7175430c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# [!DNL ImageSetMemberUpdate]{#imagesetmemberupdate}

I den här typen är pageReset-fältet användbart för resurstyperna RenderSet och Catalog:

* För `RenderSet` anger `pageReset` början på en ny renderingsvy/färgrutegrupp.

* För katalog anger `pageReset` början på en ny sidvy. Vanligtvis finns det två sidbilder per sidvy, men du kan ha fler eller färre.

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Resurshandtag i bilduppsättningens medlemsarray. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3">Återställer sidan. <p>Inställningen ignoreras och värdet tvingas till true för <span class="codeph"> ImageSet </span> och <span class="codeph"> SpinSet </span>. </p></td> 
  </tr> 
 </tbody> 
</table>
