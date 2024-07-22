---
description: Mönsterelement för reguljära uttryck. Valfritt i <rule>-element.
solution: Experience Manager
title: uttryck
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# uttryck{#expression}

Mönsterelement för reguljära uttryck. Valfritt i `<rule>`-element.

## Attribut {#section-fd0574eee1f9423cbb2ed709c0906800}

Ingen.

## Data {#section-4cd740c511a1432da0955e9acfbcf96f}

Mönstersträng för reguljärt uttryck.

## Beskrivning {#section-3245c8a531bb455d8398449f6ea63b37}

Elementet `<expression>` kan vara tomt eller innehålla en enkel söksträng eller ett mönster för reguljära uttryck. Mönstret används på hela strängen för begäran.

En matchning inträffar alltid när `<expression>` är tom eller inte har angetts. Detta motsvarar att ange `<expression>.*</expression>`.

Implementeringen baseras på Java-paketet [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e) som tillhandahåller en syntax för reguljära uttryck som liknar Perls.

## Anteckning {#section-6b41a900b0ce4a9590e5861e3c81599c}

Uttryckssträngen får inte innehålla literala &lt;- och &amp;-tecken. Dessa reserverade tecken kan kodas med `&` respektive `<`, eller så kan hela strängen omslutas av ett XML `CDATA` -avsnitt:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alla tecken mellan taggarna `<expression>` och `</expression>` skickas till parsern för reguljära uttryck, inklusive tecken utanför det valfria avsnittet `CDATA`. Försiktighet bör iakttas för att undvika extra tomt utrymme.

## Se även {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
