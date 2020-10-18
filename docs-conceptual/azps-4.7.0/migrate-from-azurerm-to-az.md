---
title: Migrowanie skryptów programu Azure PowerShell z modułu AzureRM do modułu Az
description: Poznaj procedury i narzędzia dotyczące migracji skryptów z modułu AzureRM do nowego modułu Az.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001567"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="dcae7-103">Migrowanie programu Azure PowerShell z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="dcae7-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="dcae7-104">Wszystkie wersje modułu AzureRM PowerShell są nieaktualne, ale nie są pozbawione pomocy technicznej.</span><span class="sxs-lookup"><span data-stu-id="dcae7-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="dcae7-105">[Moduł Az programu PowerShell](install-az-ps.md) jest obecnie zalecanym modułem programu PowerShell na potrzeby interakcji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcae7-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="dcae7-106">Skrypty napisane dla poleceń cmdlet modułu AzureRM nie będą automatycznie działać z nowym modułem.</span><span class="sxs-lookup"><span data-stu-id="dcae7-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="dcae7-107">Aby ułatwić przeniesienie, opracowano [zestaw narzędzi do migracji modułu AzureRM do Az](https://github.com/Azure/azure-powershell-migration).</span><span class="sxs-lookup"><span data-stu-id="dcae7-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="dcae7-108">Każda migracja do nowego zestawu poleceń jest kłopotliwa, jednak ten artykuł pomoże Ci rozpocząć przejście do modułu Az programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dcae7-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="dcae7-109">Aby dowiedzieć się więcej na temat przyczyn utworzenia modułu Az programu PowerShell, zobacz [Wprowadzenie do nowego modułu Az usługi Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="dcae7-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="dcae7-110">Aby wyświetlić pełną listę zmian powodujących niezgodność między modułami AzureRM i Az, zobacz [wszystkie różnice między modułem AzureRM i Az](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="dcae7-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="dcae7-111">Upewnianie się, że istniejące skrypty działają z najnowszą wersją modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="dcae7-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="dcae7-112">Przed wykonaniem jakichkolwiek kroków związanych z migracją sprawdź, które wersje modułu AzureRM są zainstalowane w systemie.</span><span class="sxs-lookup"><span data-stu-id="dcae7-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="dcae7-113">Dzięki temu możesz się upewnić, że skrypty są już uruchamiane w najnowszej wersji, i dowiedzieć, które wersje modułu AzureRM muszą zostać odinstalowane.</span><span class="sxs-lookup"><span data-stu-id="dcae7-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="dcae7-114">Aby sprawdzić, które wersje modułu AzureRM są zainstalowane, uruchom następujący przykład:</span><span class="sxs-lookup"><span data-stu-id="dcae7-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="dcae7-115">**Najnowszą** dostępną wersją modułu AzureRM jest wersja **6.13.1**.</span><span class="sxs-lookup"><span data-stu-id="dcae7-115">The **latest** available release of AzureRM is **6.13.1**.</span></span> <span data-ttu-id="dcae7-116">Jeśli ta wersja nie jest zainstalowana, może być konieczne dodatkowe zmodyfikowanie istniejących skryptów, aby działały z modułem Az, w sposób wykraczający poza zmiany opisane w tym artykule i na [liście zmian powodujących niezgodność](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="dcae7-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="dcae7-117">Jeśli skrypty nie działają z wersją 6.13.1 modułu AzureRM, zaktualizuj je zgodnie z [przewodnikiem migracji modułu AzureRM z wersji 5.x do wersji 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).</span><span class="sxs-lookup"><span data-stu-id="dcae7-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="dcae7-118">Jeśli używasz wcześniejszej wersji modułu AzureRM, dostępne są przewodniki migracji dla wszystkich wersji głównych.</span><span class="sxs-lookup"><span data-stu-id="dcae7-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="dcae7-119">Instalowanie zestawu narzędzi do migracji modułu AzureRM do Az</span><span class="sxs-lookup"><span data-stu-id="dcae7-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="dcae7-120">Automatyczna migracja skryptów programu PowerShell</span><span class="sxs-lookup"><span data-stu-id="dcae7-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="dcae7-121">Za pomocą zestawu narzędzi do migracji modułu AzureRM do Az można wygenerować plan określający, jakie zmiany zostaną wykonane w skryptach przed wprowadzeniem jakichkolwiek modyfikacji i przed zainstalowaniem modułu Az programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dcae7-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="dcae7-122">Przewodnik Szybki start [Automatyczne migrowanie skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) przeprowadzi Cię przez cały proces automatycznego aktualizowania skryptów programu PowerShell z modułu AzureRM do Az programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dcae7-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dcae7-123">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="dcae7-123">Next steps</span></span>

<span data-ttu-id="dcae7-124">[Instalowanie programu Azure PowerShell](install-az-ps.md)
[Odinstalowywanie modułu AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="dcae7-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>
