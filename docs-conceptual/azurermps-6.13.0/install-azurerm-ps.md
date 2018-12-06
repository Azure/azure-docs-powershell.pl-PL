---
title: Instalowanie programu Azure PowerShell w systemie Windows za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 616a9e14c3944e3151676d89b8a22e35d8f9d406
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828428"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="77573-103">Instalowanie programu Azure PowerShell w systemie Windows za pomocą modułu PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="77573-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="77573-104">W tym artykule opisano kroki instalowania modułów programu Azure PowerShell w środowisku systemu Windows przy użyciu modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="77573-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="77573-105">Moduł PowerShellGet i funkcja zarządzania modułami to preferowany sposób instalacji programu Azure PowerShell, ale jeśli wolisz go zainstalować za pomocą Instalatora platformy internetowej lub pakietu MSI, zobacz [Inne metody instalacji](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="77573-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="77573-106">Aby uzyskać instrukcje dotyczące instalacji programu Azure PowerShell na innych platformach, zobacz [Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="77573-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="77573-107">Klasyczny model wdrażania platformy Azure nie jest obsługiwany przez tę wersję programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77573-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="77573-108">Aby uzyskać pomoc techniczną w przypadku wdrożeń klasycznych, postępuj zgodnie z instrukcjami na stronie [Instalowanie modułu zarządzania usługami programu Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="77573-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="requirements"></a><span data-ttu-id="77573-109">Wymagania</span><span class="sxs-lookup"><span data-stu-id="77573-109">Requirements</span></span>

<span data-ttu-id="77573-110">Począwszy od programu Azure PowerShell w wersji 6.0, jest wymagany program PowerShell w wersji 5.0.</span><span class="sxs-lookup"><span data-stu-id="77573-110">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="77573-111">Aby sprawdzić wersję programu PowerShell na maszynie, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="77573-111">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="77573-112">Jeśli masz nieaktualną wersję, zobacz [Upgrading existing Windows PowerShell (Uaktualnianie istniejącego programu Windows PowerShell)](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="77573-112">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77573-113">Moduł opisany w tym dokumencie (AzureRM) korzysta z programu .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="77573-113">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="77573-114">Dlatego jest on niezgodny z programem PowerShell 6.0, który korzysta z platformy .NET Core.</span><span class="sxs-lookup"><span data-stu-id="77573-114">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="77573-115">Jeśli korzystasz z programu PowerShell 6.0, postępuj zgodnie z [instrukcjami dotyczącymi instalacji dla systemów macOS i Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="77573-115">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="77573-116">Instalacja modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="77573-116">Install the Azure PowerShell module</span></span>

<span data-ttu-id="77573-117">Do zainstalowania modułów z galerii programu PowerShell jest wymagany podwyższony poziom uprawnień.</span><span class="sxs-lookup"><span data-stu-id="77573-117">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="77573-118">Aby zainstalować program Azure PowerShell, uruchom następujące polecenie w sesji z podwyższonym poziomem uprawnień:</span><span class="sxs-lookup"><span data-stu-id="77573-118">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="77573-119">Jeśli masz wersję pakietu NuGet starszą niż 2.8.5.201, zostanie wyświetlony monit o pobranie i zainstalowanie najnowszej wersji pakietu NuGet.</span><span class="sxs-lookup"><span data-stu-id="77573-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="77573-120">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="77573-120">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="77573-121">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="77573-121">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="77573-122">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="77573-122">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="77573-123">Moduł `AzureRM` to zbiorczy moduł poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77573-123">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="77573-124">Po jego zainstalowaniu są pobierane wszystkie dostępne moduły usługi Azure Resource Manager i są udostępniane do użycia ich polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77573-124">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="77573-125">Logowanie</span><span class="sxs-lookup"><span data-stu-id="77573-125">Sign in</span></span>

<span data-ttu-id="77573-126">Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77573-126">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="77573-127">Jeśli wyłączono automatyczne ładowanie modułów, musisz ręcznie zaimportować moduł za pomocą polecenia `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="77573-127">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="77573-128">Ze względu na strukturę modułu może to potrwać kilka sekund.</span><span class="sxs-lookup"><span data-stu-id="77573-128">Because of the way the module is structured, this can take a few seconds.</span></span>


<span data-ttu-id="77573-129">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="77573-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="77573-130">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="77573-130">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="77573-131">Aktualizowanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="77573-131">Update the Azure PowerShell module</span></span>

<span data-ttu-id="77573-132">Możesz zaktualizować instalację programu Azure PowerShell przez uruchomienie polecenia [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="77573-132">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="77573-133">To polecenie __nie__ powoduje odinstalowania wcześniejszych wersji.</span><span class="sxs-lookup"><span data-stu-id="77573-133">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="77573-134">Jeśli chcesz usunąć starsze wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="77573-134">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="77573-135">Korzystanie z wielu wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="77573-135">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="77573-136">Jest możliwe zainstalowanie więcej niż jednej wersji programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77573-136">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="77573-137">Aby sprawdzić, czy masz wiele zainstalowanych wersji programu Azure PowerShell, użyj następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="77573-137">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name AzureRM -List | select Name,Version
```

<span data-ttu-id="77573-138">Aby usunąć wersję programu Azure PowerShell, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="77573-138">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="77573-139">Obecność więcej niż jednej wersji może być potrzebna w przypadku pracy z lokalnymi zasobami usługi Azure Stack, korzystania ze starszej wersji systemu Windows lub używania klasycznego modelu wdrażania platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="77573-139">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="77573-140">Aby zainstalować starszą wersję, podaj argument `-RequiredVersion` podczas instalacji.</span><span class="sxs-lookup"><span data-stu-id="77573-140">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="77573-141">Podczas ładowania modułu Azure PowerShell jest domyślnie ładowana najnowsza wersja.</span><span class="sxs-lookup"><span data-stu-id="77573-141">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="77573-142">Aby załadować inną wersję, podaj argument `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="77573-142">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="77573-143">Przekazywanie opinii</span><span class="sxs-lookup"><span data-stu-id="77573-143">Provide feedback</span></span>

<span data-ttu-id="77573-144">Jeśli znajdziesz błąd podczas korzystania z programu Azure Powershell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="77573-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="77573-145">Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="77573-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="77573-146">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="77573-146">Next Steps</span></span>

<span data-ttu-id="77573-147">Aby zacząć korzystać z programu Azure PowerShell i dowiedzieć się więcej o module i jego funkcjach, zobacz [Rozpoczęcie korzystania z programu Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="77573-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
