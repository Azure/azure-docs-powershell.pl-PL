---
title: Omówienie programu Azure PowerShell | Microsoft Docs
description: Ten temat zawiera omówienie programu Azure PowerShell oraz linki prowadzące do informacji dotyczących instalacji i konfiguracji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 09/11/2018
ms.openlocfilehash: bdd8e69a2ea9df8b4fff100e1f3cc4c82d2d9d9d
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259714"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="e8a0f-103">Omówienie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e8a0f-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="e8a0f-104">Program Azure PowerShell udostępnia zestaw poleceń cmdlet, które pozwalają zarządzać zasobami platformy Azure przy użyciu modelu usługi [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview).</span><span class="sxs-lookup"><span data-stu-id="e8a0f-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="e8a0f-105">Można go również używać w przeglądarce z usługą [Azure Cloud Shell](/azure/cloud-shell/overview) albo można go zainstalować na maszynie lokalnej i używać w dowolnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8a0f-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="e8a0f-106">Używaj usługi [Cloud Shell](/azure/cloud-shell/overview), aby uruchamiać program Azure PowerShell w przeglądarce, albo [zainstaluj](install-azurerm-ps.md) go na swoim komputerze.</span><span class="sxs-lookup"><span data-stu-id="e8a0f-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="e8a0f-107">Następnie przeczytaj artykuł [Wprowadzenie](get-started-azureps.md), aby rozpocząć korzystanie z programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8a0f-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="e8a0f-108">Aby uzyskać informacje o najnowszej wersji, zobacz [informacje o wersji](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e8a0f-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="e8a0f-109">Poniższe przykłady mogą pomóc nauczyć się, jak realizować typowe scenariusze za pomocą programu Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e8a0f-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="e8a0f-110">Maszyny wirtualne z systemem Linux</span><span class="sxs-lookup"><span data-stu-id="e8a0f-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="e8a0f-111">Maszyny wirtualne z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="e8a0f-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="e8a0f-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="e8a0f-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="e8a0f-113">Bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e8a0f-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="learn-powershell-basics"></a><span data-ttu-id="e8a0f-114">Podstawy programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="e8a0f-114">Learn PowerShell basics</span></span>

<span data-ttu-id="e8a0f-115">Jeśli nie znasz programu PowerShell, pomocne może być wprowadzenie do programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e8a0f-115">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="e8a0f-116">Instalowanie programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="e8a0f-116">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="e8a0f-117">Tworzenie skryptów przy użyciu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="e8a0f-117">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="e8a0f-118">Możesz również obejrzeć ten film wideo: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Podstawy programu PowerShell (część 1): rozpoczynanie pracy z programem PowerShell).</span><span class="sxs-lookup"><span data-stu-id="e8a0f-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="e8a0f-119">Ewentualnie skorzystaj z kursu [Wprowadzenie do programu PowerShell — szybkie rozpoczęcie pracy](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span><span class="sxs-lookup"><span data-stu-id="e8a0f-119">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="e8a0f-120">Rozwijanie umiejętności dzięki środowisku Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="e8a0f-120">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="e8a0f-121">Automatyzowanie zadań platformy Azure za pomocą skryptów programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="e8a0f-121">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="e8a0f-122">Więcej interakcyjnych zasobów szkoleniowych...</span><span class="sxs-lookup"><span data-stu-id="e8a0f-122">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="e8a0f-123">Inne moduły programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e8a0f-123">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="e8a0f-124">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e8a0f-124">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="e8a0f-125">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="e8a0f-125">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="e8a0f-126">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e8a0f-126">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="e8a0f-127">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="e8a0f-127">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
