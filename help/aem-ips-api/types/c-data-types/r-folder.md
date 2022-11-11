---
description: Hierarkiska fil- eller resurslagringsobjekt. Mappar kan innehålla en (eller flera) undermappar.
solution: Experience Manager
title: Mapp
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# [!DNL Folder]{#folder}

Hierarkiska fil- eller resurslagringsobjekt. Mappar kan innehålla en (eller flera) undermappar.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| folderHandle | `xsd:string` | Mappreferens. |
| [!DNL path] | `xsd:string` | Mappsökväg. |
| lastModified | `xsd:dateTime` | Senaste ändringsdatum. |
| childLastModified | `xsd:dateTime` | Senaste ändringsdatum för undermappar och underordnade mappresurser. |
| permissionsSetHandle | `xsd:string` | Mappbehörighetshantering. |
| hasSubfolder | `types:Boolean` | Avgör om en mapp har undermappar. |
| subfolderArray | `types:FolderArray` | En array med undermappar i en mapp. |
