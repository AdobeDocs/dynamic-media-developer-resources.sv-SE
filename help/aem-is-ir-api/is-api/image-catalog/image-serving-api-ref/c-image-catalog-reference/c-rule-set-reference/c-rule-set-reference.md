---
description: Image Serving har stöd för en enkel förbearbetningsmekanism för begäranden som baseras på matchnings- och ersättningsregler för reguljära uttryck.
seo-description: Image Serving har stöd för en enkel förbearbetningsmekanism för begäranden som baseras på matchnings- och ersättningsregler för reguljära uttryck.
seo-title: Referens för regeluppsättning
solution: Experience Manager
title: Referens för regeluppsättning
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Referens för regeluppsättning{#rule-set-reference}

Image Serving har stöd för en enkel förbearbetningsmekanism för begäranden som baseras på matchnings- och ersättningsregler för reguljära uttryck.

Samlingar med förbearbetningsregler (*regeluppsättningar*) kan bifogas till bildkataloger eller standardkatalogen. Regler i standardkatalogen gäller bara om begäran inte identifierar en viss huvudbildkatalog.

Regler för förbehandling av begäranden kan ändra sökvägen och frågedelarna av begäranden innan de bearbetas av plattformsserverns parser, inklusive att ändra sökvägen, lägga till kommandon, ändra kommandovärden och använda mallar eller makron. Regler kan också användas för att konfigurera och åsidosätta vissa säkerhetsfunktioner som normalt bara styrs med katalogattribut, till exempel begärandeförfalskning, vattenmärkning, samt för att begränsa tjänsten till specifika IP-adresser för klienter.

Regeluppsättningar sparas som XML-dokumentfiler. Den relativa eller absoluta sökvägen för regeluppsättningsfilen måste anges i `attribute::RuleSetFile`.

## Allmän struktur {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

Elementen `<?xml>` och `<ruleset>` är alltid obligatoriska i en giltig XML-fil för regeluppsättningar, även om inga faktiska regler har definierats.

Ett `<ruleset>` element som innehåller valfritt antal `<rule>` element tillåts.

Innehållet i regelfiler för förbearbetning är skiftlägeskänsligt.

## Validering av regeluppsättning {#section-d8d101a0b4d74580835e37d128d05567}

En kopia av [!DNL RuleSet.xsd] finns i katalogmappen och bör användas för att validera en regeluppsättningsfil innan den registreras i [!DNL catalog.ini] filen. Observera att Image Serving använder en intern kopia av [!DNL RuleSet.xsd] för validering.

## Förbehandling av URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Innan någon annan bearbetning utförs, analyseras en inkommande HTTP-begäran delvis för att avgöra vilken bildkatalog som ska användas. När katalogen har identifierats tillämpas regeluppsättningen för den valda katalogen (eller standardkatalogen, om ingen specifik katalog har identifierats).

Elementen `<rule>` söks igenom i den ordning som anges för att matcha innehållet i `<expression>` elementet ( *`expression`*).

Om en `<rule>` matchas *`substitution`* tillämpas den valfria strängen och den ändrade begärandesträngen skickas till serverns begärandeparser för normal bearbetning.

Om ingen matchning görs när slutet av `<ruleset>` sökningen nås, skickas begäran till tolken utan ändring.

## Attributet OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

Standardbeteendet kan ändras med `OnMatch` -attributet för `<rule>` elementet. `OnMatch` kan anges till `break` (standard), `continue`eller `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Element och attribut</b> </th> 
   <th class="entry"> <b>Beteende när en matchning inträffar</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>Regelbearbetningen avslutas omedelbart efter att ersättandet för den här regeln har tillämpats. Standard. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>Ersättningen används och bearbetningen fortsätter med nästa regel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>Regelbearbetningen avslutas omedelbart och statusen för svaret på begäran avslagen returneras till klienten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Åsidosätta katalogattribut {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` -element kan också definiera attribut som åsidosätter motsvarande katalogattribut när regeln matchas. Om flera matchade regler anger samma attribut gäller den sista. I beskrivningen av elementet finns en lista med attribut som kan styras med regler. ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)`

## Reguljära uttryck {#section-3f77bb9a265147b38c645f63ab1bad8b}

Enkel strängmatchning fungerar för mycket grundläggande program, men reguljära uttryck krävs i de flesta fall. Medan reguljära uttryck är branschstandard varierar den specifika implementeringen från instans till instans.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) beskriver den specifika implementeringen av reguljära uttryck som används av Image Serving.

## Infångade delsträngar {#section-066e659406d5403599cd26ae35e80d68}

För att underlätta komplexa URL-ändringar kan delsträngar fångas in i uttrycket genom att omsluta delsträngen med parenteser (..). Infångade delsträngar numreras sekventiellt med början på 1 enligt positionen för den inledande parentesen. De hämtade delsträngarna kan infogas i substitutionen med ` $ *`n`*`, där *`n`* är sekvensnumret för den hämtade delsträngen.

## Hantera regeluppsättningsfiler {#section-0598a608e4044bb4805fe93ceebe10a9}

En regeluppsättningsfil kan bifogas till varje bildkatalog med katalogattributet `attribute::RuleSetFile`. Du kan redigera regeluppsättningsfilen när som helst, men bildservern känner bara igen ändringarna när den associerade bildkatalogen läses in igen. Den här inläsningen sker när plattformsservern startas eller startas om och när den primära katalogfilen, som har ett [!DNL .ini] filsuffix, ändras eller&quot;ändras&quot; för att ändra fildatumet.

## Exempel {#section-aa769437d967459299b83a4bf34fe924}

**Exempel A.** Definiera en regel som ökar bildkvalitetsinställningarna om bildnamnet har suffixet &quot; [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

Regeluttrycket anger en skiftlägesokänslig matchning av &quot; [!DNL _hg]&quot; i slutet av URL-strängen. Suffixet ersätts med den angivna frågesträngen som ändrar bildkvalitetsinställningarna. Observera att `?` tecknet i ersättningssträngen escape-konverteras eftersom det är ett specialtecken i reguljära uttryck.

>[!NOTE]
>
>Den kodning som krävs för et-tecknet. Alternativt kan ersättningssträngen omslutas av ett CDATA-block:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Exempel B.** Ett visst webbprogram tillåter inte frågesträngar. Definiera en regel som översätter det efterföljande banelementet `small`, `medium`eller `large` till en mall, med resten av sökvägen som bildnamn. skulle till exempel `myCat/myImage/small` översätta till `myCat/smallTemplate?src=myCat/myImage`.

Vi kan använda delsträngar för att strukturera om begäran:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Se även {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
