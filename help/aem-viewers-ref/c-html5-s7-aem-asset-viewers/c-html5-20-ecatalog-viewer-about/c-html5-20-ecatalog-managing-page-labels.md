---
description: Hantera sidetiketter
solution: Experience Manager
title: Hantera sidetiketter
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Hantera sidetiketter{#managing-page-labels}

Det finns två platser i visningsprogrammets användargränssnitt där sidetiketter visas: miniatyrläge och listrutan Innehållsförteckning.

Det finns tre typer av etiketter som kan definieras:

* Etiketter som definieras av författaren med hjälp av SYMBOL-lokaliseringsmekanismen.
* Etiketter som författaren har definierat på baksidan, i Dynamic Media Classic.
* Etiketter som automatiskt genereras av visningsprogrammet.

SYMBOL-baserade etiketter definieras med `MediaSet.LABEL_XX[_YY]` och `MediaSet.LABEL_DELIM` SYMBOL enligt beskrivningen i [Lokalisering av element i användargränssnittet](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Du kan definiera sådana etiketter för hela det kataloguppslaget, och då ska du använda kort SYMBOL-syntax ( `MediaSet.LABEL_XX`). Du kan också ange den för varje sida individuellt med hjälp av den fullständiga SYMBOL-syntaxen ( `MediaSet.LABEL_XX_YY`).

När du definierar etiketter för båda sidorna i det kataloguppslaget sammanfogar visningsprogrammet dessa etiketter till en sträng med `MediaSet.LABEL_DELIM` SYMBOL. SYMBOL-baserade etiketter har företräde framför etiketter som definieras på baksidan eller automatiskt genereras av användaren.

Etiketter som definieras i Dynamic Media Classic lagras i posten UserData för enskilda sidbilder. Samma som med SYMBOL-baserade etiketter. Det innebär att om båda sidorna i det kataloguppslaget har etiketter definierade, sammanfogas de med `MediaSet.LABEL_DELIM` SYMBOL i liggande läge. Dynamic Media Classic-etiketter har företräde framför automatiskt genererade etiketter, men åsidosätts av SYMBOL-baserade etiketter.

Automatiskt genererade etiketter är sekventiella nummer som tilldelas alla sidor i katalogen. Automatiskt genererade etiketter ignoreras för det angivna uppslaget om det har SYMBOL-baserade etiketter definierade eller Dynamic Media Classic-etiketter definierade.

I innehållsförteckningen går det att inaktivera visningen av automatiskt genererade etiketter med parametern `showdefault`.
