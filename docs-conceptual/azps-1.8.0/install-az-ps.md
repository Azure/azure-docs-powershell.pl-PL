---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365745"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="a6031-103">Instalacja modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6031-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="a6031-104">W tym artykule wyjaśniono, jak zainstalować moduły programu Azure PowerShell przy użyciu modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="a6031-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="a6031-105">Te instrukcje działają na platformach Windows, macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="a6031-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="a6031-106">W przypadku modułu Az nie są obecnie obsługiwane żadne inne metody instalacji.</span><span class="sxs-lookup"><span data-stu-id="a6031-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6031-107">Wymagania</span><span class="sxs-lookup"><span data-stu-id="a6031-107">Requirements</span></span>

<span data-ttu-id="a6031-108">Program Azure PowerShell działa z programem PowerShell 5.1 lub nowszym w systemie Windows albo z programem PowerShell Core 6.x lub nowszym na dowolnej platformie.</span><span class="sxs-lookup"><span data-stu-id="a6031-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="a6031-109">Jeśli nie masz pewności, czy masz program PowerShell, albo korzystasz z systemu macOS lub Linux, [zainstaluj najnowszą wersję programu PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="a6031-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="a6031-110">Aby sprawdzić używaną wersję programu PowerShell, uruchom polecenie:</span><span class="sxs-lookup"><span data-stu-id="a6031-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="a6031-111">Aby uruchomić program Azure PowerShell w programie PowerShell 5.1 w systemie Windows:</span><span class="sxs-lookup"><span data-stu-id="a6031-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="a6031-112">Jeśli to konieczne, przeprowadź aktualizację do programu [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="a6031-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="a6031-113">Jeśli używasz systemu Windows 10, masz już zainstalowany program PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="a6031-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="a6031-114">Zainstaluj program [.NET Framework 4.7.2 lub nowszy](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="a6031-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="a6031-115">Nie istnieją żadne dodatkowe wymagania dotyczące programu Azure PowerShell, gdy korzysta się z programu PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="a6031-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="a6031-116">Instalacja modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6031-116">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="a6031-117">Moduły AzureRM i Az mogą być zainstalowane jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="a6031-117">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="a6031-118">Jeśli oba są zainstalowane, __nie włączaj aliasów__.</span><span class="sxs-lookup"><span data-stu-id="a6031-118">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="a6031-119">Włączenie aliasów spowoduje powstanie konfliktów między poleceniami cmdlet modułu AzureRM i aliasami poleceń modułu Az, co może doprowadzić do nieoczekiwanego zachowania.</span><span class="sxs-lookup"><span data-stu-id="a6031-119">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="a6031-120">Zalecamy, aby przed zainstalowaniem modułu Az odinstalować moduł AzureRM.</span><span class="sxs-lookup"><span data-stu-id="a6031-120">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="a6031-121">Odinstalować moduł AzureRM lub włączyć aliasy możesz w dowolnym momencie.</span><span class="sxs-lookup"><span data-stu-id="a6031-121">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="a6031-122">Aby dowiedzieć się więcej o aliasach poleceń AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="a6031-122">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="a6031-123">Aby uzyskać instrukcje odinstalowywania, zobacz [Odinstalowywanie modułu AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="a6031-123">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="a6031-124">Aby zainstalować moduły w zakresie globalnym, wymagany jest podwyższony poziom uprawnień w celu zainstalowania modułów z galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6031-124">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="a6031-125">Aby zainstalować program Azure PowerShell, uruchom następujące polecenie w sesji z podwyższonym poziomem uprawnień (opcja „Uruchom jako Administrator” w systemie Windows lub z uprawnieniami superużytkownika w systemie macOS lub Linux):</span><span class="sxs-lookup"><span data-stu-id="a6031-125">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="a6031-126">Jeśli nie masz dostępu do uprawnień administratora, możesz przeprowadzić instalację dla bieżącego użytkownika, dodając argument `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="a6031-126">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="a6031-127">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="a6031-127">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="a6031-128">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="a6031-128">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="a6031-129">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="a6031-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="a6031-130">Moduł Az to zbiorczy moduł poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6031-130">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a6031-131">Po jego zainstalowaniu są pobierane wszystkie dostępne moduły usługi Azure Resource Manager i są udostępniane do użycia ich polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6031-131">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="a6031-132">Logowanie</span><span class="sxs-lookup"><span data-stu-id="a6031-132">Sign in</span></span>

<span data-ttu-id="a6031-133">Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6031-133">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="a6031-134">Jeśli wyłączono automatyczne ładowanie modułów, musisz ręcznie zaimportować moduł za pomocą polecenia `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="a6031-134">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="a6031-135">Ze względu na strukturę modułu może to potrwać kilka sekund.</span><span class="sxs-lookup"><span data-stu-id="a6031-135">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="a6031-136">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="a6031-136">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="a6031-137">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="a6031-137">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="a6031-138">Aktualizowanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6031-138">Update the Azure PowerShell module</span></span>

<span data-ttu-id="a6031-139">Ze względu na sposób spakowania modułu Az polecenie [Update-Module](/powershell/module/powershellget/update-module) nie zaktualizuje poprawnie Twojej instalacji.</span><span class="sxs-lookup"><span data-stu-id="a6031-139">Because of how the Az module is package, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="a6031-140">Od strony technicznej moduł Az jest metamodułem, obejmującym wszystkie podmoduły zawierające polecenia cmdlet do interakcji z usługami platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6031-140">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="a6031-141">Oznacza to, że w celu zaktualizowania modułu Azure PowerShell konieczna będzie __ponowna instalacja__, a nie sama __aktualizacja__.</span><span class="sxs-lookup"><span data-stu-id="a6031-141">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="a6031-142">Jest ona realizowana w taki sam sposób jak instalacja, ale może być konieczne dodanie argumentu `-Force`:</span><span class="sxs-lookup"><span data-stu-id="a6031-142">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="a6031-143">Mimo że może to spowodować zastąpienie zainstalowanych modułów, nadal można mieć starsze wersje pozostawione w systemie.</span><span class="sxs-lookup"><span data-stu-id="a6031-143">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="a6031-144">Aby dowiedzieć się, jak usunąć stare wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="a6031-144">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="a6031-145">Korzystanie z wielu wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a6031-145">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="a6031-146">Jest możliwe zainstalowanie więcej niż jednej wersji programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a6031-146">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="a6031-147">Aby sprawdzić, czy masz wiele zainstalowanych wersji programu Azure PowerShell, użyj następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="a6031-147">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="a6031-148">Aby usunąć wersję programu Azure PowerShell, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="a6031-148">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="a6031-149">Określoną wersję modułu `Az` możesz zainstalować lub załadować, używając argumentu `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="a6031-149">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="a6031-150">Jeśli masz zainstalowaną więcej niż jedną wersję modułu, funkcja automatycznego ładowania modułów i polecenie `Import-Module` domyślnie ładują najnowszą wersję.</span><span class="sxs-lookup"><span data-stu-id="a6031-150">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="a6031-151">Przekazywanie opinii</span><span class="sxs-lookup"><span data-stu-id="a6031-151">Provide feedback</span></span>

<span data-ttu-id="a6031-152">Jeśli znajdziesz usterkę w programie Azure PowerShell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="a6031-152">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="a6031-153">Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="a6031-153">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a6031-154">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="a6031-154">Next Steps</span></span>

<span data-ttu-id="a6031-155">Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="a6031-155">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="a6031-156">Jeśli znasz program Azure PowerShell i chcesz przeprowadzić migrację z modułu AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="a6031-156">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
