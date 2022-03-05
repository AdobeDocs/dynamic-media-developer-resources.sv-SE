---
description: En egenskapsuppsättningstyp anger olika inställningar som används för att hantera egenskapsuppsättningar.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# createPropertySetType{#createpropertysettype}

En egenskapsuppsättningstyp anger olika inställningar som används för att hantera egenskapsuppsättningar.

Syntax

## Auktoriserade användartyper {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-43dece72eb9f44df80f4a119dd2c008b}

**Indata (createPropertySetTypeParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Nej | Referensen till företaget som äger egenskapsuppsättningstypen. If `companyHandle` skickas inte och anroparen är en `IpsAdmin`, skapas en global egenskapsuppsättningstyp. |
| `*`name`*` | `xsd:string` | Ja | Namnet på egenskapsuppsättningstypen. |
| `*`propertyType`*` | `xsd:string` | Ja | Val av egenskapsuppsättningstyper. |
| `*`allowMultiple`*` | `xsd:boolean` | Ja | Avgör om ditt program kan ha flera egenskapsuppsättningar. |

**Utdata (createPropertySetTypeReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Ja | Ett handtag till typen. |

## Exempel {#section-13396c9639a6475190e622eae3cdb534}

I det här kodexemplet skapas en egenskapsuppsättning med ett namn och en typ som anges av `PropertySet Types` konstant. Referensen till företaget som äger egenskapsuppsättningstypen. Om companyHandle inte skickas och anroparen är en IpsAdmin skapas en global egenskapsuppsättningstyp.

**Begäran**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**Svar**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```
