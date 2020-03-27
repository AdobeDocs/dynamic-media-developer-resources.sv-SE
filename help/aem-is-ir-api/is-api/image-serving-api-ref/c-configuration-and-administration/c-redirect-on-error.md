---
description: IS-servrar kan konfigureras för failover till alternativa servrar för begäranden som innehåller en källbild som inte kan öppnas eller läsas.
seo-description: IS-servrar kan konfigureras för failover till alternativa servrar för begäranden som innehåller en källbild som inte kan öppnas eller läsas.
seo-title: Omdirigering vid fel
solution: Experience Manager
title: Omdirigering vid fel
topic: Scene7 Image Serving - Image Rendering API
uuid: 894babe9-9c3c-4972-ae8f-387d65b4167d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Omdirigering vid fel{#redirect-on-error}

IS-servrar kan konfigureras för failover till alternativa servrar för begäranden som innehåller en källbild som inte kan öppnas eller läsas.

Följande typer av begäranden omdirigeras:

* IS Images that are in the catalog, but not on disk.

   Om en bild inte finns i en katalog bör felomdirigering inte ske när det inte går att hitta bilden.

* Skadade bilder, färgprofiler eller teckensnitt.
* Statiskt innehåll kan inte hittas på disken.

   Förfrågningar om statiskt innehåll omdirigeras när det inte går att hitta på disken, även om det refererade statiska innehållet inte har någon katalogpost.

Omdirigering av fel sker inte i något annat fall.

När den är aktiverad och ett sådant fel inträffar under bearbetningen av begäran, skickar den primära servern begäran till den sekundära servern för bearbetning. Svaret vidarebefordras sedan direkt till klienten, oavsett om det visar om det är klart eller inte. Den primära servern markerar loggposter för sådana vidarebefordrade begäranden med cacheanvändning `REMOTE`. Svarsdata cachelagras inte lokalt av den primära servern.

Felomdirigering aktiveras genom inställning `PS::errorRedirect.rootUrl` till den sekundära serverns HTTP-domännamn och portnummer. Dessutom konfigureras timeout för anslutningen med `PS::errorRedirect.connectTimeout` och den maximala tid som den primära servern väntar på ett svar från den sekundära servern innan ett fel returneras till klienten konfigureras med `PS::errorRedirect.socketTimeout`.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Om den sekundära servern inte kan kontaktas returneras ett textfelssvar till klienten, även om en standardbild eller felbild är konfigurerad.

>[!NOTE]
>
>Rörtecken (|) i nätsökvägen stöds inte för felomdirigering.

## Se även {#section-2e8bfc128b944baf8108279d16492f3f}

[Felomdirigering](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
