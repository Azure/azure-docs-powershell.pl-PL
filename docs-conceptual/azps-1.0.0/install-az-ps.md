---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 828fa8cb2aabac893c566fb146d00af04b16b479
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982930"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="ecf77-103">Instalacja modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ecf77-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="ecf77-104">W tym artykule wyjaśniono, jak zainstalować moduły programu Azure PowerShell przy użyciu modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="ecf77-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="ecf77-105">Te instrukcje działają na platformach Windows, macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="ecf77-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="ecf77-106">W przypadku modułu Az nie są obecnie obsługiwane żadne inne metody instalacji.</span><span class="sxs-lookup"><span data-stu-id="ecf77-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf77-107">Wymagania</span><span class="sxs-lookup"><span data-stu-id="ecf77-107">Requirements</span></span>

<span data-ttu-id="ecf77-108">Program Azure PowerShell działa z programem PowerShell 5.x w systemie Windows 7 lub nowszym albo z programem PowerShell 6.x na dowolnej platformie.</span><span class="sxs-lookup"><span data-stu-id="ecf77-108">Azure PowerShell works with PowerShell 5.x on Windows 7 or higher, or PowerShell 6.x on any platform.</span></span>
<span data-ttu-id="ecf77-109">Aby sprawdzić używaną wersję programu PowerShell, uruchom polecenie:</span><span class="sxs-lookup"><span data-stu-id="ecf77-109">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="ecf77-110">Jeśli masz nieaktualną wersją lub musisz zainstalować program PowerShell, zobacz [Instalowanie różnych wersji programu PowerShell](/powershell/scripting/setup/installing-powershell).</span><span class="sxs-lookup"><span data-stu-id="ecf77-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](/powershell/scripting/setup/installing-powershell).</span></span> <span data-ttu-id="ecf77-111">Ta strona zawiera linki do informacji o instalacji dla określonych platform.</span><span class="sxs-lookup"><span data-stu-id="ecf77-111">Install information for your platform is linked from that page.</span></span>

<span data-ttu-id="ecf77-112">Jeśli używasz programu PowerShell 5.x w systemie Windows, musisz mieć również zainstalowany program .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="ecf77-112">If you are using PowerShell 5.x on Windows, you also need .NET Framework 4.7.2 installed.</span></span> <span data-ttu-id="ecf77-113">Aby uzyskać instrukcje dotyczące aktualizacji lub instalowania nowej wersji programu .NET Framework, zobacz [Przewodnik instalacji programu .NET Framework](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="ecf77-113">For instructions on updating or installing a new version of .NET Framework, see the [.NET Framework installation guide](/dotnet/framework/install).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="ecf77-114">Instalacja modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ecf77-114">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="ecf77-115">Moduły AzureRM i Az mogą być zainstalowane jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="ecf77-115">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="ecf77-116">Jeśli oba są zainstalowane, __nie włączaj aliasów__.</span><span class="sxs-lookup"><span data-stu-id="ecf77-116">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="ecf77-117">Włączenie aliasów spowoduje powstanie konfliktów między poleceniami cmdlet modułu AzureRM i aliasami poleceń modułu Az, co może doprowadzić do nieoczekiwanego zachowania.</span><span class="sxs-lookup"><span data-stu-id="ecf77-117">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="ecf77-118">Zalecamy, aby przed zainstalowaniem modułu Az odinstalować moduł AzureRM.</span><span class="sxs-lookup"><span data-stu-id="ecf77-118">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="ecf77-119">Odinstalować moduł AzureRM lub włączyć aliasy możesz w dowolnym momencie.</span><span class="sxs-lookup"><span data-stu-id="ecf77-119">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="ecf77-120">Aby dowiedzieć się więcej o aliasach poleceń AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="ecf77-120">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="ecf77-121">Aby uzyskać instrukcje odinstalowywania, zobacz [Odinstalowywanie modułu AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="ecf77-121">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="ecf77-122">Aby zainstalować moduły w zakresie globalnym, wymagany jest podwyższony poziom uprawnień w celu zainstalowania modułów z galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ecf77-122">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="ecf77-123">Aby zainstalować program Azure PowerShell, uruchom następujące polecenie w sesji z podwyższonym poziomem uprawnień (opcja „Uruchom jako Administrator” w systemie Windows lub z uprawnieniami superużytkownika w systemie macOS lub Linux):</span><span class="sxs-lookup"><span data-stu-id="ecf77-123">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="ecf77-124">Jeśli nie masz dostępu do uprawnień administratora, możesz przeprowadzić instalację dla bieżącego użytkownika, dodając argument `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="ecf77-124">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="ecf77-125">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="ecf77-125">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="ecf77-126">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="ecf77-126">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="ecf77-127">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="ecf77-127">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="ecf77-128">Moduł Az to zbiorczy moduł poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ecf77-128">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ecf77-129">Po jego zainstalowaniu są pobierane wszystkie dostępne moduły usługi Azure Resource Manager i są udostępniane do użycia ich polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecf77-129">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="ecf77-130">Logowanie</span><span class="sxs-lookup"><span data-stu-id="ecf77-130">Sign in</span></span>

<span data-ttu-id="ecf77-131">Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf77-131">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="ecf77-132">Jeśli wyłączono automatyczne ładowanie modułów, musisz ręcznie zaimportować moduł za pomocą polecenia `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="ecf77-132">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="ecf77-133">Ze względu na strukturę modułu może to potrwać kilka sekund.</span><span class="sxs-lookup"><span data-stu-id="ecf77-133">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="ecf77-134">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="ecf77-134">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="ecf77-135">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ecf77-135">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="ecf77-136">Aktualizowanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ecf77-136">Update the Azure PowerShell module</span></span>

<span data-ttu-id="ecf77-137">Możesz zaktualizować instalację programu Azure PowerShell przez uruchomienie polecenia [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="ecf77-137">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="ecf77-138">To polecenie __nie__ powoduje odinstalowania starszych wersji.</span><span class="sxs-lookup"><span data-stu-id="ecf77-138">This command does __not__ uninstall older versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="ecf77-139">Aby dowiedzieć się, jak usunąć stare wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ecf77-139">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="ecf77-140">Korzystanie z wielu wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ecf77-140">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="ecf77-141">Jest możliwe zainstalowanie więcej niż jednej wersji programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ecf77-141">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="ecf77-142">Aby sprawdzić, czy masz wiele zainstalowanych wersji programu Azure PowerShell, użyj następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="ecf77-142">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="ecf77-143">Aby usunąć wersję programu Azure PowerShell, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ecf77-143">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="ecf77-144">Określoną wersję modułu `Az` możesz zainstalować lub załadować, używając argumentu `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="ecf77-144">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="ecf77-145">Jeśli masz zainstalowaną więcej niż jedną wersję modułu, funkcja automatycznego ładowania modułów i polecenie `Import-Module` domyślnie ładują najnowszą wersję.</span><span class="sxs-lookup"><span data-stu-id="ecf77-145">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="ecf77-146">Przekazywanie opinii</span><span class="sxs-lookup"><span data-stu-id="ecf77-146">Provide feedback</span></span>

<span data-ttu-id="ecf77-147">Jeśli znajdziesz usterkę w programie Azure PowerShell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="ecf77-147">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="ecf77-148">Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="ecf77-148">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ecf77-149">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="ecf77-149">Next Steps</span></span>

<span data-ttu-id="ecf77-150">Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ecf77-150">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="ecf77-151">Jeśli znasz program Azure PowerShell i chcesz przeprowadzić migrację z modułu AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="ecf77-151">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
