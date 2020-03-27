---
description: Bildåtergivning har stöd för en enkel förbearbetningsmekanism för begäranden som baseras på matchnings- och ersättningsregler för reguljära uttryck.
seo-description: Bildåtergivning har stöd för en enkel förbearbetningsmekanism för begäranden som baseras på matchnings- och ersättningsregler för reguljära uttryck.
seo-title: Referens för regeluppsättning
solution: Experience Manager
title: Referens för regeluppsättning
topic: Scene7 Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Referens för regeluppsättning{#rule-set-reference}

Bildåtergivning har stöd för en enkel förbearbetningsmekanism för begäranden som baseras på matchnings- och ersättningsregler för reguljära uttryck.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Samlingar med förbearbetningsregler (*regeluppsättningar*) kan bifogas till materialkataloger eller standardkatalogen. Regler i standardkatalogen gäller bara om begäran inte bifogar en viss materialkatalog.

Regler för förbehandling av begäranden kan ändra sökvägen och frågedelarna av begäranden innan de bearbetas av serverns begärandeparser, bland annat ändra sökvägen, lägga till kommandon, ändra kommandovärden och använda mallar eller makron. Regler kan också användas för att konfigurera och åsidosätta vissa katalogattribut, samt för att begränsa tjänsten till vissa IP-adresser för klienter.

Regeluppsättningar sparas som XML-dokumentfiler. Den relativa eller absoluta sökvägen för regeluppsättningsfilen måste anges i `attribute::RuleSetFile`.

## Allmän struktur {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

Elementen `<?xml>`, `<!DOCTYPE>` och `<ruleset>` är alltid obligatoriska i en giltig XML-fil för regeluppsättningar, även om inga faktiska regler har definierats.

Ett `<ruleset>` element som innehåller valfritt antal `<rule>` element tillåts.

Innehållet i regelfiler för förbearbetning är skiftlägeskänsligt.

## Förbehandling av URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Innan någon annan bearbetning utförs, analyseras en inkommande HTTP-begäran delvis för att avgöra vilken materialkatalog som ska användas. När katalogen har identifierats tillämpas regeluppsättningen för den valda katalogen (eller standardkatalogen, om ingen specifik katalog har identifierats).

Elementen `<rule>` söks igenom i den ordning som anges för att matcha innehållet i `<expression>` elementet ( *`expression`*).

Om en `<rule>` matchas *`substitution`* tillämpas den valfria strängen och den ändrade begärandesträngen skickas till serverns begärandeparser för normal bearbetning.

Om ingen matchning görs när slutet av `<ruleset>` sökningen nås, skickas begäran till tolken utan ändring.

## Attributet OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

Standardbeteendet kan ändras med attributet `OnMatch` för `<rule>` elementen. `OnMatch` kan anges till `break` (standard), `continue`eller `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Element och attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Beteende när en matchning inträffar </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Regelbearbetningen avslutas omedelbart efter att ersättandet för den här regeln har tillämpats. Standard. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Ersättningen används och bearbetningen fortsätter med nästa regel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>Regelbearbetningen avslutas omedelbart och statusen för svaret på begäran avslagen returneras till klienten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Åsidosätta katalogattribut {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` -element kan eventuellt definiera attribut som åsidosätter motsvarande katalogattribut när regeln matchas och `OnMatch="break"` ställs in. Inga attribut används om `OnMatch="continue"` de anges. I beskrivningen av finns en lista `<rule>` med attribut som kan styras med regler.

## Reguljära uttryck {#section-4d326507b52544b0960a9a5f303e3fe6}

Enkel strängmatchning fungerar för mycket grundläggande program, men reguljära uttryck krävs i de flesta fall. Medan reguljära uttryck är branschstandard varierar den specifika implementeringen från instans till instans.

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) beskriver den specifika implementeringen av reguljära uttryck som används av Image Serving.

## Infångade delsträngar {#section-8057cd65d48949ffb6a50e929bd3688b}

För att underlätta komplexa URL-ändringar kan delsträngar fångas in i uttrycket genom att omsluta delsträngen med parenteser (..). Infångade delsträngar numreras sekventiellt med början på 1 enligt positionen för den inledande parentesen. De hämtade delsträngarna kan infogas i substitutionen med *`$n`*, där *`n`* är sekvensnumret för den hämtade delsträngen.

## Hantera regeluppsättningsfiler {#section-e8ce976b56404c009496426fd334d23d}

En regeluppsättningsfil kan bifogas till varje materialkatalog med katalogattributet `attribute::RuleSetFile`. Du kan redigera regeluppsättningsfilen när som helst, men bildservern känner bara igen ändringarna när den tillhörande materialkatalogen läses in igen. Detta inträffar när plattformsservern startas eller startas om och när den primära katalogfilen (som har ett [!DNL .ini] filsuffix) ändras eller &quot;ändras&quot; (för att ändra fildatumet).

## Exempel {#section-c4142a41f5cd4ff799a72fbc130c3700}

Exempel på regeluppsättningar finns i motsvarande avsnitt i referenshandboken för bildkatalogen i dokumentationen för bildservrar.

## Se även {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
