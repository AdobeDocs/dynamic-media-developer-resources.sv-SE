---
description: Egenskapsuppsättningar är programspecifika uppsättningar med namn/värde-par som kan kopplas till olika IPS-objekt, beroende på egenskapsuppsättningstypen. Om egenskapsuppsättningstypen inte tillåter att flera uppsättningar kopplas till ett objekt (PropertySetType/allowMultipleisfalse) och objektet redan har en associerad uppsättning av samma typ, ersätter den nya uppsättningen den befintliga.
seo-description: Egenskapsuppsättningar är programspecifika uppsättningar med namn/värde-par som kan kopplas till olika IPS-objekt, beroende på egenskapsuppsättningstypen. Om egenskapsuppsättningstypen inte tillåter att flera uppsättningar kopplas till ett objekt (PropertySetType/allowMultipleisfalse) och objektet redan har en associerad uppsättning av samma typ, ersätter den nya uppsättningen den befintliga.
seo-title: createPropertySet
solution: Experience Manager
title: createPropertySet
topic: Scene7 Image Production System API
uuid: f0b5b951-143f-4a31-bb6b-cdeabdebbcbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createPropertySet{#createpropertyset}

Egenskapsuppsättningar är programspecifika uppsättningar med namn/värde-par som kan kopplas till olika IPS-objekt, beroende på egenskapsuppsättningstypen. Om egenskapsuppsättningstypen inte tillåter att flera uppsättningar kopplas till ett objekt (PropertySetType/allowMultipleisfalse) och objektet redan har en associerad uppsättning av samma typ, ersätter den nya uppsättningen den befintliga.

Syntax

## Auktoriserade användartyper {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-25258e75f5f3419bad165c797eb6cd8e}

**Indata (createPropertySetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | Ja | Referensen till egenskapsuppsättningstypen. |
| ` *`primaryOwnerHandle`*` | `xsd:string` | Ja | Referensen till den primära ägaren av egenskapsuppsättningen. |
| ` *`secondaryOwnerHandle`*` | `xsd:string` | Nej | Handtaget till den sekundära ägaren av egenskapsuppsättningen. |
| ` *`propertyArray`*` | `types:PropertyArray` | Ja | Arrayen med egenskaper. |
| ` *`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**Utdata (createPropertySetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`setHandle`*` | `xsd:string` | Ja | Referensen till den nya egenskapsuppsättningen. |

## Exempel {#section-4e1f5b2883664bc88f590fcd253df22b}

I det här kodexemplet skapas en egenskapsuppsättning som innehåller namn och värden för egenskaper. Svaret returnerar en referens till den nya egenskapsuppsättningen.

**Begäran**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**Svar**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```

