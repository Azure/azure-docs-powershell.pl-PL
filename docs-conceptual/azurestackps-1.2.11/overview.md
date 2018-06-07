---
title: Omówienie programu Azure Stack PowerShell | Microsoft Docs
description: Omówienie instalacji i konfiguracji programu Azure Stack PowerShell.
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 3f55ff613004f0726e20255126b29bf7f64662b8
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820205"
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="dd9a9-103">Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="dd9a9-103">Azure Stack PowerShell</span></span>

<span data-ttu-id="dd9a9-104">Usługa Azure Stack wymaga dwóch następujących modułów programu PowerShell:</span><span class="sxs-lookup"><span data-stu-id="dd9a9-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="dd9a9-105">Zgodny z usługą Azure Stack moduł **AzureRM**, który jest dostępny po zainstalowaniu profilu wersji interfejsu API **2017-03-09-profile**.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="dd9a9-106">Z poleceń cmdlet zainstalowanych za pomocą tego profilu mogą korzystać użytkownicy i operatorzy usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-106">The cmdlets installed by using this profile can be used by Azure Stack operators and users.</span></span>

2. <span data-ttu-id="dd9a9-107">Najnowszą wersją jest instalacja **1.2.11** modułu **AzureStack**.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-107">The most current version is the **1.2.11** install of the **AzureStack** module.</span></span> <span data-ttu-id="dd9a9-108">Z poleceń cmdlet zainstalowanych za pomocą tego modułu mogą korzystać tylko operatorzy usługi Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-108">The cmdlets installed by using this module can be used by Azure Stack operators only.</span></span> <span data-ttu-id="dd9a9-109">Operatorzy mogą wykonywać operacje, takie jak zarządzanie ofertami, planami, usługami, przydziałami itp., przy użyciu poleceń cmdlet programu PowerShell oferowanych przez ten moduł.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-109">Operators can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="dd9a9-110">Aby dowiedzieć się więcej o poleceniach cmdlet programu PowerShell dostępnych w tym module, zobacz zawartość dokumentacji rozwiązań [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) i [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage).</span><span class="sxs-lookup"><span data-stu-id="dd9a9-110">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dd9a9-111">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="dd9a9-111">Next Steps</span></span>

* <span data-ttu-id="dd9a9-112">[Install PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Instalowanie programu PowerShell dla usługi Azure Stack)</span><span class="sxs-lookup"><span data-stu-id="dd9a9-112">[Install PowerShell for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)</span></span>
* <span data-ttu-id="dd9a9-113">[Configure PowerShell for use with Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Konfigurowanie programu PowerShell do używania z usługą Azure Stack)</span><span class="sxs-lookup"><span data-stu-id="dd9a9-113">[Configure PowerShell for use with Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)</span></span>
