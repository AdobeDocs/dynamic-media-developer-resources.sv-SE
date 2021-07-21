---
description: En användare med resurser och typer i systemet.
solution: Experience Manager
title: Användare
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Användare{#user}

En användare med resurser och typer i systemet.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | Användarhandtag. |
| `*`firstName`*` | `xsd:string` | Användarens förnamn. |
| `*`lastName`*` | `xsd:string` | Användarens efternamn. |
| `*`e-post`*` | `xsd:string` | e-postadress. |
| `*`defaultRole`*` | `xsd:string` | Anger rollen för en användare i varje företag de tillhör. Användarrollen `IpsAmin` åsidosätter dock andra användarroller. |
| `*`isValid`*` | `xsd:boolean` | Anger om användaren är giltig. |
| `*`passwordExpires`*` | `xsd:dateTime` | Anger förfallodatum för lösenord. |
