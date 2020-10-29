---
title: Instalowanie programu Azure PowerShell w systemie Windows za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c03c6ee3782b68de8a237b3c215405ff6513dbca
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523244"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="5a302-103">Instalowanie programu Azure PowerShell w systemie Windows za pomocą modułu PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="5a302-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="5a302-104">W tym artykule opisano kroki instalowania modułów programu Azure PowerShell w programie PowerShell 5.x w systemie Windows przy użyciu modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="5a302-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="5a302-105">Moduł PowerShellGet i funkcja zarządzania modułami to preferowany sposób instalacji programu Azure PowerShell, ale jeśli wolisz go zainstalować za pomocą Instalatora platformy internetowej lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="5a302-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="5a302-106">Klasyczny model wdrażania platformy Azure nie jest obsługiwany przez tę wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a302-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="5a302-107">Aby uzyskać pomoc techniczną w przypadku wdrożeń klasycznych, postępuj zgodnie z instrukcjami na stronie [Instalowanie modułu zarządzania usługami programu Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="5a302-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a302-108">Moduł AzureRM nie jest obsługiwany w systemach macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="5a302-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="5a302-109">Aby używać poleceń cmdlet programu Azure PowerShell na tych platformach, należy [zainstalować moduł Az](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="5a302-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a302-110">Wymagania</span><span class="sxs-lookup"><span data-stu-id="5a302-110">Requirements</span></span>

<span data-ttu-id="5a302-111">Do zainstalowania programu Azure PowerShell jest wymagany moduł PowerShellGet w wersji 1.1.2.0 lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="5a302-111">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="5a302-112">Aby sprawdzić, czy jest on dostępny w systemie, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="5a302-112">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="5a302-113">Powinny zostać wyświetlone dane wyjściowe podobne do poniższych:</span><span class="sxs-lookup"><span data-stu-id="5a302-113">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="5a302-114">Aby zaktualizować instalację modułu PowerShellGet, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="5a302-114">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="5a302-115">Jeśli nie masz zainstalowanego modułu PowerShellGet, postępuj zgodnie z instrukcjami w poniższej tabeli dotyczącymi Twojego systemu.</span><span class="sxs-lookup"><span data-stu-id="5a302-115">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="5a302-116">Scenariusz</span><span class="sxs-lookup"><span data-stu-id="5a302-116">Scenario</span></span>|<span data-ttu-id="5a302-117">Instrukcje dotyczące instalacji</span><span class="sxs-lookup"><span data-stu-id="5a302-117">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="5a302-118">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5a302-118">Windows 10</span></span><br/><span data-ttu-id="5a302-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5a302-119">Windows Server 2016</span></span>|<span data-ttu-id="5a302-120">Wbudowane w platformę Windows Management Framework (WMF) 5.0 zawartą w systemie operacyjnym</span><span class="sxs-lookup"><span data-stu-id="5a302-120">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="5a302-121">Uaktualnienie do programu PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="5a302-121">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="5a302-122">Zainstaluj najnowszą wersję platformy WMF</span><span class="sxs-lookup"><span data-stu-id="5a302-122">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)</li><li><span data-ttu-id="5a302-123">Uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="5a302-123">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="5a302-124">Korzystanie z modułu PowerShellGet wymaga zasad wykonania pozwalających uruchamiać skrypty.</span><span class="sxs-lookup"><span data-stu-id="5a302-124">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="5a302-125">Aby uzyskać więcej informacji na temat zasad wykonania programu PowerShell, zobacz [Informacje o zasadach wykonania](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="5a302-125">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="5a302-126">Moduł opisany w tym dokumencie (AzureRM) korzysta z programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="5a302-126">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="5a302-127">Dlatego jest on niezgodny z programem PowerShell 6.0, który korzysta z platformy .NET Core.</span><span class="sxs-lookup"><span data-stu-id="5a302-127">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="5a302-128">Jeśli korzystasz z programu PowerShell 6.0, postępuj zgodnie z [instrukcjami dotyczącymi instalacji dla systemów macOS i Linux](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="5a302-128">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="5a302-129">Instalacja modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a302-129">Install the Azure PowerShell module</span></span>

<span data-ttu-id="5a302-130">Do zainstalowania modułów z galerii programu PowerShell jest wymagany podwyższony poziom uprawnień.</span><span class="sxs-lookup"><span data-stu-id="5a302-130">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="5a302-131">Aby zainstalować program Azure PowerShell, uruchom następujące polecenie w sesji z podwyższonym poziomem uprawnień:</span><span class="sxs-lookup"><span data-stu-id="5a302-131">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="5a302-132">Jeśli masz wersję pakietu NuGet starszą niż 2.8.5.201, zostanie wyświetlony monit o pobranie i zainstalowanie najnowszej wersji pakietu NuGet.</span><span class="sxs-lookup"><span data-stu-id="5a302-132">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="5a302-133">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="5a302-133">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="5a302-134">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="5a302-134">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="5a302-135">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="5a302-135">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="5a302-136">Moduł `AzureRM` to zbiorczy moduł poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a302-136">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="5a302-137">Po jego zainstalowaniu są pobierane wszystkie dostępne moduły usługi Azure Resource Manager i są udostępniane do użycia ich polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a302-137">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="5a302-138">Logowanie</span><span class="sxs-lookup"><span data-stu-id="5a302-138">Sign in</span></span>

<span data-ttu-id="5a302-139">Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `AzureRM` w bieżącej sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5a302-139">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="5a302-140">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="5a302-140">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="5a302-141">Automatyczne zaimportowanie modułu `AzureRM` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="5a302-141">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="5a302-142">Aby dowiedzieć się, jak można utrwalić swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="5a302-142">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="5a302-143">Aktualizowanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a302-143">Update the Azure PowerShell module</span></span>

<span data-ttu-id="5a302-144">Możesz zaktualizować instalację programu Azure PowerShell przez uruchomienie polecenia [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="5a302-144">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="5a302-145">To polecenie __nie__ powoduje odinstalowania wcześniejszych wersji.</span><span class="sxs-lookup"><span data-stu-id="5a302-145">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="5a302-146">Jeśli chcesz usunąć starsze wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5a302-146">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="5a302-147">Korzystanie z wielu wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a302-147">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="5a302-148">Jest możliwe zainstalowanie wielu wersji programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a302-148">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="5a302-149">Obecność więcej niż jednej wersji może być potrzebna w przypadku pracy z lokalnymi zasobami usługi Azure Stack, korzystania ze starszej wersji systemu Windows, której nie można zaktualizować do programu PowerShell 5.0, lub używania klasycznego modelu wdrażania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5a302-149">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="5a302-150">Aby zainstalować starszą wersję, podaj argument `-RequiredVersion` podczas instalacji.</span><span class="sxs-lookup"><span data-stu-id="5a302-150">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="5a302-151">Podczas ładowania modułu Azure PowerShell jest domyślnie ładowana najnowsza wersja.</span><span class="sxs-lookup"><span data-stu-id="5a302-151">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="5a302-152">Aby załadować inną wersję, podaj argument `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="5a302-152">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="5a302-153">Przekazywanie opinii</span><span class="sxs-lookup"><span data-stu-id="5a302-153">Provide feedback</span></span>

<span data-ttu-id="5a302-154">Jeśli znajdziesz błąd podczas korzystania z programu Azure Powershell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="5a302-154">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="5a302-155">Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="5a302-155">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5a302-156">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="5a302-156">Next Steps</span></span>

<span data-ttu-id="5a302-157">Aby zacząć korzystać z programu Azure PowerShell i dowiedzieć się więcej o module i jego funkcjach, zobacz [Rozpoczęcie korzystania z programu Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5a302-157">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
