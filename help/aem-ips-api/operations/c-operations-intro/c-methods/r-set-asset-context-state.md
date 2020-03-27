---
description: Ange eller uppdatera publiceringsläget för en eller flera resurser. Du kan ange separata publiceringstillstånd för varje publiceringskontext i ett företag.
seo-description: Ange eller uppdatera publiceringsläget för en eller flera resurser. Du kan ange separata publiceringstillstånd för varje publiceringskontext i ett företag.
seo-title: setAssetsContextState
solution: Experience Manager
title: setAssetsContextState
topic: Scene7 Image Production System API
uuid: 4b94f9ea-3f7b-45ee-9381-6434f2bc4e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetsContextState{#setassetscontextstate}

Ange eller uppdatera publiceringsläget för en eller flera resurser. Du kan ange separata publiceringstillstånd för varje publiceringskontext i ett företag.

## Auktoriserade användartyper {#section-815eb031f85143278c1560c18c5e3431}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läsåtkomst för att kunna returnera resursen.

## Parametrar {#section-009b9006de8e4c16ad657c47f28ace9f}

**Indata (setAssetsContextStateParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| ` *`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | Ja | En array med resurser och deras nya publiceringstillstånd. |

**Utdata (setAssetsContexStateReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Antalet resurser har ändrats. |
| ` *`warningCount`*` | `xsd:int` | Ja | Antalet varningar som genereras när åtgärden försökte ändra resurser. |
| ` *`errorCount`*` | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte ändra resurser. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Array med fel som genereras av resurser när åtgärden försökte ändra dem. |

## Exempel {#section-283a073f3cb14bcda5abed863c538aa4}

I det här kodexemplet anges publiceringsstatus för en resurs som använder `NotMarkedForPublish`.

**Begäran**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**Svar**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```

