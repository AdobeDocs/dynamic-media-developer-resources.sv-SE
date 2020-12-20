---
description: 'null'
seo-description: 'null'
seo-title: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
topic: Dynamic media
uuid: c7063907-78e8-47f8-9424-78ab9d123ad1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`mall`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> mall</span></span> </p> </td> 
   <td> <p>Innehållsmallen som data som returneras från infoservern sammanfogas i. </p> <p>Innehållsmallen är en XML som följer detta DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>Syntaxen för innehållsmallen är följande: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>Det innebär att mallen måste börja med <span class="codeph"> &lt;info&gt;</span>-elementet som kan innehålla <span class="codeph"> &lt;var&gt;</span>-element (valfritt). Själva mallinnehållet <span class="codeph"> TEMPLATE_CONTENT</span> är HTML-text. Innehållsmallen kan dessutom innehålla variabelnamn omgivna av <span class="codeph"> $</span> tecken som ersätts med de variabelvärden som informationsservern returnerar eller med standardvärden. </p> <p>Standardvariabler som definieras i mallen kan antingen vara globala (om rollover-attributet inte har angetts) eller specifika för en viss rollover-nyckel (om rollover-attributet finns). </p> <p>Under mallbearbetningen har variabler som är specifika för rollover-nycklar företräde framför globala variabler. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tänk på att när du konfigurerar Info Panel-popup körs den HTML-kod och JavaScript-kod som skickas till Info-panelen på klientens dator. Kontrollera därför att sådan HTML-kod och JavaScript-kod är säkra.

## Egenskaper {#section-6dd7785357d740d095fa9f7fd0f67da4}

Valfritt.

## Standard {#section-cd5db06d08aa4de49e37d6c938b41570}

Ingen.

## Exempel {#section-16d184665c484964af9a22f79ff3f840}

Om informationsserversvaret returnerar produktnamnet som variabel `$1$` och produktbild-URL returneras som variabel `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
