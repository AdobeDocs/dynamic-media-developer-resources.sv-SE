---
description: Inställningarna i det här avsnittet gäller för mediesvaren som hämtas av req=set modifier.
solution: Experience Manager
title: Medieuppsättningssvar
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Medieuppsättningssvar{#media-set-responses}

Inställningarna i det här avsnittet gäller för mediesvaren som hämtas av req=set modifier.

## PS::fvctx.useCatalogRecordValidation - Caching Policy {#section-9accb087d16548a988993bb30395a6f6}

Den här egenskapen styr cachelagringsprincipen när du avgör om ett svar som hämtas från cache måste genereras om eller inte. Om egenskapen är inaktiverad används tidsstämpeln för filen [!DNL catalog.ini] för validering. Om egenskapen är aktiverad används den senaste `catalog::LastModified`-tidsstämpeln från alla refererade poster för validering.

## PS::fvctx.nestingLimit - kapslingsgräns {#section-280210341f1647fea02590e7069934d2}

Det maximala kapslingsdjupet för ett `req=set`-svar. Om djupet överskrids returneras ett fel.

## PS::fvctx.brochureLimit - broschyrgräns {#section-fe36e47db49244cea7f07e9dd3639440}

Det maximala antalet e-katalogbroschyrer i `req=set`-svaret som innehåller alla associerade metadata. När den här gränsen har överskridits ignoreras alla privata kartor och användardata som är kopplade till broschyrobjektet.
