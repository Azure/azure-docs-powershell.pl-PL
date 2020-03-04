---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 66d755384e532d434811f3e6122dcba97d5c48b5
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477852"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="0dee3-103">Instalacja modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0dee3-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="0dee3-104">W tym artykule wyjaśniono, jak zainstalować moduły programu Azure PowerShell przy użyciu modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0dee3-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="0dee3-105">Te instrukcje działają na platformach Windows, macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="0dee3-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="0dee3-106">W przypadku modułu Az nie są obecnie obsługiwane żadne inne metody instalacji.</span><span class="sxs-lookup"><span data-stu-id="0dee3-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dee3-107">Wymagania</span><span class="sxs-lookup"><span data-stu-id="0dee3-107">Requirements</span></span>

<span data-ttu-id="0dee3-108">Program Azure PowerShell działa z programem PowerShell 5.1 lub nowszym w systemie Windows albo z programem PowerShell Core 6.x lub nowszym na dowolnej platformie.</span><span class="sxs-lookup"><span data-stu-id="0dee3-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="0dee3-109">Jeśli nie masz pewności, czy masz program PowerShell, albo korzystasz z systemu macOS lub Linux, [zainstaluj najnowszą wersję programu PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="0dee3-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="0dee3-110">Aby sprawdzić używaną wersję programu PowerShell, uruchom polecenie:</span><span class="sxs-lookup"><span data-stu-id="0dee3-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="0dee3-111">Aby uruchomić program Azure PowerShell w programie PowerShell 5.1 w systemie Windows:</span><span class="sxs-lookup"><span data-stu-id="0dee3-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="0dee3-112">Jeśli to konieczne, przeprowadź aktualizację do programu [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="0dee3-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="0dee3-113">Jeśli używasz systemu Windows 10, masz już zainstalowany program PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="0dee3-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="0dee3-114">Zainstaluj program [.NET Framework 4.7.2 lub nowszy](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="0dee3-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="0dee3-115">Nie istnieją żadne dodatkowe wymagania dotyczące programu Azure PowerShell, gdy korzysta się z programu PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="0dee3-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="0dee3-116">Instalacja modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0dee3-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="0dee3-117">__Nie możesz__ mieć równocześnie zainstalowanych modułów AzureRM i Az dla programu PowerShell 5.1 dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="0dee3-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="0dee3-118">Jeśli potrzebujesz zachować moduł AzureRM dostępny w systemie, zainstaluj moduł Az dla programu PowerShell Core w wersji 6.x lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="0dee3-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="0dee3-119">Aby to zrobić, [zainstaluj program PowerShell Core w wersji 6.x lub nowszej](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows), a następnie wykonaj następujące instrukcje w terminalu programu PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="0dee3-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="0dee3-120">Zaleca się przeprowadzić instalację tylko dla aktywnego użytkownika:</span><span class="sxs-lookup"><span data-stu-id="0dee3-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="0dee3-121">Jeśli chcesz przeprowadzić instalację dla wszystkich użytkowników w systemie, wymagane są uprawnienia administratora.</span><span class="sxs-lookup"><span data-stu-id="0dee3-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="0dee3-122">W sesji programu PowerShell z podwyższonym poziomem uprawnień uruchom jako administrator lub za pomocą polecenia `sudo` w systemie macOS lub Linux:</span><span class="sxs-lookup"><span data-stu-id="0dee3-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="0dee3-123">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0dee3-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="0dee3-124">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="0dee3-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="0dee3-125">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="0dee3-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="0dee3-126">Moduł Az to zbiorczy moduł poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0dee3-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="0dee3-127">Po jego zainstalowaniu są pobierane wszystkie dostępne moduły usługi Azure Resource Manager i są udostępniane do użycia ich polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dee3-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="0dee3-128">Instalowanie w trybie offline</span><span class="sxs-lookup"><span data-stu-id="0dee3-128">Install offline</span></span>

<span data-ttu-id="0dee3-129">W niektórych środowiskach nie jest możliwe nawiązanie połączenia z galerią programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0dee3-129">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="0dee3-130">W takich sytuacjach nadal możesz przeprowadzić instalację w trybie offline przy użyciu jednej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="0dee3-130">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="0dee3-131">Pobierz moduły do innej lokalizacji, a następnie użyj jej jako źródłowej lokalizacji instalacji w sieci.</span><span class="sxs-lookup"><span data-stu-id="0dee3-131">Download the modules to another location and use that as an installation source on your network.</span></span> <span data-ttu-id="0dee3-132">Może to być skomplikowany proces, ale umożliwi buforowanie modułów programu PowerShell na pojedynczym serwerze lub wdrażanie udziału plików za pomocą modułu PowerShellGet w dowolnym rozłączonym systemie.</span><span class="sxs-lookup"><span data-stu-id="0dee3-132">This can be a complicated process, but will let you cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="0dee3-133">Aby dowiedzieć się, jak skonfigurować lokalne repozytorium i przeprowadzić instalację w systemach rozłączonych, zobacz [Working with local PowerShellGet repositories (Praca z lokalnymi repozytoriami modułu PowerShellGet)](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="0dee3-133">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="0dee3-134">[Pobierz pakiet MSI programu Azure PowerShell](install-az-ps-msi.md) na maszynę połączoną z siecią, a następnie skopiuj instalator do systemów bez dostępu do galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0dee3-134">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="0dee3-135">Pamiętaj, że instalator MSI działa tylko na potrzeby programu PowerShell 5.1 w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="0dee3-135">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="0dee3-136">Zapisz moduł za pomocą polecenia [Save-Module](/powershell/module/PowershellGet/Save-Module) w udziale plików lub zapisz go w innej lokalizacji źródłowej, a następnie ręcznie skopiuj na inne maszyny:</span><span class="sxs-lookup"><span data-stu-id="0dee3-136">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="0dee3-137">Rozwiązywanie problemów</span><span class="sxs-lookup"><span data-stu-id="0dee3-137">Troubleshooting</span></span>

<span data-ttu-id="0dee3-138">Poniżej przedstawiono niektóre typowe problemy występujące podczas instalowania modułu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0dee3-138">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="0dee3-139">Jeśli masz problem, który nie został opisany w tym miejscu, [zgłoś go w usłudze GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="0dee3-139">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="0dee3-140">Serwer proxy blokuje połączenie</span><span class="sxs-lookup"><span data-stu-id="0dee3-140">Proxy blocks connection</span></span>

<span data-ttu-id="0dee3-141">Jeśli widzisz błędy z polecenia `Install-Module`, które wskazują, że galeria programu PowerShell jest nieosiągalna, możesz znajdować się za serwerem proxy.</span><span class="sxs-lookup"><span data-stu-id="0dee3-141">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="0dee3-142">Różne systemy operacyjne mają różne wymagania dotyczące konfigurowania serwera proxy dla całego systemu, które nie zostały tu szczegółowo omówione.</span><span class="sxs-lookup"><span data-stu-id="0dee3-142">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="0dee3-143">Skontaktuj się z administratorem systemu w celu uzyskania informacji o ustawieniach serwera proxy oraz sposobie konfigurowania ich dla Twojego systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0dee3-143">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="0dee3-144">Sam program PowerShell może nie być skonfigurowany do automatycznego korzystania z tego serwera proxy.</span><span class="sxs-lookup"><span data-stu-id="0dee3-144">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="0dee3-145">Za pomocą programu PowerShell 5.1 lub nowszego skonfiguruj serwer proxy do użytku dla sesji programu PowerShell, używając następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="0dee3-145">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="0dee3-146">Jeśli poświadczenia w Twoim systemie operacyjnym są skonfigurowane poprawnie, spowoduje to kierowanie żądań programu PowerShell przez serwer proxy.</span><span class="sxs-lookup"><span data-stu-id="0dee3-146">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="0dee3-147">Aby to ustawienie utrzymywało się między sesjami, dodaj to polecenie do [profilu programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="0dee3-147">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="0dee3-148">Aby zainstalować pakiet, Twój serwer proxy musi zezwalać na połączenia HTTPS z następującym adresem:</span><span class="sxs-lookup"><span data-stu-id="0dee3-148">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="0dee3-149">Logowanie</span><span class="sxs-lookup"><span data-stu-id="0dee3-149">Sign in</span></span>

<span data-ttu-id="0dee3-150">Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0dee3-150">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="0dee3-151">Jeśli wyłączono automatyczne ładowanie modułów, ręcznie zaimportuj moduł za pomocą polecenia `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="0dee3-151">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="0dee3-152">Ze względu na strukturę modułu może to potrwać kilka sekund.</span><span class="sxs-lookup"><span data-stu-id="0dee3-152">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="0dee3-153">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="0dee3-153">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="0dee3-154">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="0dee3-154">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="0dee3-155">Aktualizowanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0dee3-155">Update the Azure PowerShell module</span></span>

<span data-ttu-id="0dee3-156">Jeśli pierwotnie korzystano z polecenia Install-Module, należy użyć polecenia [Update-Module](/powershell/module/powershellget/update-module), aby uzyskać najnowszą wersję.</span><span class="sxs-lookup"><span data-stu-id="0dee3-156">If you originally used Install-Module, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="0dee3-157">Jeśli pierwotnie korzystano z pakietu MSI, należy pobrać i zainstalować nowy pakiet MSI w celu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="0dee3-157">If you originally used the MSI package then you should download and install the new MSI in order to udpate.</span></span> <span data-ttu-id="0dee3-158">Jeśli masz problemy z aktualizowaniem lub używaniem pakietu z modułu PowershellGet, należy wykonać __ponowną instalację__ a nie __aktualizację__.</span><span class="sxs-lookup"><span data-stu-id="0dee3-158">If you have any issues with updating using the package from PowershellGet then you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="0dee3-159">Jest ona realizowana w taki sam sposób jak instalacja, ale może być konieczne dodanie argumentu `-Force`:</span><span class="sxs-lookup"><span data-stu-id="0dee3-159">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="0dee3-160">Mimo że może to spowodować zastąpienie zainstalowanych modułów, nadal można mieć starsze wersje pozostawione w systemie.</span><span class="sxs-lookup"><span data-stu-id="0dee3-160">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="0dee3-161">Aby dowiedzieć się, jak usunąć stare wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="0dee3-161">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="0dee3-162">Korzystanie z wielu wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0dee3-162">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="0dee3-163">Jest możliwe zainstalowanie więcej niż jednej wersji programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0dee3-163">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="0dee3-164">Aby sprawdzić, czy masz wiele zainstalowanych wersji programu Azure PowerShell, użyj następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="0dee3-164">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="0dee3-165">Aby usunąć wersję programu Azure PowerShell, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="0dee3-165">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="0dee3-166">Określoną wersję modułu `Az` możesz zainstalować lub załadować, używając argumentu `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="0dee3-166">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="0dee3-167">Jeśli masz zainstalowaną więcej niż jedną wersję modułu, funkcja automatycznego ładowania modułów i polecenie `Import-Module` domyślnie ładują najnowszą wersję.</span><span class="sxs-lookup"><span data-stu-id="0dee3-167">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="0dee3-168">Przekazywanie opinii</span><span class="sxs-lookup"><span data-stu-id="0dee3-168">Provide feedback</span></span>

<span data-ttu-id="0dee3-169">Jeśli znajdziesz usterkę w programie Azure PowerShell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="0dee3-169">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="0dee3-170">Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="0dee3-170">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0dee3-171">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="0dee3-171">Next Steps</span></span>

<span data-ttu-id="0dee3-172">Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0dee3-172">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="0dee3-173">Jeśli znasz program Azure PowerShell i chcesz przeprowadzić migrację z modułu AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="0dee3-173">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>