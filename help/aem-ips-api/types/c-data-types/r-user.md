---
description: En användare med resurser och typer i systemet.
solution: Experience Manager
title: Användare
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---

# [!DNL User]{#user}

En användare med resurser och typer i systemet.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| userHandle | `xsd:string` | Användarhandtag. |
| firstName | `xsd:string` | Användarens förnamn. |
| lastName | `xsd:string` | Efternamn. |
| e-post | `xsd:string` | e-postadress. |
| defaultRole | `xsd:string` | Anger rollen för en användare i varje företag de tillhör. Användarrollen `IpsAmin` åsidosätter dock andra användarroller. |
| isValid | `xsd:boolean` | Anger om användaren är giltig. |
| passwordExpires | `xsd:dateTime` | Anger förfallodatum för lösenord. |
