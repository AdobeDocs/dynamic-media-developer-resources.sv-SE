---
description: En användare med resurser och typer i systemet.
seo-description: En användare med resurser och typer i systemet.
seo-title: Användare
solution: Experience Manager
title: Användare
topic: Scene7 Image Production System API
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Användare{#user}

En användare med resurser och typer i systemet.

Syntax

## Parametrar {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Namn | Typ | Beskrivning |
|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Användarhandtag. |
| ` *`firstName`*` | `xsd:string` | Användarens förnamn. |
| ` *`lastName`*` | `xsd:string` | Användarens efternamn. |
| ` *`e-post`*` | `xsd:string` | e-postadress. |
| ` *`defaultRole`*` | `xsd:string` | Anger rollen för en användare i varje företag de tillhör. Användarrollen `IpsAmin` åsidosätter dock andra användarroller. |
| ` *`isValid`*` | `xsd:boolean` | Anger om användaren är giltig. |
| ` *`passwordExpires`*` | `xsd:dateTime` | Anger förfallodatum för lösenord. |

