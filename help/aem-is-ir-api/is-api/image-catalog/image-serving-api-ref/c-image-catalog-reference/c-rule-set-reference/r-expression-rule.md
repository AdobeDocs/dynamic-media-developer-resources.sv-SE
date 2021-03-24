---
description: Mönsterelement för reguljära uttryck. Valfritt i <rule>-element.
solution: Experience Manager
title: uttryck
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# uttryck{#expression}

Mönsterelement för reguljära uttryck. Valfritt i `<rule>`-element.

## Attribut {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Ingen.

## Data {#section-e2601008d71243109af1a8c55b58416d}

Mönstersträng för reguljärt uttryck.

## Beskrivning {#section-759bfb738ddb45dba1f0807aba8c1113}

Elementet `<expression>` kan vara tomt eller innehålla en enkel söksträng eller ett mönster för reguljära uttryck. Mönstret används på hela strängen för begäran.

En matchning inträffar alltid när `<expression>` är tom eller inte har angetts; motsvarar att ange `<expression>.*</expression>`.

Implementeringen baseras på Java-paketet [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), som har en syntax för reguljära uttryck som liknar Perls.

## Anteckningar {#section-10b472a902674893b49ca49a7052c366}

Uttryckssträngen får inte innehålla literala &lt;- och &amp;-tecken. Dessa reserverade tecken kan kodas med `&` och `<`, eller så kan hela strängen omslutas av ett XML `CDATA`-avsnitt:

`<expression><![CDATA[&fmt=custom]]></expression>`

Alla tecken mellan taggarna `<expression>` och `</expression>` skickas till parsern för reguljära uttryck, inklusive tecken utanför det valfria `CDATA`-avsnittet. Försiktighet bör iakttas för att undvika extra utrymme.

## Se även {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
