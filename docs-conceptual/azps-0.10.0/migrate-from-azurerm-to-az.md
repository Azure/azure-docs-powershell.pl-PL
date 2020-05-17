---
title: Migrowanie skryptów programu Azure PowerShell z modułu AzureRM do modułu Az
description: Poznaj procedury i narzędzia dotyczące migracji skryptów z modułu AzureRM do nowego modułu Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 02b39653ebb4aa0f74d2340a7be7b35e08d5e44d
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2020
ms.locfileid: "81446040"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="66880-103">Migrowanie programu Azure PowerShell z modułu AzureRM do modułu Az</span><span class="sxs-lookup"><span data-stu-id="66880-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="66880-104">Moduł Az zapewnia równoważność funkcji z modułem AzureRM, jednak używa krótszych i bardziej spójnych nazw poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66880-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="66880-105">Skrypty napisane dla poleceń cmdlet modułu AzureRM nie będą automatycznie działać z nowym modułem.</span><span class="sxs-lookup"><span data-stu-id="66880-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="66880-106">Aby ułatwić przejście, moduł Az oferuje narzędzia umożliwiające uruchamianie istniejących skryptów przy użyciu modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="66880-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="66880-107">Każda migracja do nowego zestawu poleceń jest kłopotliwa, jednak ten artykuł pomoże Ci rozpocząć przejście do nowego modułu.</span><span class="sxs-lookup"><span data-stu-id="66880-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

<span data-ttu-id="66880-108">Aby wyświetlić pełną listę zmian powodujących niezgodność między modułami AzureRM i Az, zobacz [wszystkie różnice między modułem AzureRM i Az](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="66880-108">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="66880-109">Upewnianie się, że istniejące skrypty działają z najnowszą wersją modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="66880-109">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="66880-110">Przed wykonaniem jakichkolwiek kroków związanych z migracją sprawdź, które wersje modułu AzureRM są zainstalowane w systemie.</span><span class="sxs-lookup"><span data-stu-id="66880-110">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span> <span data-ttu-id="66880-111">Dzięki temu możesz się upewnić, że skrypty są już uruchamiane w najnowszej wersji, i dowiedzieć, które wersje modułu AzureRM muszą zostać odinstalowane.</span><span class="sxs-lookup"><span data-stu-id="66880-111">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="66880-112">Aby sprawdzić, które wersje modułu AzureRM są zainstalowane, uruchom polecenie:</span><span class="sxs-lookup"><span data-stu-id="66880-112">To check which version(s) of AzureRM you have installed, run the command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

<span data-ttu-id="66880-113">__Najnowszą__ dostępną wersją modułu AzureRM jest wersja __6.13.1__.</span><span class="sxs-lookup"><span data-stu-id="66880-113">The __latest__ available release of AzureRM is __6.13.1__.</span></span> <span data-ttu-id="66880-114">Jeśli ta wersja nie jest zainstalowana, może być konieczne dodatkowe zmodyfikowanie istniejących skryptów, aby działały z modułem Az, w sposób wykraczający poza zmiany opisane tutaj i na [liście zmian powodujących niezgodność](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="66880-114">If you don't have this version installed, your existing scripts may need additional modification to work with the Az module beyond what's described here and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="66880-115">Jeśli skrypty nie działają z wersją 6.13.1 modułu AzureRM, zaktualizuj je zgodnie z [przewodnikiem migracji modułu AzureRM z wersji 5.x do wersji 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).</span><span class="sxs-lookup"><span data-stu-id="66880-115">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span>
<span data-ttu-id="66880-116">Jeśli używasz wcześniejszej wersji modułu AzureRM, dostępne są przewodniki migracji dla wszystkich wersji głównych.</span><span class="sxs-lookup"><span data-stu-id="66880-116">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="uninstall-azurerm"></a><span data-ttu-id="66880-117">Odinstalowywanie modułu AzureRM</span><span class="sxs-lookup"><span data-stu-id="66880-117">Uninstall AzureRM</span></span>

<span data-ttu-id="66880-118">Zgodność modułu Az z wszelkimi istniejącymi instalacjami modułu AzureRM w programie PowerShell 5.1 dla systemu Windows nie jest gwarantowana.</span><span class="sxs-lookup"><span data-stu-id="66880-118">The Az module is not guaranteed to be compatible with any existing AzureRM installs in PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="66880-119">Przed zainstalowaniem modułu Az [odinstaluj moduł AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="66880-119">Before you install the Az module, [uninstall AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="66880-120">Jeśli nie chcesz jeszcze usuwać modułu AzureRM z systemu, możesz zamiast tego zainstalować moduł Az dla programu [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) w wersji 6.x lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="66880-120">If you're not ready to remove the AzureRM module from your system, you can install the Az module for [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x or later instead.</span></span> <span data-ttu-id="66880-121">Programy PowerShell Core i PowerShell 5.1 dla systemu Windows korzystają z różnych bibliotek modułów, więc nie wystąpią żadne konflikty.</span><span class="sxs-lookup"><span data-stu-id="66880-121">PowerShell Core and PowerShell 5.1 for Windows use different module libraries, so there will be no conflicts.</span></span> <span data-ttu-id="66880-122">Nadal możesz [włączyć aliasy](#enable-azurerm-compatibility-aliases) w programie PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="66880-122">You can still [enable aliases](#enable-azurerm-compatibility-aliases) in PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="66880-123">Instalowanie modułu Az programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="66880-123">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="66880-124">Pierwszym krokiem jest zainstalowanie modułu Az na Twojej platformie.</span><span class="sxs-lookup"><span data-stu-id="66880-124">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="66880-125">Po zainstalowaniu modułu Az zaleca się odinstalowanie modułu AzureRM.</span><span class="sxs-lookup"><span data-stu-id="66880-125">When you install Az, it's recommended that you uninstall AzureRM.</span></span> <span data-ttu-id="66880-126">W poniższych krokach opisano, co zrobić, aby istniejące skrypty nadal działały, i jak włączyć zgodność ze starymi nazwami poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66880-126">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="66880-127">Aby zainstalować moduł Az programu Azure PowerShell, postępuj zgodnie z instrukcjami w artykule [Instalowanie modułu Az](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="66880-127">To install the Azure PowerShell Az module, follow the instructions in [Install the Az module](install-az-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="66880-128">W tym momencie możesz uruchomić polecenie cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) udostępnione w module Az, aby upewnić się, że wszystkie wersje modułu AzureRM zostały odinstalowane i nie będą powodować konfliktów.</span><span class="sxs-lookup"><span data-stu-id="66880-128">At this point, you might want to run the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet provided in the Az module, just to make sure that all versions of AzureRM have been uninstalled and won't cause conflicts.</span></span>

## <a name="enable-azurerm-compatibility-aliases"></a><span data-ttu-id="66880-129">Włączanie aliasów zapewniających zgodność z modułem AzureRM</span><span class="sxs-lookup"><span data-stu-id="66880-129">Enable AzureRM compatibility aliases</span></span>

<span data-ttu-id="66880-130">Po upewnieniu się, że skrypty działają z najnowszą wersją modułu AzureRM, i odinstalowaniu modułu AzureRM następny krok to włączenie trybu zgodności dla modułu Az.</span><span class="sxs-lookup"><span data-stu-id="66880-130">With AzureRM uninstalled and your scripts working with the latest AzureRM version, the next step is to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="66880-131">Zgodność należy włączyć za pomocą polecenia:</span><span class="sxs-lookup"><span data-stu-id="66880-131">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="66880-132">Aliasy umożliwiają używanie starych nazw poleceń cmdlet po zainstalowaniu modułu Az.</span><span class="sxs-lookup"><span data-stu-id="66880-132">Aliases enable the ability to use old cmdlet names with the Az module installed.</span></span> <span data-ttu-id="66880-133">Te aliasy są zapisywane w profilu dla wybranego zakresu.</span><span class="sxs-lookup"><span data-stu-id="66880-133">These aliases are written to the profile for the selected scope.</span></span> <span data-ttu-id="66880-134">Jeśli profil nie istnieje, zostanie utworzony.</span><span class="sxs-lookup"><span data-stu-id="66880-134">If no profile exists, one is created.</span></span>
<span data-ttu-id="66880-135">W przypadku użycia parametru `-Scope` określającego zakres szerszy niż `CurrentUser` wymagane są uprawnienia niezbędne do utworzenia lub zaktualizowania odpowiedniego pliku profilu.</span><span class="sxs-lookup"><span data-stu-id="66880-135">When using a `-Scope` broader than `CurrentUser`, the appropriate permissions are required to create or update the corresponding profile file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66880-136">Aliasy są tworzone __tylko__ dla nazw poleceń. Nie są tworzone aliasy nazw modułów.</span><span class="sxs-lookup"><span data-stu-id="66880-136">__Only__ cmdlet names are aliased - module names aren't!</span></span> <span data-ttu-id="66880-137">Jeśli używasz instrukcji `#Requires` lub `Import-Module`, list zależności w pliku `.psd1` albo w pełni kwalifikowanych nazw poleceń cmdlet, koniecznie przeprowadź ich migrację na tym etapie, zgodnie z procesem omówionym w sekcji dotyczącej nazw modułów artykułu z [listą zmian powodujących niezgodność](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="66880-137">If you're using `#Requires`, `Import-Module`, dependency lists in a `.psd1`, or fully-qualified cmdlet names, make sure that you migrate them at this point by following the process outlined in the [breaking changes list](migrate-az-1.0.0.md) regarding module names.</span></span>

> [!WARNING]
>
> <span data-ttu-id="66880-138">Dla tego polecenia możesz użyć innego parametru `-Scope`, ale nie jest to zalecane.</span><span class="sxs-lookup"><span data-stu-id="66880-138">You can use a different `-Scope` for this command, but it's not recommended.</span></span> <span data-ttu-id="66880-139">Aliasy są wpisane w profil użytkownika dla wybranego zakresu, dlatego włączaj je dla tak ograniczonego zakresu, jak to możliwe.</span><span class="sxs-lookup"><span data-stu-id="66880-139">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="66880-140">Włączenie aliasów dla całego systemu może spowodować problemy dla innych użytkowników, którzy mają moduł AzureRM zainstalowany w swoim zakresie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="66880-140">Enabling aliases system-wide can cause issues for other users who have AzureRM installed in their local scope.</span></span>

<span data-ttu-id="66880-141">Po włączeniu trybu aliasów ponownie uruchom skrypty, aby potwierdzić, że nadal działają zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="66880-141">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span>
<span data-ttu-id="66880-142">Niektóre nazwy parametrów zostały zmienione lub dodane albo stały się wymagane przez moduł Az.</span><span class="sxs-lookup"><span data-stu-id="66880-142">Some parameter names have been changed, added, or made required by the Az module.</span></span> <span data-ttu-id="66880-143">Ponadto mogły ulec zmianie typy danych wyjściowych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66880-143">Output types of cmdlets may have changed as well.</span></span> <span data-ttu-id="66880-144">Te zmiany są szczegółowo opisane na [liście zmian powodujących niezgodność](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="66880-144">These changes are detailed in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

## <a name="update-cmdlets-modules-and-parameters"></a><span data-ttu-id="66880-145">Aktualizacja poleceń cmdlet, modułów i parametrów</span><span class="sxs-lookup"><span data-stu-id="66880-145">Update cmdlets, modules, and parameters</span></span>

<span data-ttu-id="66880-146">Gdy skrypty zostaną zaktualizowane i będą działać przy użyciu aliasów, możesz stopniowo aktualizować je w celu używania nowych poleceń cmdlet i skorzystania z innych zmian, np. nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="66880-146">With scripts updated and running under aliases, you can take your time to update them to use the new cmdlets and take advantage of other changes like new features.</span></span> <span data-ttu-id="66880-147">W przypadku większości skryptów wystarczy zaktualizować nazwy poleceń cmdlet [zgodnie z nowym schematem nazewnictwa poleceń cmdlet w module Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes).</span><span class="sxs-lookup"><span data-stu-id="66880-147">For most scripts, you will only need to update cmdlet names, [following the new cmdlet naming scheme in Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes).</span></span> <span data-ttu-id="66880-148">Aby skrypty działały, być może trzeba będzie również wprowadzić inne zmiany w zależności od tego, jakie operacje przeprowadzają i z których funkcji programu Azure PowerShell korzystają.</span><span class="sxs-lookup"><span data-stu-id="66880-148">There may also be some other changes that you need to make in order to have your scripts work, depending on what they do and which Azure PowerShell features they take advantage of.</span></span>

<span data-ttu-id="66880-149">Na przykład [polecenia cmdlet usługi Blob Storage](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) zostały całkowicie przeprojektowane w celu używania nowego modelu asynchronicznego, więc aktualizacja skryptów, które z nich korzystają, będzie wymagać więcej pracy niż aktualizacja skryptów, w których wystarczy zmienić nazwy poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66880-149">For example, the [Blob Storage cmdlets](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) have been completely reworked to use a new asynchronous model, so scripts using them will take more work to update than those where the only relevant changes were cmdlet names.</span></span>

<span data-ttu-id="66880-150">Nawet jeśli do tej pory wystarczyło wprowadzić w skryptach niewielkie, proste zmiany (lub jeśli działają one bez zmian po włączeniu aliasów), przeczytaj [pełną listę zmian powodujących niezgodność w module Az 1.0.0](migrate-az-1.0.0.md), aby upewnić się, że nie polegasz na „przezroczystym” zachowaniu aliasów, które może zniknąć po zmianie nazw poleceń cmdlet i wyłączeniu aliasów.</span><span class="sxs-lookup"><span data-stu-id="66880-150">Even if you've only had to make small, simple changes to your scripts up to this point - or they even work without additional modification when aliases are enabled -  read the [full list of breaking changes in Az 1.0.0](migrate-az-1.0.0.md) to make sure that you're not relying on 'transparent' behavior of aliases which could disappear after you change cmdlet names and disable aliases.</span></span>

## <a name="disable-aliases"></a><span data-ttu-id="66880-151">Wyłączanie aliasów</span><span class="sxs-lookup"><span data-stu-id="66880-151">Disable aliases</span></span>

<span data-ttu-id="66880-152">Po ukończeniu migracji, gdy już nie polegasz na zachowaniu aliasów, zaleca się wyłączenie aliasów.</span><span class="sxs-lookup"><span data-stu-id="66880-152">Once you've completed your migration and are no longer relying on aliasing behavior, it's recommended that you disable aliases.</span></span> <span data-ttu-id="66880-153">Służy do tego polecenie [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="66880-153">This is done with the [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66880-154">Podczas uruchamiania tego polecenia cmdlet __upewnij się, że__ zostanie ono wywołane dla każdej wartości `-Scope`, dla której wywołano polecenie cmdlet `Enable-AzureRmAlias`. W przeciwnym razie w systemie mogą nadal istnieć skrypty polegające na zachowaniu aliasów.</span><span class="sxs-lookup"><span data-stu-id="66880-154">When running this cmdlet, __make sure__ that you invoke it for each `-Scope` that `Enable-AzureRmAlias` was invoked for, otherwise there may still be scripts on your system relying on the aliasing behavior.</span></span>