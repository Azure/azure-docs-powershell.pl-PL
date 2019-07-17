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
ms.openlocfilehash: 0541975e55620a8792c0d51213c4ed02ea29988f
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863407"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="62e8f-103">Omówienie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="62e8f-103">Overview of Azure PowerShell</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

<span data-ttu-id="62e8f-104">Program Azure PowerShell udostępnia zestaw poleceń cmdlet, które pozwalają zarządzać zasobami platformy Azure przy użyciu modelu usługi [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview).</span><span class="sxs-lookup"><span data-stu-id="62e8f-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="62e8f-105">Można go również używać w przeglądarce z usługą [Azure Cloud Shell](/azure/cloud-shell/overview) albo można go zainstalować na maszynie lokalnej i używać w dowolnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="62e8f-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="62e8f-106">Używaj usługi [Cloud Shell](/azure/cloud-shell/overview), aby uruchamiać program Azure PowerShell w przeglądarce, albo [zainstaluj](install-azurerm-ps.md) go na swoim komputerze.</span><span class="sxs-lookup"><span data-stu-id="62e8f-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="62e8f-107">Następnie przeczytaj artykuł [Wprowadzenie](get-started-azureps.md), aby rozpocząć korzystanie z programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="62e8f-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="62e8f-108">Aby uzyskać informacje o najnowszej wersji, zobacz [informacje o wersji](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="62e8f-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="62e8f-109">Poniższe przykłady mogą pomóc nauczyć się, jak realizować typowe scenariusze za pomocą programu Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="62e8f-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="62e8f-110">Maszyny wirtualne z systemem Linux</span><span class="sxs-lookup"><span data-stu-id="62e8f-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="62e8f-111">Maszyny wirtualne z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="62e8f-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="62e8f-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="62e8f-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="62e8f-113">Bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="62e8f-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="62e8f-114">Podstawy programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="62e8f-114">Learn PowerShell basics</span></span>

<span data-ttu-id="62e8f-115">Jeśli nie znasz programu PowerShell, pomocne może być wprowadzenie do programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="62e8f-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="62e8f-116">Instalowanie programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="62e8f-116">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="62e8f-117">Tworzenie skryptów przy użyciu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="62e8f-117">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="62e8f-118">Możesz również obejrzeć to wideo: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Podstawy programu PowerShell, część 1: Wprowadzenie do programu PowerShell).</span><span class="sxs-lookup"><span data-stu-id="62e8f-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="62e8f-119">Inne moduły programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="62e8f-119">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="62e8f-120">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="62e8f-120">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="62e8f-121">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="62e8f-121">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="62e8f-122">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="62e8f-122">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="62e8f-123">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="62e8f-123">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
