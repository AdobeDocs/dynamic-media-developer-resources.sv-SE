---
description: Hierarkiska fil- eller resurslagringsobjekt. Mappar kan innehålla en (eller flera) undermappar.
seo-description: Hierarkiska fil- eller resurslagringsobjekt. Mappar kan innehålla en (eller flera) undermappar.
seo-title: Mapp
solution: Experience Manager
title: Mapp
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
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

