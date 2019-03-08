---
title: Omówienie programu Azure PowerShell
description: Omówienie modułu Az programu Azure PowerShell wraz z informacjami na temat instalowania i rozpoczynania pracy.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 45ab083dd133c8c7b8dbe902484c92564bc216b9
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837201"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="9ad77-103">Omówienie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9ad77-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="9ad77-104">Program Azure PowerShell udostępnia zestaw poleceń cmdlet, które pozwalają zarządzać zasobami platformy Azure przy użyciu modelu usługi [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview).</span><span class="sxs-lookup"><span data-stu-id="9ad77-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="9ad77-105">Program Azure PowerShell używa platformy .NET Standard, dzięki czemu jest dostępny dla systemów Windows, macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="9ad77-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="9ad77-106">Program Azure PowerShell jest również dostępny w usłudze Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="9ad77-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="9ad77-107">Informacje o nowym module Az</span><span class="sxs-lookup"><span data-stu-id="9ad77-107">About the new Az module</span></span>

<span data-ttu-id="9ad77-108">W tej dokumentacji opisano nowy moduł Az programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ad77-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="9ad77-109">Ten nowy moduł został napisany od podstaw na platformie .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="9ad77-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="9ad77-110">Dzięki użyciu platformy .NET Standard program Azure PowerShell może działać w ramach programu PowerShell 5 w systemie Windows lub programu PowerShell 6 na dowolnej platformie.</span><span class="sxs-lookup"><span data-stu-id="9ad77-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5 on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="9ad77-111">Interakcja z platformą Azure za pośrednictwem programu PowerShell powinna się teraz odbywać za pomocą modułu Az.</span><span class="sxs-lookup"><span data-stu-id="9ad77-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="9ad77-112">Usterki w module AzureRM będą nadal usuwane, ale nie będą już w nim wprowadzane żadne nowe funkcje.</span><span class="sxs-lookup"><span data-stu-id="9ad77-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="9ad77-113">Szczegółowe informacje dotyczące nowego modułu, w tym zmienione nazwy poleceń i plany konserwacji modułu AzureRM, znajdują się w artykule [Wprowadzenie do modułu Az programu Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="9ad77-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="9ad77-114">Jeśli od razu chcesz rozpocząć pracę przy użyciu nowego modułu, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="9ad77-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="9ad77-115">Dostępna jest także [dokumentacja modułu AzureRM](/powershell/azure/azurerm).</span><span class="sxs-lookup"><span data-stu-id="9ad77-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="9ad77-116">Dokumentacja platformy Azure jest aktualizowana w celu odzwierciedlenia nowych nazw poleceń cmdlet modułu, ale artykuły mogą nadal zawierać polecenia modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="9ad77-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="9ad77-117">Po zainstalowaniu modułu Az zaleca się włączenie aliasów poleceń cmdlet modułu AzureRM za pomocą polecenia `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="9ad77-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="9ad77-118">Więcej szczegółów znajduje się w artykule [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="9ad77-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="9ad77-119">Uruchamianie lub instalowanie</span><span class="sxs-lookup"><span data-stu-id="9ad77-119">Run or install</span></span>

<span data-ttu-id="9ad77-120">Program Azure PowerShell można zainstalować w programie PowerShell 5.1 lub nowszym w systemie Windows, w programie PowerShell 6 na dowolnej platformie albo uruchamiać w usłudze Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="9ad77-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell 6 on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="9ad77-121">Aby uruchomić program w przeglądarce przy użyciu usługi Azure Cloud Shell, zobacz [Przewodnik Szybki start dotyczący programu PowerShell w usłudze Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="9ad77-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="9ad77-122">Aby zainstalować program Azure PowerShell w swoim systemie, zobacz [Instalowanie programu Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="9ad77-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="9ad77-123">Aby uzyskać informacje o najnowszej wersji programu Azure PowerShell, zobacz [informacje o wersji](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9ad77-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="9ad77-124">Rozpoczęcie pracy</span><span class="sxs-lookup"><span data-stu-id="9ad77-124">Get Started</span></span>

<span data-ttu-id="9ad77-125">Przeczytaj artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md), aby poznać podstawy programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ad77-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="9ad77-126">Jeśli nie znasz programu PowerShell, pomocne może być wprowadzenie:</span><span class="sxs-lookup"><span data-stu-id="9ad77-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="9ad77-127">Instalowanie programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="9ad77-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="9ad77-128">Tworzenie skryptów przy użyciu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="9ad77-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* <span data-ttu-id="9ad77-129">[PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Podstawy programu PowerShell, część 1: Wprowadzenie do programu PowerShell)</span><span class="sxs-lookup"><span data-stu-id="9ad77-129">[PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)</span></span>
* <span data-ttu-id="9ad77-130">Kurs [Wprowadzenie do programu PowerShell — szybkie rozpoczęcie pracy](https://mva.microsoft.com/liveevents/powershell-jumpstart) w witrynie Microsoft Virtual Academy</span><span class="sxs-lookup"><span data-stu-id="9ad77-130">Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span></span>

<span data-ttu-id="9ad77-131">Poniższe przykłady mogą pomóc w przypadku niektórych typowych zastosowań platformy Azure:</span><span class="sxs-lookup"><span data-stu-id="9ad77-131">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="9ad77-132">Maszyny wirtualne z systemem Linux</span><span class="sxs-lookup"><span data-stu-id="9ad77-132">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9ad77-133">Maszyny wirtualne z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="9ad77-133">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9ad77-134">Web Apps</span><span class="sxs-lookup"><span data-stu-id="9ad77-134">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9ad77-135">Bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="9ad77-135">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="9ad77-136">Rozwijanie umiejętności dzięki środowisku Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="9ad77-136">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="9ad77-137">Automatyzowanie zadań platformy Azure za pomocą skryptów programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="9ad77-137">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="9ad77-138">Więcej interakcyjnych zasobów szkoleniowych...</span><span class="sxs-lookup"><span data-stu-id="9ad77-138">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="9ad77-139">Inne moduły programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9ad77-139">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="9ad77-140">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9ad77-140">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="9ad77-141">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9ad77-141">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="9ad77-142">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="9ad77-142">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)