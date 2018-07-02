---
title: Omówienie programu Azure PowerShell | Microsoft Docs
description: Ten temat zawiera omówienie programu Azure PowerShell oraz linki prowadzące do informacji dotyczących instalacji i konfiguracji.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: 7e728a31578989d8ce5e200491111ed9e11acba1
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238002"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="3652c-103">Omówienie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3652c-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="3652c-104">Program Azure PowerShell udostępnia zestaw poleceń cmdlet, które pozwalają zarządzać zasobami platformy Azure przy użyciu modelu usługi [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview).</span><span class="sxs-lookup"><span data-stu-id="3652c-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="3652c-105">Można go również używać w przeglądarce z usługą [Azure Cloud Shell](/azure/cloud-shell/overview) albo można go zainstalować na maszynie lokalnej i używać w dowolnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3652c-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="3652c-106">Używaj usługi [Cloud Shell](/azure/cloud-shell/overview), aby uruchamiać program Azure PowerShell w przeglądarce, albo [zainstaluj](install-azurerm-ps.md) go na swoim komputerze.</span><span class="sxs-lookup"><span data-stu-id="3652c-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="3652c-107">Następnie przeczytaj artykuł [Wprowadzenie](get-started-azureps.md), aby rozpocząć korzystanie z programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3652c-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="3652c-108">Aby uzyskać informacje o najnowszej wersji, zobacz [informacje o wersji](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="3652c-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="3652c-109">Poniższe przykłady mogą pomóc nauczyć się, jak realizować typowe scenariusze za pomocą programu Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="3652c-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="3652c-110">Maszyny wirtualne z systemem Linux</span><span class="sxs-lookup"><span data-stu-id="3652c-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3652c-111">Maszyny wirtualne z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="3652c-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3652c-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="3652c-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="3652c-113">Bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="3652c-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="3652c-114">Jeśli masz wdrożenia korzystające z klasycznego modelu wdrażania, których nie można przekonwertować, możesz zainstalować wersję zarządzania usługą programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3652c-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="3652c-115">Aby uzyskać więcej informacji, zobacz [Instalowanie modułu Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="3652c-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

### <a name="need-help-with-powershell"></a><span data-ttu-id="3652c-116">Potrzebujesz pomocy z programem PowerShell?</span><span class="sxs-lookup"><span data-stu-id="3652c-116">Need help with PowerShell?</span></span>

<span data-ttu-id="3652c-117">Jeśli nie znasz programu PowerShell, pomocne może być wprowadzenie do programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3652c-117">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="3652c-118">Instalowanie programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="3652c-118">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="3652c-119">Tworzenie skryptów przy użyciu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="3652c-119">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="3652c-120">Możesz również obejrzeć ten film wideo: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Podstawy programu PowerShell (część 1): rozpoczynanie pracy z programem PowerShell).</span><span class="sxs-lookup"><span data-stu-id="3652c-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="3652c-121">Ewentualnie skorzystaj z kursu [Wprowadzenie do programu PowerShell — szybkie rozpoczęcie pracy](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span><span class="sxs-lookup"><span data-stu-id="3652c-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="3652c-122">Inne moduły programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3652c-122">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="3652c-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="3652c-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="3652c-124">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="3652c-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="3652c-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="3652c-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="3652c-126">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="3652c-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)