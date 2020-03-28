---
description: Inställningarna i det här avsnittet gäller för mediesvaren som hämtas av req=set modifier.
seo-description: Inställningarna i det här avsnittet gäller för mediesvaren som hämtas av req=set modifier.
seo-title: Medieuppsättningssvar
solution: Experience Manager
title: Medieuppsättningssvar
topic: Scene7 Image Serving - Image Rendering API
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Medieuppsättningssvar{#media-set-responses}

Inställningarna i det här avsnittet gäller för mediesvaren som hämtas av req=set modifier.

## PS::fvctx.useCatalogRecordValidation - Caching Policy {#section-9accb087d16548a988993bb30395a6f6}

Den här egenskapen styr cachelagringsprincipen när du avgör om ett svar som hämtas från cache måste genereras om eller inte. Om egenskapen är inaktiverad används tidsstämpeln för [!DNL catalog.ini] filen för validering. Om egenskapen är aktiverad används den senaste `catalog::LastModified` tidsstämpeln från alla refererade poster för validering.

## PS::fvctx.nestingLimit - kapslingsgräns {#section-280210341f1647fea02590e7069934d2}

Maximalt kapslingsdjup för alla `req=set` svar. Om djupet överskrids returneras ett fel.

## PS::fvctx.brochureLimit - broschyrgräns {#section-fe36e47db49244cea7f07e9dd3639440}

Det maximala antalet e-katalogbroschyrer i svaret som innehåller alla associerade metadata `req=set` . När den här gränsen har överskridits ignoreras alla privata kartor och användardata som är kopplade till broschyrobjektet.
