---
description: 'null'
seo-description: 'null'
seo-title: Hantera sidetiketter
solution: Experience Manager
title: Hantera sidetiketter
topic: Dynamic media
uuid: 49444fe6-ef34-4e5b-a293-e23830a67b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Hantera sidetiketter{#managing-page-labels}

Det finns två platser i visningsprogrammets användargränssnitt där sidetiketter visas: miniatyrläge och listrutan Innehållsförteckning.

Det finns tre typer av etiketter som kan definieras:

* Etiketter som definieras av författaren med hjälp av SYMBOL-lokaliseringsmekanismen.
* Etiketter som författaren har definierat på baksidan, i Scene7 Publishing System.
* Etiketter som automatiskt genereras av visningsprogrammet.

SYMBOL-baserade etiketter definieras med hjälp av `MediaSet.LABEL_XX[_YY]` - och `MediaSet.LABEL_DELIM` SYMBOL:er enligt beskrivningen i [Lokalisering av element](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)i användargränssnittet. Du kan definiera sådana etiketter för hela det kataloguppslaget, och då ska du använda kort SYMBOL-syntax ( `MediaSet.LABEL_XX`). Du kan också ange den för varje sida individuellt med hjälp av den fullständiga SYMBOL-syntaxen ( `MediaSet.LABEL_XX_YY`).

När du definierar etiketter för båda sidorna i det kataloguppslaget sammanfogar visningsprogrammet dessa etiketter till en sträng med hjälp av `MediaSet.LABEL_DELIM` SYMBOL. SYMBOL-baserade etiketter har företräde framför etiketter som definieras på baksidan eller automatiskt genereras av användaren.

Etiketter som definieras i Scene7 Publishing System lagras i UserData-posten för enskilda sidbilder. Samma som med SYMBOL-baserade etiketter. Det innebär att om båda sidorna i det kataloguppslaget har etiketter definierade, sammanfogas de med `MediaSet.LABEL_DELIM` SYMBOL i liggande läge. Scene7 Publishing System-etiketter har företräde framför automatiskt genererade etiketter, men åsidosätts av SYMBOL-baserade etiketter.

Automatiskt genererade etiketter är sekventiella nummer som tilldelas alla sidor i katalogen. Automatiskt genererade etiketter ignoreras för det angivna uppslaget om SYMBOL-baserade etiketter har definierats eller Scene7 Publishing System-etiketter har definierats.

I innehållsförteckningen går det att inaktivera visningen av automatiskt genererade etiketter med hjälp av `showdefault` parametern.
