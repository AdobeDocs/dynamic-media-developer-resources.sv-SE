---
description: Information om aktivitetens förlopp.
seo-description: Information om aktivitetens förlopp.
seo-title: AktivitetFörlopp
solution: Experience Manager
title: AktivitetFörlopp
topic: Scene7 Image Production System API
uuid: b3b67803-147a-48a3-acc3-d608e01e0800
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AktivitetFörlopp{#taskprogress}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Beskrivning av uppgiftstyp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcsed</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Antal uppgiftsobjekt som redan har bearbetats. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Antal pågående uppgiftsobjekt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Antal väntande aktivitetsobjekt (ännu inte bearbetat). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> förlopp</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dubbel</span> </td> 
   <td colname="col3"> Förlopp i procent (intervall 0,0 - 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Förloppsmeddelande. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> När den senaste förloppsinformationen uppdaterades senast. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> typer:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Array med uppgiftsobjekt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3">Värdena är: 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Okänd</span>: När aktiviteten övervakar övergångar mellan lägen. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Nytt</span>: Uppgiftsövervakaren har skapats men har inte accepterat uppgifter än. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Bearbetar</span>: Aktivitetsövervakaren bearbetar aktivt uppgifter. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Stoppar</span>: Aktivitetsövervakaren stoppar ett jobb på grund av en begäran om att stoppa jobb. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Klart</span>: Jobb som tilldelats aktivitetsövervakarens jobb har slutförts. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> Misslyckades</span>: Anger ett allvarligt fel. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

