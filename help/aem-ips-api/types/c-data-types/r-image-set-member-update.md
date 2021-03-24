---
description: 'I den här typen är fältet pageReset användbart för bildresurstyperna RenderSet och Catalog '
solution: Experience Manager
title: ImageSetMemberUpdate
feature: Dynamic Media Classic,SDK/API,Bilduppsättningar
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# ImageSetMemberUpdate{#imagesetmemberupdate}

I den här typen är pageReset-fältet användbart för resurstyperna RenderSet och Catalog:

* För `RenderSet` anger `pageReset` starten för en ny renderingsvy/färgrutegrupp.

* För Katalog anger `pageReset` början på en ny sidvy. Vanligtvis finns det två sidbilder per sidvy, men du kan ha fler eller färre.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Resurshandtag i bilduppsättningens medlemsarray. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pageReset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3">Återställer sidan. <p>Inställningen ignoreras och värdet tvingas till true för <span class="codeph"> ImageSet</span> och <span class="codeph"> SpinSet</span>. </p></td> 
  </tr> 
 </tbody> 
</table>

