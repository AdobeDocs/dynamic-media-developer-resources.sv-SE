---
description: Hierarkiska fil- eller resurslagringsobjekt. Mappar kan innehålla en (eller flera) undermappar.
solution: Experience Manager
title: Mapp
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---


# Mapp{#folder}

Hierarkiska fil- eller resurslagringsobjekt. Mappar kan innehålla en (eller flera) undermappar.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Mappreferens. |
| `*`bana`*` | `xsd:string` | Mappsökväg. |
| `*`lastModified`*` | `xsd:dateTime` | Senaste ändringsdatum. |
| `*`childLastModified`*` | `xsd:dateTime` | Senaste ändringsdatum för undermappar och underordnade mappresurser. |
| `*`permissionsSetHandle`*` | `xsd:string` | Mappbehörighetshantering. |
| `*`hasSubfolder`*` | `types:Boolean` | Avgör om en mapp har undermappar. |
| `*`subfolderArray`*` | `types:FolderArray` | En array med undermappar i en mapp. |

