---
description: Avgör om en grupp resurser är klara att publiceras.
seo-description: Avgör om en grupp resurser är klara att publiceras.
seo-title: setAssetsPublishState
solution: Experience Manager
title: setAssetsPublishState
topic: Scene7 Image Production System API
uuid: 2910cd6c-573b-405c-864d-a0136ac5472d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetsPublishState{#setassetspublishstate}

Avgör om en grupp resurser är klara att publiceras.

Detta är batchversionen av [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## Auktoriserade användartyper {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till resursen.

## Parametrar {#section-3e49d7859f8647b990d75373cc8dbc24}

**Indata (setAssetsPublishStateParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| ` *`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | Ja | Array med publiceringsstatusvärden för resurserna. |

**Utdata (setAssetsPublishStateParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Antalet resurser som har uppdaterats. |
| ` *`warningCount`*` | `xsd:int` | Ja | Antalet resurser som genererade en varning när åtgärden försökte uppdatera dem. |
| ` *`errorCount`*` | `xsd:int` | Ja | Antalet resurser som genererade ett fel när åtgärden försökte ta bort dem. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Information som är associerad med tillgångsuppdateringarna som genererade en varning. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Information som är associerad med resursuppdateringar som genererade ett fel. |

## Exempel {#section-38cfdd3436214a06a1bae16875501d51}

I det här kodexemplet anges publiceringsstatus för en resurs.

**Begäran**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**Svar**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```

