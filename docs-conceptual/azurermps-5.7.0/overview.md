---
title: Omówienie programu Azure PowerShell | Microsoft Docs
description: Ten temat zawiera omówienie programu Azure PowerShell oraz linki prowadzące do informacji dotyczących instalacji i konfiguracji.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7d220266bd6e36fd083f56290cb6cee8f2e80d3e
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243705"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="fed1b-103">Omówienie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fed1b-103">Overview of Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="fed1b-104">Program Azure PowerShell udostępnia zestaw poleceń cmdlet, które pozwalają zarządzać zasobami platformy Azure przy użyciu modelu usługi [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview).</span><span class="sxs-lookup"><span data-stu-id="fed1b-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="fed1b-105">Można go również używać w przeglądarce z usługą [Azure Cloud Shell](/azure/cloud-shell/overview) albo można go zainstalować na maszynie lokalnej i używać w dowolnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fed1b-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="fed1b-106">Używaj usługi [Cloud Shell](/azure/cloud-shell/overview), aby uruchamiać program Azure PowerShell w przeglądarce, albo [zainstaluj](install-azurerm-ps.md) go na swoim komputerze.</span><span class="sxs-lookup"><span data-stu-id="fed1b-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="fed1b-107">Następnie przeczytaj artykuł [Wprowadzenie](get-started-azureps.md), aby rozpocząć korzystanie z programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fed1b-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="fed1b-108">Aby uzyskać informacje o najnowszej wersji, zobacz [informacje o wersji](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="fed1b-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="fed1b-109">Poniższe przykłady mogą pomóc nauczyć się, jak realizować typowe scenariusze za pomocą programu Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="fed1b-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

- [<span data-ttu-id="fed1b-110">Maszyny wirtualne z systemem Linux</span><span class="sxs-lookup"><span data-stu-id="fed1b-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="fed1b-111">Maszyny wirtualne z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="fed1b-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="fed1b-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="fed1b-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
- [<span data-ttu-id="fed1b-113">Bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="fed1b-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="fed1b-114">Podstawy programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="fed1b-114">Learn PowerShell basics</span></span>

<span data-ttu-id="fed1b-115">Jeśli nie znasz programu PowerShell, pomocne może być wprowadzenie do programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fed1b-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

- [<span data-ttu-id="fed1b-116">Instalowanie programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="fed1b-116">Installing PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
- [<span data-ttu-id="fed1b-117">Zasoby szkoleniowe dotyczące programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="fed1b-117">PowerShell learning resources</span></span>](/powershell/scripting/learn/more-powershell-learning)

<span data-ttu-id="fed1b-118">Możesz również obejrzeć to wideo: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Podstawy programu PowerShell, część 1: Wprowadzenie do programu PowerShell).</span><span class="sxs-lookup"><span data-stu-id="fed1b-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="fed1b-119">Inne moduły programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fed1b-119">Other Azure PowerShell modules</span></span>

- [<span data-ttu-id="fed1b-120">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fed1b-120">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
- [<span data-ttu-id="fed1b-121">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="fed1b-121">Azure Information Protection</span></span>](/powershell/azure/aip/)
- [<span data-ttu-id="fed1b-122">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fed1b-122">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
- [<span data-ttu-id="fed1b-123">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="fed1b-123">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
