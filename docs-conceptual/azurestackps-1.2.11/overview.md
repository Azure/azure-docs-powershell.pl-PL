---
title: Omówienie programu Azure Stack PowerShell | Microsoft Docs
description: Omówienie instalacji i konfiguracji programu Azure Stack PowerShell.
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: f895992b4200f260189b3dbc541452e73a377b00
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
---
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell

Usługa Azure Stack wymaga dwóch następujących modułów programu PowerShell:  

1. Zgodny z usługą Azure Stack moduł **AzureRM**, który jest dostępny po zainstalowaniu profilu wersji interfejsu API **2017-03-09-profile**. Z poleceń cmdlet zainstalowanych za pomocą tego profilu mogą korzystać użytkownicy i operatorzy usługi Azure Stack.

2. Najnowszą wersją jest instalacja **1.2.11** modułu **AzureStack**. Z poleceń cmdlet zainstalowanych za pomocą tego modułu mogą korzystać tylko operatorzy usługi Azure Stack. Operatorzy mogą wykonywać operacje, takie jak zarządzanie ofertami, planami, usługami, przydziałami itp., przy użyciu poleceń cmdlet programu PowerShell oferowanych przez ten moduł. Aby dowiedzieć się więcej o poleceniach cmdlet programu PowerShell dostępnych w tym module, zobacz zawartość dokumentacji rozwiązań [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) i [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage).

## <a name="next-steps"></a>Następne kroki

* [Install PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Instalowanie programu PowerShell dla usługi Azure Stack)
* [Configure PowerShell for use with Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Konfigurowanie programu PowerShell do używania z usługą Azure Stack)
