---
description: Hierarkiska fil- eller resurslagringsobjekt. Mappar kan innehålla en (eller flera) undermappar.
seo-description: Hierarkiska fil- eller resurslagringsobjekt. Mappar kan innehålla en (eller flera) undermappar.
seo-title: Mapp
solution: Experience Manager
title: Mapp
topic: Scene7 Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Mapp{#folder}

Hierarkiska fil- eller resurslagringsobjekt. Mappar kan innehålla en (eller flera) undermappar.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Mappreferens. |
| ` *`bana`*` | `xsd:string` | Mappsökväg. |
| ` *`lastModified`*` | `xsd:dateTime` | Senaste ändringsdatum. |
| ` *`childLastModified`*` | `xsd:dateTime` | Senaste ändringsdatum för undermappar och underordnade mappresurser. |
| ` *`permissionsSetHandle`*` | `xsd:string` | Mappbehörighetshantering. |
| ` *`hasSubfolder`*` | `types:Boolean` | Avgör om en mapp har undermappar. |
| ` *`subfolderArray`*` | `types:FolderArray` | En array med undermappar i en mapp. |

