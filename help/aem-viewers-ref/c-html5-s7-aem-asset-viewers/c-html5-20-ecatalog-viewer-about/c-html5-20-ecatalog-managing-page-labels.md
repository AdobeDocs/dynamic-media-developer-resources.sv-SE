---
description: Hantera sidetiketter
solution: Experience Manager
title: Hantera sidetiketter
topic: Dynamic media
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---


# Hantera sidetiketter{#managing-page-labels}

Det finns två platser i visningsprogrammets användargränssnitt där sidetiketter visas: miniatyrläge och listrutan Innehållsförteckning.

Det finns tre typer av etiketter som kan definieras:

* Etiketter som definieras av författaren med hjälp av SYMBOL-lokaliseringsmekanismen.
* Etiketter som författaren har definierat på baksidan, i SPS.
* Etiketter som automatiskt genereras av visningsprogrammet.

SYMBOL-baserade etiketter definieras med `MediaSet.LABEL_XX[_YY]` och `MediaSet.LABEL_DELIM` SYMBOL enligt beskrivningen i [Lokalisering av element i användargränssnittet](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Du kan definiera sådana etiketter för hela det kataloguppslaget, och då ska du använda kort SYMBOL-syntax ( `MediaSet.LABEL_XX`). Du kan också ange den för varje sida individuellt med hjälp av den fullständiga SYMBOL-syntaxen ( `MediaSet.LABEL_XX_YY`).

När du definierar etiketter för båda sidorna i det kataloguppslaget sammanfogar visningsprogrammet dessa etiketter till en sträng med `MediaSet.LABEL_DELIM` SYMBOL. SYMBOL-baserade etiketter har företräde framför etiketter som definieras på baksidan eller automatiskt genereras av användaren.

Etiketter som definieras i SPS lagras i UserData-posten för enskilda sidbilder. Samma som med SYMBOL-baserade etiketter. Det innebär att om båda sidorna i det kataloguppslaget har etiketter definierade, sammanfogas de med `MediaSet.LABEL_DELIM` SYMBOL i liggande läge. SPS-etiketter har företräde framför automatiskt genererade etiketter, men åsidosätts av SYMBOL-baserade etiketter.

Automatiskt genererade etiketter är sekventiella nummer som tilldelas alla sidor i katalogen. Automatiskt genererade etiketter ignoreras för det angivna uppslaget om det har SYMBOL-baserade etiketter definierade eller SPS-etiketter definierade.

I innehållsförteckningen går det att inaktivera visningen av automatiskt genererade etiketter med parametern `showdefault`.
