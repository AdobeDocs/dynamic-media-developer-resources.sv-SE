---
description: En användare med resurser och typer i systemet.
solution: Experience Manager
title: Användare
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
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

