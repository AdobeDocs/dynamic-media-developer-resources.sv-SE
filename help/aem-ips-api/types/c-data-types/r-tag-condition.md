---
description: Definierar sökvillkor för taggfält.
seo-description: Definierar sökvillkor för taggfält.
seo-title: TaggCondition
solution: Experience Manager
title: TaggCondition
topic: Scene7 Image Production System API
uuid: c7727267-05b6-4011-9ddf-7f3134e9609b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# TagCondition{#tagcondition}

Definierar sökvillkor för taggfält.

Syntax

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Fälthandtag för tagg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3">Beroende på taggfältstypen och om värdet eller värdetArray-fältet används. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Om <span class="codeph">-värdet</span> skickas måste <span class="codeph"> op</span> vara strängkonstanten Matches. Villkoret matchar alla resurser som är associerade med taggvärdet. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Om <span class="codeph"> valueArray</span> skickas kan det översta fältet vara konstanten <span class="codeph"> MatchesAny</span> för antingen enkla eller flervärdiga taggfält. Ett <span class="codeph"> MatcharAny</span>-villkor matchar alla resurser som är associerade med minst ett av taggvärdena i <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">För flervärdesfält kan det översta fältet anges till konstanten <span class="codeph"> MatchesAll</span> med fältet <span class="codeph"> valueArray</span>. I det här fallet matchar villkoret bara resurser som är associerade med alla taggvärden i <span class="codeph"> valueArray</span> (eventuellt utöver andra taggvärden). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ett matchande värde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> Flera matchande värden. </td> 
  </tr> 
 </tbody> 
</table>

