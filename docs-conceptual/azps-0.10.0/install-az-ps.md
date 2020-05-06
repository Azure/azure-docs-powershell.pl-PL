---
title: Instalowanie programu Azure PowerShell za pomocą modułu PowerShellGet
description: Jak zainstalować program Azure PowerShell za pomocą modułu PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.openlocfilehash: 7a25270566f5e856ee44c4c191a47a3e7334508b
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2020
ms.locfileid: "81445700"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="15b13-103">Instalowanie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="15b13-103">Install Azure PowerShell</span></span>

<span data-ttu-id="15b13-104">W tym artykule wyjaśniono, jak zainstalować moduły programu Azure PowerShell przy użyciu modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="15b13-104">This article explains how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="15b13-105">Te instrukcje działają na platformach Windows, macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="15b13-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="15b13-106">Program Azure PowerShell jest również dostępny w usłudze Azure [Cloud Shell](/azure/cloud-shell/overview) i jest teraz wstępnie instalowany w [obrazach platformy Docker](azureps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="15b13-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15b13-107">Wymagania</span><span class="sxs-lookup"><span data-stu-id="15b13-107">Requirements</span></span>

<span data-ttu-id="15b13-108">Program Azure PowerShell działa z programem PowerShell 5.1 lub nowszym w systemie Windows albo z programem PowerShell Core 6.x lub nowszym na dowolnej platformie.</span><span class="sxs-lookup"><span data-stu-id="15b13-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="15b13-109">Należy zainstalować [najnowszą wersję programu PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core) dostępną dla danego systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="15b13-109">You should install the [latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core) available for your operating system.</span></span> <span data-ttu-id="15b13-110">Program Azure PowerShell nie ma dodatkowych wymagań w przypadku uruchamiania w programie PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="15b13-110">Azure PowerShell has no additional requirements when run on PowerShell Core.</span></span>

<span data-ttu-id="15b13-111">Aby sprawdzić używaną wersję programu PowerShell, uruchom polecenie:</span><span class="sxs-lookup"><span data-stu-id="15b13-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="15b13-112">Aby użyć programu Azure PowerShell w programie PowerShell 5.1 w systemie Windows:</span><span class="sxs-lookup"><span data-stu-id="15b13-112">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="15b13-113">Jeśli to konieczne, przeprowadź aktualizację do programu [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="15b13-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="15b13-114">Jeśli używasz systemu Windows 10, masz już zainstalowany program PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="15b13-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="15b13-115">Zainstaluj program [.NET Framework 4.7.2 lub nowszy](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="15b13-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="15b13-116">Upewnij się, że masz najnowszą wersję modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="15b13-116">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="15b13-117">Uruchom polecenie `Update-Module PowerShellGet -Force`.</span><span class="sxs-lookup"><span data-stu-id="15b13-117">Run `Update-Module PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="15b13-118">Instalacja modułu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="15b13-118">Install the Azure PowerShell module</span></span>

<span data-ttu-id="15b13-119">Użycie poleceń cmdlet PowerShellGet jest preferowaną metodą instalacji.</span><span class="sxs-lookup"><span data-stu-id="15b13-119">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="15b13-120">Ta metoda działa tak samo na platformach Windows, macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="15b13-120">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="15b13-121">Uruchom następujące polecenie z sesji programu PowerShell:</span><span class="sxs-lookup"><span data-stu-id="15b13-121">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="15b13-122">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="15b13-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="15b13-123">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="15b13-123">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="15b13-124">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="15b13-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="15b13-125">Moduł Az to zbiorczy moduł poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="15b13-125">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="15b13-126">Po jego zainstalowaniu są pobierane wszystkie dostępne moduły usługi Azure Resource Manager i są udostępniane do użycia ich polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15b13-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

> [!WARNING]
> <span data-ttu-id="15b13-127">Nie obsługujemy równocześnie zainstalowanych modułów AzureRM i Az w programie PowerShell 5.1 dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="15b13-127">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="15b13-128">Jeśli potrzebujesz zachować moduł AzureRM dostępny w systemie, zainstaluj moduł Az dla programu PowerShell Core w wersji 6.x lub nowszej.</span><span class="sxs-lookup"><span data-stu-id="15b13-128">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span>

<span data-ttu-id="15b13-129">Najpierw [zainstaluj program PowerShell Core 6.x lub nowszy](/powershell/scripting/install/installing-powershell-core-on-windows)</span><span class="sxs-lookup"><span data-stu-id="15b13-129">First, [install PowerShell Core 6.x or later](/powershell/scripting/install/installing-powershell-core-on-windows)</span></span>

<span data-ttu-id="15b13-130">Następnie w sesji programu PowerShell Core zainstaluj moduł Az tylko dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="15b13-130">Then, from a PowerShell Core session, install the Az module for the current user only.</span></span> <span data-ttu-id="15b13-131">Jest to zalecany zakres instalacji.</span><span class="sxs-lookup"><span data-stu-id="15b13-131">This is the recommended installation scope.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="15b13-132">Zainstalowanie modułu dla wszystkich użytkowników w systemie wymaga podniesionych uprawnień.</span><span class="sxs-lookup"><span data-stu-id="15b13-132">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="15b13-133">Uruchom sesję programu PowerShell przy użyciu pozycji **Uruchom jako administrator** w systemie Windows albo polecenia `sudo` w systemie macOS lub Linux:</span><span class="sxs-lookup"><span data-stu-id="15b13-133">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

## <a name="install-offline"></a><span data-ttu-id="15b13-134">Instalowanie w trybie offline</span><span class="sxs-lookup"><span data-stu-id="15b13-134">Install offline</span></span>

<span data-ttu-id="15b13-135">W niektórych środowiskach nie jest możliwe nawiązanie połączenia z galerią programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="15b13-135">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="15b13-136">W takich sytuacjach nadal możesz przeprowadzić instalację w trybie offline przy użyciu jednej z następujących metod:</span><span class="sxs-lookup"><span data-stu-id="15b13-136">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="15b13-137">Pobierz moduły do innej lokalizacji w sieci, a następnie użyj jej jako źródłowej lokalizacji instalacji.</span><span class="sxs-lookup"><span data-stu-id="15b13-137">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="15b13-138">Umożliwi to buforowanie modułów programu PowerShell na jednym serwerze lub w jednym udziale plików, a następnie wdrażanie ich za pomocą modułu PowerShellGet w dowolnym odłączonym systemie.</span><span class="sxs-lookup"><span data-stu-id="15b13-138">This allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="15b13-139">Aby dowiedzieć się, jak skonfigurować lokalne repozytorium i przeprowadzić instalację w systemach rozłączonych, zobacz [Working with local PowerShellGet repositories (Praca z lokalnymi repozytoriami modułu PowerShellGet)](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="15b13-139">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="15b13-140">[Pobierz pakiet MSI programu Azure PowerShell](install-az-ps-msi.md) na maszynę połączoną z siecią, a następnie skopiuj instalator do systemów bez dostępu do galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="15b13-140">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="15b13-141">Pamiętaj, że instalator MSI działa tylko na potrzeby programu PowerShell 5.1 w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="15b13-141">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="15b13-142">Zapisz moduł za pomocą polecenia [Save-Module](/powershell/module/PowershellGet/Save-Module) w udziale plików lub zapisz go w innej lokalizacji źródłowej, a następnie ręcznie skopiuj na inne maszyny:</span><span class="sxs-lookup"><span data-stu-id="15b13-142">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="15b13-143">Rozwiązywanie problemów</span><span class="sxs-lookup"><span data-stu-id="15b13-143">Troubleshooting</span></span>

<span data-ttu-id="15b13-144">Poniżej przedstawiono niektóre typowe problemy występujące podczas instalowania modułu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="15b13-144">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="15b13-145">Jeśli masz problem, który nie został opisany w tym miejscu, [zgłoś go w usłudze GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="15b13-145">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="15b13-146">Serwer proxy blokuje połączenie</span><span class="sxs-lookup"><span data-stu-id="15b13-146">Proxy blocks connection</span></span>

<span data-ttu-id="15b13-147">Jeśli widzisz błędy z polecenia `Install-Module`, które wskazują, że galeria programu PowerShell jest nieosiągalna, możesz znajdować się za serwerem proxy.</span><span class="sxs-lookup"><span data-stu-id="15b13-147">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="15b13-148">Różne systemy operacyjne i środowiska sieciowe mają różne wymagania dotyczące konfigurowania serwera proxy dla całego systemu.</span><span class="sxs-lookup"><span data-stu-id="15b13-148">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="15b13-149">Skontaktuj się z administratorem systemu w celu uzyskania informacji o ustawieniach serwera proxy oraz sposobie konfigurowania ich dla Twojego środowiska.</span><span class="sxs-lookup"><span data-stu-id="15b13-149">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="15b13-150">Sam program PowerShell może nie być skonfigurowany do automatycznego korzystania z tego serwera proxy.</span><span class="sxs-lookup"><span data-stu-id="15b13-150">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="15b13-151">Za pomocą programu PowerShell 5.1 lub nowszego skonfiguruj sesję programu PowerShell do użycia serwera proxy, wydając następujące polecenia:</span><span class="sxs-lookup"><span data-stu-id="15b13-151">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="15b13-152">Jeśli poświadczenia w Twoim systemie operacyjnym są skonfigurowane poprawnie, ta konfiguracja spowoduje kierowanie żądań programu PowerShell przez serwer proxy.</span><span class="sxs-lookup"><span data-stu-id="15b13-152">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="15b13-153">Aby to ustawienie utrzymywało się między sesjami, dodaj te polecenia do [profilu programu PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="15b13-153">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="15b13-154">Aby zainstalować pakiet, Twój serwer proxy musi zezwalać na połączenia HTTPS z następującym adresem:</span><span class="sxs-lookup"><span data-stu-id="15b13-154">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="15b13-155">Logowanie</span><span class="sxs-lookup"><span data-stu-id="15b13-155">Sign in</span></span>

<span data-ttu-id="15b13-156">Aby rozpocząć pracę z programem Azure PowerShell, zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="15b13-156">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="15b13-157">Jeśli wyłączono automatyczne ładowanie modułów, ręcznie zaimportuj moduł za pomocą polecenia `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="15b13-157">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="15b13-158">Ze względu na strukturę modułu może to potrwać kilka sekund.</span><span class="sxs-lookup"><span data-stu-id="15b13-158">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="15b13-159">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="15b13-159">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="15b13-160">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach programu PowerShell, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="15b13-160">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="15b13-161">Aktualizowanie modułu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="15b13-161">Update the Azure PowerShell module</span></span>

<span data-ttu-id="15b13-162">Aby zaktualizować dowolny moduł programu PowerShell, należy użyć tej samej metody, która została użyta do zainstalowania modułu.</span><span class="sxs-lookup"><span data-stu-id="15b13-162">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="15b13-163">Jeśli na przykład pierwotnie skorzystano z polecenia `Install-Module`, należy użyć polecenia [Update-Module](/powershell/module/powershellget/update-module), aby uzyskać najnowszą wersję.</span><span class="sxs-lookup"><span data-stu-id="15b13-163">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="15b13-164">Jeśli pierwotnie skorzystano z pakietu MSI, należy pobrać i zainstalować nowy pakiet MSI.</span><span class="sxs-lookup"><span data-stu-id="15b13-164">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="15b13-165">Polecenia cmdlet PowerShellGet nie mogą zaktualizować modułów, które zostały zainstalowane za pomocą pakietu MSI.</span><span class="sxs-lookup"><span data-stu-id="15b13-165">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="15b13-166">Pakiety MSI nie aktualizują modułów, które zostały zainstalowane przy użyciu modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="15b13-166">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="15b13-167">Jeśli masz problemy z aktualizacją za pomocą modułu PowerShellGet, **zainstaluj ponownie** zamiast **aktualizować**.</span><span class="sxs-lookup"><span data-stu-id="15b13-167">If you have any issues updating using PowershellGet then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="15b13-168">Ponowna instalacja jest przeprowadzana w taki sam sposób jak instalacja, ale należy dodać parametr `-Force`:</span><span class="sxs-lookup"><span data-stu-id="15b13-168">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="15b13-169">W przeciwieństwie do instalacji opartych na pakiecie MSI instalowanie lub aktualizowanie przy użyciu modułu PowerShellGet nie powoduje usunięcia starszych wersji, które mogą istnieć w systemie.</span><span class="sxs-lookup"><span data-stu-id="15b13-169">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="15b13-170">Aby usunąć stare wersje programu Azure PowerShell z systemu, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="15b13-170">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="15b13-171">Aby uzyskać więcej informacji na temat instalacji opartych na pakiecie MSI, zobacz [Instalowanie programu Azure PowerShell za pomocą pakietu MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="15b13-171">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="15b13-172">Korzystanie z wielu wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="15b13-172">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="15b13-173">Jest możliwe zainstalowanie więcej niż jednej wersji programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="15b13-173">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="15b13-174">Aby sprawdzić, czy masz wiele zainstalowanych wersji programu Azure PowerShell, użyj następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="15b13-174">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="15b13-175">Aby usunąć wersję programu Azure PowerShell, zobacz [Odinstalowywanie modułu programu Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="15b13-175">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="15b13-176">Jeśli masz zainstalowaną więcej niż jedną wersję modułu, funkcja automatycznego ładowania modułów i polecenie `Import-Module` domyślnie ładują najnowszą wersję.</span><span class="sxs-lookup"><span data-stu-id="15b13-176">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="15b13-177">Określoną wersję modułu `Az` możesz zainstalować lub załadować, używając parametru `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="15b13-177">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a><span data-ttu-id="15b13-178">Przekaż opinię</span><span class="sxs-lookup"><span data-stu-id="15b13-178">Provide feedback</span></span>

<span data-ttu-id="15b13-179">Jeśli znajdziesz usterkę w programie Azure PowerShell, [zgłoś problem w usłudze GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="15b13-179">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="15b13-180">Aby przekazać opinię z wiersza polecenia, użyj polecenia cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="15b13-180">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="15b13-181">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="15b13-181">Next Steps</span></span>

<span data-ttu-id="15b13-182">Aby dowiedzieć się więcej o modułach programu Azure PowerShell i ich funkcjach, zobacz [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="15b13-182">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="15b13-183">Jeśli znasz program Azure PowerShell i chcesz przeprowadzić migrację z modułu AzureRM, zobacz [Migrowanie z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="15b13-183">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
