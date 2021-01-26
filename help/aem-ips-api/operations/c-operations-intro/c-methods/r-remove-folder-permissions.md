---
description: Tar bort mappbehörigheter.
seo-description: Tar bort mappbehörigheter.
seo-title: removeFolderPermissions
solution: Experience Manager
title: removeFolderPermissions
topic: Dynamic Media Image Production System API
uuid: cd9f7a42-e314-4ec9-abe2-a27581c7cd23
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---


# removeFolderPermissions{#removefolderpermissions}

Tar bort mappbehörigheter.

Syntax

## Auktoriserade användartyper {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-7efa68377fd846219b906d354ae64ed3}

**Indata (removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Obligatoriskt </th> 
   <th colname="col4" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Referensen till företaget med mappar med behörigheter som du vill ta bort. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Hantera till mappen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>När <span class="codeph"> är true</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">Borttagning av behörigheter sprids genom alla mappbehörighetsåtgärder. </li> 
     </ul> </p> <p>När <span class="codeph"> är false</span>: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">Åtgärden påverkar endast den angivna mappen. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (removeFolderPermissionsReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-04390f0ec7cc460cb5d34d518e33e7a5}

Det här kodexemplet tar bort behörigheter från en mapp och dess undermappar. Ange `updateChildren` till `false` om du bara behöver ta bort behörigheter från den överordnade mappen.

**Begäran**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**Svar**

Ingen.
