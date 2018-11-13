---
title: Migrowanie skryptów programu Azure PowerShell z modułu AzureRM do modułu Az
description: Poznaj procedury i narzędzia dotyczące migracji skryptów z modułu AzureRM do nowego modułu Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274902"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="62b0e-103">Migrowanie z modułu AzureRM do modułu Az programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="62b0e-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="62b0e-104">Moduł Az zapewnia równoważność funkcji z modułem AzureRM, jednak używa krótszych i bardziej spójnych nazw poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62b0e-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="62b0e-105">Skrypty napisane dla poleceń cmdlet modułu AzureRM nie będą automatycznie działać z nowym modułem.</span><span class="sxs-lookup"><span data-stu-id="62b0e-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="62b0e-106">Aby ułatwić przejście, moduł Az oferuje narzędzia umożliwiające uruchamianie istniejących skryptów przy użyciu modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="62b0e-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="62b0e-107">Każda migracja do nowego zestawu poleceń jest kłopotliwa, jednak ten artykuł pomoże Ci rozpocząć przejście do nowego modułu.</span><span class="sxs-lookup"><span data-stu-id="62b0e-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="62b0e-108">Upewnianie się, że istniejące skrypty działają z najnowszą wersją modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="62b0e-108">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="62b0e-109">To jest najważniejszy krok!</span><span class="sxs-lookup"><span data-stu-id="62b0e-109">This is the most important step!</span></span> <span data-ttu-id="62b0e-110">Uruchom istniejące skrypty i upewnij się, że działają one z _najnowszą_ wersją modułu AzureRM (__6.12.0__).</span><span class="sxs-lookup"><span data-stu-id="62b0e-110">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.12.0__).</span></span> <span data-ttu-id="62b0e-111">Jeśli Twoje skrypty nie działają, zapoznaj się z [przewodnikiem po migracji modułu AzureRM](migration-guide.6.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="62b0e-111">If your scripts don't work, make sure to read the [AzureRM migration guide](migration-guide.6.0.0.md).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="62b0e-112">Instalowanie modułu Az programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="62b0e-112">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="62b0e-113">Pierwszym krokiem jest zainstalowanie modułu Az na Twojej platformie.</span><span class="sxs-lookup"><span data-stu-id="62b0e-113">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="62b0e-114">Aby zainstalować moduł Az, należy najpierw odinstalować moduł AzureRM.</span><span class="sxs-lookup"><span data-stu-id="62b0e-114">To install Az, you need to uninstall AzureRM.</span></span>
<span data-ttu-id="62b0e-115">W poniższych krokach opisano, co zrobić, aby istniejące skrypty nadal działały, i jak włączyć zgodność ze starymi nazwami poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62b0e-115">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="62b0e-116">Aby zainstalować moduł Az programu Azure PowerShell, wykonaj następujące kroki:</span><span class="sxs-lookup"><span data-stu-id="62b0e-116">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="62b0e-117">[Odinstaluj moduł AzureRM](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="62b0e-117">[Uninstall the AzureRM module](uninstall-azurerm-ps.md).</span></span> <span data-ttu-id="62b0e-118">Upewnij się, że usuwasz _wszystkie_ zainstalowane wersje modułu AzureRM, a nie tylko najnowszą.</span><span class="sxs-lookup"><span data-stu-id="62b0e-118">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* [<span data-ttu-id="62b0e-119">Zainstaluj moduł Az</span><span class="sxs-lookup"><span data-stu-id="62b0e-119">Install the Az module</span></span>](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><span data-ttu-id="62b0e-120"><a name="aliases"/>Włączanie trybu aliasów modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="62b0e-120"><a name="aliases"/>Enable AzureRM alias mode</span></span>

<span data-ttu-id="62b0e-121">Po upewnieniu się, że skrypty działają z najnowszą wersją modułu AzureRM, i odinstalowaniu modułu AzureRM nadszedł czas, aby włączyć tryb zgodności dla modułu Az.</span><span class="sxs-lookup"><span data-stu-id="62b0e-121">With AzureRM uninstalled and your scripts working with the latest AzureRM version, now is the time to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="62b0e-122">Zgodność należy włączyć za pomocą polecenia:</span><span class="sxs-lookup"><span data-stu-id="62b0e-122">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="62b0e-123">Aliasy umożliwiają używanie starych nazw poleceń cmdlet po zainstalowaniu modułu `Az`.</span><span class="sxs-lookup"><span data-stu-id="62b0e-123">Aliases enable the ability to use old cmdlet names with the `Az` module installed.</span></span> <span data-ttu-id="62b0e-124">Te aliasy są wpisane w profil użytkownika dla wybranego zakresu.</span><span class="sxs-lookup"><span data-stu-id="62b0e-124">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="62b0e-125">Jeśli profil użytkownika nie istnieje, jest on tworzony.</span><span class="sxs-lookup"><span data-stu-id="62b0e-125">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="62b0e-126">Dla tego polecenia można użyć innego parametru `-Scope`, ale nie jest to zalecane!</span><span class="sxs-lookup"><span data-stu-id="62b0e-126">You can use a different `-Scope` for this command, but it's not recommended!</span></span> <span data-ttu-id="62b0e-127">Aliasy są wpisane w profil użytkownika dla wybranego zakresu, dlatego włączaj je dla tak ograniczonego zakresu, jak to możliwe.</span><span class="sxs-lookup"><span data-stu-id="62b0e-127">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="62b0e-128">Włączenie aliasów dla całego systemu może także spowodować problemy dla innych użytkowników, którzy mają zainstalowany moduł `AzureRM` w swoim zakresie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="62b0e-128">Enabling aliases system-wide could also cause issues for other users which have `AzureRM` installed in their local scope.</span></span>

<span data-ttu-id="62b0e-129">Po włączeniu trybu aliasów ponownie uruchom skrypty, aby potwierdzić, że nadal działają zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="62b0e-129">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="62b0e-130">Zmienianie importów modułu i nazw poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="62b0e-130">Change module imports and cmdlet names</span></span>

<span data-ttu-id="62b0e-131">Ogólnie rzecz biorąc, nazwy modułu zostały zmienione tak, aby nazwy `AzureRM` i `Azure` stały się nazwą `Az` — to samo dotyczy poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62b0e-131">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="62b0e-132">Na przykład nazwa modułu `AzureRM.Compute` została zmieniona na `Az.Compute`.</span><span class="sxs-lookup"><span data-stu-id="62b0e-132">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="62b0e-133">Polecenie `New-AzureRmVM` stało się poleceniem `New-AzVM`, a polecenie `Get-AzureStorageBlob` to teraz polecenie `Get-AzStorageBlob`.</span><span class="sxs-lookup"><span data-stu-id="62b0e-133">`New-AzureRmVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="62b0e-134">Istnieją wyjątki od tej reguły zmiany nazw, o których należy wiedzieć przed rozpoczęciem zmieniania nazewnictwa:</span><span class="sxs-lookup"><span data-stu-id="62b0e-134">There are exceptions to this naming change that you should be aware of before doing any renaming:</span></span>

| <span data-ttu-id="62b0e-135">Moduł AzureRM</span><span class="sxs-lookup"><span data-stu-id="62b0e-135">AzureRM module</span></span> | <span data-ttu-id="62b0e-136">Moduł Az</span><span class="sxs-lookup"><span data-stu-id="62b0e-136">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="62b0e-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="62b0e-137">AzureRM.DataFactories</span></span> | <span data-ttu-id="62b0e-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="62b0e-138">Az.DataFactory</span></span> |
| <span data-ttu-id="62b0e-139">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="62b0e-139">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="62b0e-140">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="62b0e-140">Az.DataFactory</span></span> |
| <span data-ttu-id="62b0e-141">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="62b0e-141">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="62b0e-142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="62b0e-142">Az.RecoveryServices</span></span> |
| <span data-ttu-id="62b0e-143">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="62b0e-143">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="62b0e-144">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="62b0e-144">Az.RecoveryServices</span></span> |

## <a name="summary"></a><span data-ttu-id="62b0e-145">Podsumowanie</span><span class="sxs-lookup"><span data-stu-id="62b0e-145">Summary</span></span>

<span data-ttu-id="62b0e-146">Wykonując powyższe czynności, można zaktualizować wszystkie istniejące skrypty w celu korzystania z nowego modułu.</span><span class="sxs-lookup"><span data-stu-id="62b0e-146">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="62b0e-147">Jeśli masz jakiekolwiek pytania lub problemy dotyczące tych kroków, które utrudniały migrację, dodaj komentarz do tego artykułu, abyśmy mogli ulepszyć instrukcje.</span><span class="sxs-lookup"><span data-stu-id="62b0e-147">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>