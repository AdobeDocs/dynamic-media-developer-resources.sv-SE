---
description: Skapar en förinställd vy som avgör vad en användare kan se. Visningsprogrammet kan vara av valfri typ i IPS. Förinställningsvyn används när resurserna publiceras.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,visningsförinställningar
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# createViewerPreset{#createviewerpreset}

Skapar en förinställd vy som avgör vad en användare kan se. Visningsprogrammet kan vara av valfri typ i IPS. Förinställningsvyn används när resurserna publiceras.

Syntax

## Auktoriserade användartyper {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Indata (createViewerPresetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget för det företag som innehåller visningsprogrammets förinställningar och resurser. |
| `*`folderHandle`*` | `xsd:string` | Ja | Hanteringen av mappen som innehåller resurserna. |
| `*`name`*` | `xsd:string` | Ja | Namn på visningsprogram. |
| `*`type`*` | `xsd:string` | Ja | Typ av visningsprogram. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Nej | En array som innehåller namn, värden och handtag för bilder som du använder förinställningar på. |

**Utdata (createViewerPresetReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | Ja | Handtag för förinställningen till användaren. |

## Exempel {#section-c88ea63536f3461cbe4677ba53f875dd}

I det här kodexemplet skapas en videospelarförinställning. Svaret returnerar ett handtag till förinställningen.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**Svar**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```
