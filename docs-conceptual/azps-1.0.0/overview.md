---
title: Omówienie programu Azure PowerShell
description: Omówienie modułu Az programu Azure PowerShell wraz z informacjami na temat instalowania i rozpoczynania pracy.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736464"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="c00e2-103">Omówienie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c00e2-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="c00e2-104">Program Azure PowerShell udostępnia zestaw poleceń cmdlet, które pozwalają zarządzać zasobami platformy Azure przy użyciu modelu usługi [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview).</span><span class="sxs-lookup"><span data-stu-id="c00e2-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="c00e2-105">Program Azure PowerShell używa platformy .NET Standard, dzięki czemu jest dostępny dla systemów Windows, macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="c00e2-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="c00e2-106">Program Azure PowerShell jest również dostępny w usłudze Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="c00e2-106">Azure PowerShell is also available from Azure Cloud Shell.</span></span>

<span data-ttu-id="c00e2-107">Używaj usługi [Azure Cloud Shell](/azure/cloud-shell/overview), aby uruchamiać program Azure PowerShell w przeglądarce, albo [zainstaluj go w środowisku lokalnym](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="c00e2-107">Use [Azure Cloud Shell](/azure/cloud-shell/overview) to run Azure PowerShell in your browser, or [install locally](install-az-ps.md).</span></span> <span data-ttu-id="c00e2-108">Zapoznaj się z artykułem [Wprowadzenie](get-started-azureps.md), aby poznać podstawy programu Azure PowerShell i rozpocząć pracę z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c00e2-108">Check out the [Get Started](get-started-azureps.md) article to learn the Azure PowerShell basics and get started with Azure.</span></span>

<span data-ttu-id="c00e2-109">Aby uzyskać informacje o najnowszej wersji programu Azure PowerShell, zobacz [informacje o wersji](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c00e2-109">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="c00e2-110">Informacje o nowym module Az</span><span class="sxs-lookup"><span data-stu-id="c00e2-110">About the new Az module</span></span>

<span data-ttu-id="c00e2-111">W tej dokumentacji opisano nowy moduł Az programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c00e2-111">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="c00e2-112">Ten nowy moduł został napisany od podstaw na platformie .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="c00e2-112">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="c00e2-113">Dzięki użyciu platformy .NET Standard program Azure PowerShell może działać w ramach programu PowerShell 5.x w systemie Windows lub programu PowerShell 6 na dowolnej platformie.</span><span class="sxs-lookup"><span data-stu-id="c00e2-113">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="c00e2-114">Interakcja z platformą Azure za pośrednictwem programu PowerShell powinna się teraz odbywać za pomocą modułu Az.</span><span class="sxs-lookup"><span data-stu-id="c00e2-114">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="c00e2-115">Usterki w module AzureRM będą nadal usuwane, ale nie będą już w nim wprowadzane żadne nowe funkcje.</span><span class="sxs-lookup"><span data-stu-id="c00e2-115">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="c00e2-116">Szczegółowe informacje dotyczące nowego modułu, w tym zmienione nazwy poleceń i plany konserwacji modułu AzureRM, znajdują się w artykule [Wprowadzenie do modułu Az programu Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="c00e2-116">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="c00e2-117">Jeśli od razu chcesz rozpocząć pracę przy użyciu nowego modułu, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="c00e2-117">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="c00e2-118">Dostępna jest także [dokumentacja modułu AzureRM](/powershell/azure/azurerm).</span><span class="sxs-lookup"><span data-stu-id="c00e2-118">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="c00e2-119">Dokumentacja platformy Azure jest aktualizowana w celu odzwierciedlenia nowych nazw poleceń cmdlet modułu, ale artykuły mogą nadal zawierać polecenia modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="c00e2-119">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="c00e2-120">Po zainstalowaniu modułu Az zaleca się włączenie aliasów poleceń cmdlet modułu AzureRM za pomocą polecenia `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="c00e2-120">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="c00e2-121">Więcej szczegółów znajduje się w artykule [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="c00e2-121">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="common-scenarios"></a><span data-ttu-id="c00e2-122">Typowe scenariusze</span><span class="sxs-lookup"><span data-stu-id="c00e2-122">Common scenarios</span></span>

<span data-ttu-id="c00e2-123">Poniższe przykłady mogą pomóc nauczyć się, jak realizować typowe scenariusze za pomocą programu Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c00e2-123">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="c00e2-124">Maszyny wirtualne z systemem Linux</span><span class="sxs-lookup"><span data-stu-id="c00e2-124">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="c00e2-125">Maszyny wirtualne z systemem Windows</span><span class="sxs-lookup"><span data-stu-id="c00e2-125">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="c00e2-126">Web Apps</span><span class="sxs-lookup"><span data-stu-id="c00e2-126">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="c00e2-127">Bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c00e2-127">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="c00e2-128">Podstawy programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="c00e2-128">Learn PowerShell basics</span></span>

<span data-ttu-id="c00e2-129">Jeśli nie znasz programu PowerShell, pomocne może być wprowadzenie.</span><span class="sxs-lookup"><span data-stu-id="c00e2-129">If you're unfamiliar with PowerShell, an introduction may be helpful.</span></span>

* [<span data-ttu-id="c00e2-130">Instalowanie programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="c00e2-130">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="c00e2-131">Tworzenie skryptów przy użyciu programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="c00e2-131">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="c00e2-132">Możesz również obejrzeć to wideo: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Podstawy programu PowerShell, część 1: Wprowadzenie do programu PowerShell).</span><span class="sxs-lookup"><span data-stu-id="c00e2-132">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="c00e2-133">Ewentualnie skorzystaj z kursu [Wprowadzenie do programu PowerShell — szybkie rozpoczęcie pracy](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span><span class="sxs-lookup"><span data-stu-id="c00e2-133">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="c00e2-134">Rozwijanie umiejętności dzięki środowisku Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="c00e2-134">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="c00e2-135">Automatyzowanie zadań platformy Azure za pomocą skryptów programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="c00e2-135">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="c00e2-136">Więcej interakcyjnych zasobów szkoleniowych...</span><span class="sxs-lookup"><span data-stu-id="c00e2-136">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="c00e2-137">Inne moduły programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c00e2-137">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="c00e2-138">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c00e2-138">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="c00e2-139">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="c00e2-139">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="c00e2-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c00e2-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="c00e2-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="c00e2-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
