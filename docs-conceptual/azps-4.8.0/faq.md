---
title: Często zadawane pytania
description: Często zadawane pytania dotyczące usługi Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002264"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="986c2-103">Często zadawane pytania dotyczące usługi Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="986c2-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="986c2-104">Co to jest Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="986c2-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="986c2-105">Azure PowerShell to zestaw poleceń cmdlet, który umożliwia zarządzanie zasobami platformy Azure bezpośrednio przy użyciu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="986c2-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="986c2-106">W grudniu 2018 r. moduł Az programu PowerShell stał się ogólnie dostępny.</span><span class="sxs-lookup"><span data-stu-id="986c2-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="986c2-107">Jest to teraz zalecany moduł programu PowerShell na potrzeby interakcji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="986c2-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="986c2-108">Aby dowiedzieć się więcej na temat modułu Az programu PowerShell, zobacz [Wprowadzenie do nowego modułu Az usługi Azure PowerShell](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="986c2-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="986c2-109">Jak mogę wyłączyć komunikaty ostrzegawcze o zmianach powodujących niezgodność w usłudze Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="986c2-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="986c2-110">Aby pomijać komunikaty ostrzegawcze o zmianach powodujących niezgodność w usłudze Azure PowerShell, należy ustawić zmienną środowiskową `SuppressAzurePowerShellBreakingChangeWarnings` na wartość `true`.</span><span class="sxs-lookup"><span data-stu-id="986c2-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
