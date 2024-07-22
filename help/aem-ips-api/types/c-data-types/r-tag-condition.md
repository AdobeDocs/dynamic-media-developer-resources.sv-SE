---
description: Definierar sökvillkor för taggfält.
solution: Experience Manager
title: TaggCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# [!DNL TagCondition]{#tagcondition}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Fälthandtag för tagg. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Beroende på taggfältstypen och om värdet eller värdetArray-fältet används. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Om <span class="codeph">-värdet </span> skickas måste <span class="codeph"> op</span> vara strängkonstanten Matches. Villkoret matchar alla resurser som är associerade med taggvärdet. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Om <span class="codeph"> valueArray</span> skickas kan det översta fältet vara konstanten <span class="codeph"> MatchesAny</span> för ett- eller flervärdesfält. Ett <span class="codeph"> MatchesAny</span>-villkor matchar alla resurser som är associerade med minst ett av taggvärdena i <span class="codeph"> valueArray </span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">För flervärdesfält kan det översta fältet anges till konstanten <span class="codeph"> MatchesAll</span> med fältet <span class="codeph"> valueArray </span>. I det här fallet matchar villkoret bara resurser som är associerade med alla taggvärden i <span class="codeph"> valueArray </span> (eventuellt utöver andra taggvärden). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ett matchande värde. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:StringArray</span> </td> 
   <td colname="col3"> Flera matchande värden. </td> 
  </tr> 
 </tbody> 
</table>
