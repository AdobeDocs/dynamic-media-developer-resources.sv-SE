---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: b792cddb-f3d2-4609-95b7-105d76fb3d6f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`mall`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> mall </span></span> </p> </td> 
   <td> <p>Innehållsmallen som data som returneras från infoservern sammanfogas i. </p> <p>Innehållsmallen är en XML som följer detta DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;&lbrack;
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      &rbrack;&gt;</code> </p> <p>Syntaxen för innehållsmallen är följande: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;!&lbrack;CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>Det innebär att mallen måste börja med elementet <span class="codeph"> &lt;info&gt;</span> som kan innehålla valfria <span class="codeph"> &lt;var&gt;</span> -element. Själva mallinnehållet <span class="codeph"> TEMPLATE_CONTENT</span> är HTML-text. Innehållsmallen kan dessutom innehålla variabelnamn omgivna av <span class="codeph"> $</span> tecken. Dessa tecken ersätts med de variabelvärden som informationsservern returnerar eller med standardvärden. </p> <p>Standardvariabler som definieras i mallen kan antingen vara globala (om rollover-attributet inte har angetts) eller specifika för en viss rollover-nyckel (om rollover-attributet finns). </p> <p>Under mallbearbetningen har variabler som är specifika för rollover-nycklar företräde framför globala variabler. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Tänk på att när du konfigurerar popup-rutan för panelen Info körs den HTML-kod och JavaScript-kod som skickas till panelen Info på klientens dator. Se därför till att sådan HTML-kod och JavaScript-kod är säkra.

## Egenskaper {#section-6dd7785357d740d095fa9f7fd0f67da4}

Valfritt.

## Standard {#section-cd5db06d08aa4de49e37d6c938b41570}

Ingen.

## Exempel {#section-16d184665c484964af9a22f79ff3f840}

Anta att informationsserversvaret returnerar produktnamnet som variabeln `$1$` och att produktbild-URL returneras som variabel `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
