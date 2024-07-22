---
description: Information om aktivitetens förlopp.
solution: Experience Manager
title: TaskProgress
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 35e3be1e-ccc2-460c-98c1-bbefab1df699
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# [!DNL TaskProgress]{#taskprogress}

Information om aktivitetens förlopp.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Beskrivning av uppgiftstyp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcsed </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Antal uppgiftsobjekt som redan har bearbetats. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Antal pågående uppgiftsobjekt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Antal väntande aktivitetsobjekt (ännu inte bearbetat). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progress </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> Förlopp i procent (intervall 0,0 - 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Progress message. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> När den senaste förloppsinformationen uppdaterades senast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Array med uppgiftsobjekt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Värdena är: 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Okänd</span>: När aktiviteten övervakar övergångar mellan lägen. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Nytt</span>: Aktivitetsövervakaren har skapats men har inte accepterat aktiviteter än. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Bearbetar</span>: Aktivitetsövervakaren bearbetar aktiviteter aktivt. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Stoppar</span>: Aktivitetsövervakaren stoppar ett jobb på grund av en begäran om stoppjobb. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Klar</span>: Jobb som tilldelats aktivitetsövervakningsjobb har slutförts. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> misslyckades</span>: Anger ett allvarligt fel. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
