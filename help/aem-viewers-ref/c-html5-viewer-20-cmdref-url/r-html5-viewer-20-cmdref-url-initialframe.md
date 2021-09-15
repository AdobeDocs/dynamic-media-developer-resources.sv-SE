---
title: initialFrame
description: Parametern är gemensam för alla visningsprogram.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 1%

---

# initialFrame{#initialframe}

Parametern är gemensam för alla visningsprogram.

>[!NOTE]
>
>Det här kommandot gäller inte för Video Image Viewer.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Anger ett nollbaserat bildruteindex som visas när visningsprogrammet läses in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Ett nollbaserat index för sidan i uppslaget när enheten är stående. För en"vänster-till-höger"-miljö betyder <span class="codeph"> 0</span>"vänster sida" och <span class="codeph"> 1</span>"höger sida". För en"höger till vänster"-miljö är det motsatt: <span class="codeph"> 0</span> betyder "högersida" och <span class="codeph"> 1</span> betyder "vänstersida". </p> <p>Om inget anges används <span class="codeph"> 0</span> som standard. Ignoreras när enheten är i liggande orientering. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-10ee45d637134e0fbcd943c62578cb78}

Valfritt.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Ingen standard.

## Exempel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
