---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b42ad6f22f47e10c9190cf5a919f781375ff26f2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a><span data-ttu-id="d2a86-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="d2a86-103">Release notes</span></span>

<span data-ttu-id="d2a86-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="d2a86-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="d2a86-105">Wersja 1.2.9</span><span class="sxs-lookup"><span data-stu-id="d2a86-105">Version 1.2.9</span></span>

<span data-ttu-id="d2a86-106">Zmiany w tej wersji</span><span class="sxs-lookup"><span data-stu-id="d2a86-106">Changes This Release</span></span>

* <span data-ttu-id="d2a86-107">Moduł AzureRm.AzureStackAdmin</span><span class="sxs-lookup"><span data-stu-id="d2a86-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="d2a86-108">Zmiany w poleceniu cmdlet Add-AzureRmResourceProviderRegistration w celu obsługi podziału na administratora usługi Azure Resource Manager i dzierżawę usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d2a86-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="d2a86-109">Został dodany nowy parametr -ResourceManagerType.</span><span class="sxs-lookup"><span data-stu-id="d2a86-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="d2a86-110">Z każdego polecenia cmdlet usunięto parametry -AdminUri, -ApiVersion, -SubscriptionId i -Token.</span><span class="sxs-lookup"><span data-stu-id="d2a86-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="d2a86-111">Generowane były ostrzeżenia, że te parametry zostaną wycofane, a teraz zostały one usunięte.</span><span class="sxs-lookup"><span data-stu-id="d2a86-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="d2a86-112">Moduł AzureStackStorage</span><span class="sxs-lookup"><span data-stu-id="d2a86-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="d2a86-113">Dodano nowe polecenia cmdlet do obsługi scenariuszy migracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="d2a86-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="d2a86-114">Usunięto polecenia cmdlet odwołujące się do wewnętrznych składników i podstawowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="d2a86-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="d2a86-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="d2a86-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="d2a86-116">Utworzono nowy moduł do zarządzania wersjami poleceń cmdlet programu Azure PowerShell przy użyciu profilów wersji</span><span class="sxs-lookup"><span data-stu-id="d2a86-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>