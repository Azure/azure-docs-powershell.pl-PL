---
title: Instalowanie programu Azure PowerShell w systemie macOS lub Linux
description: Jak zainstalować program Azure PowerShell w systemie macOS lub Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 6e7d447ea9672c174e3f1d103bc56c11a7f37192
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653801"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="fb50b-103">Instalowanie programu Azure PowerShell w systemie macOS lub Linux</span><span class="sxs-lookup"><span data-stu-id="fb50b-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="fb50b-104">W przypadku platform innych niż Windows program Azure PowerShell można uruchomić w programie PowerShell Core w wersji 6.</span><span class="sxs-lookup"><span data-stu-id="fb50b-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="fb50b-105">Ta wersja programu PowerShell jest przeznaczona do użycia na każdej platformie, która obsługuje platformę .NET Core.</span><span class="sxs-lookup"><span data-stu-id="fb50b-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="fb50b-106">Do pracy z tymi platformami jest dostępna specjalna wersja programu Azure PowerShell obsługująca platformę .NET Core.</span><span class="sxs-lookup"><span data-stu-id="fb50b-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="fb50b-107">W tej chwili oba programy, PowerShell Core w wersji 6 i Azure PowerShell for .NET Core, są wciąż w wersji beta.</span><span class="sxs-lookup"><span data-stu-id="fb50b-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="fb50b-108">Wsparcie dla tych produktów jest ograniczone.</span><span class="sxs-lookup"><span data-stu-id="fb50b-108">Support for these products is limited.</span></span> <span data-ttu-id="fb50b-109">Jeśli napotkasz problemy lub odkryjesz usterkę, prześlij zgłoszenie w witrynie GitHub.</span><span class="sxs-lookup"><span data-stu-id="fb50b-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="fb50b-110">Problemy z programem PowerShell Core w wersji 6</span><span class="sxs-lookup"><span data-stu-id="fb50b-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="fb50b-111">Problemy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb50b-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="fb50b-112">Instalowanie programu PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="fb50b-112">Install PowerShell Core</span></span>

<span data-ttu-id="fb50b-113">Instrukcje dotyczące instalacji programu PowerShell Core różnią się w przypadku systemu macOS i większości dystrybucji systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="fb50b-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="fb50b-114">Szczegółowe instrukcje można znaleźć w następujących artykułach:</span><span class="sxs-lookup"><span data-stu-id="fb50b-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="fb50b-115">Instalowanie programu PowerShell Core w systemie macOS</span><span class="sxs-lookup"><span data-stu-id="fb50b-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="fb50b-116">Instalowanie programu PowerShell Core w systemie Linux</span><span class="sxs-lookup"><span data-stu-id="fb50b-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="fb50b-117">Instalowanie programu Azure PowerShell dla platformy .NET Core</span><span class="sxs-lookup"><span data-stu-id="fb50b-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="fb50b-118">Program PowerShell Core jest dostarczany z już zainstalowanym modułem PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="fb50b-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="fb50b-119">Instalacja modułów programu PowerShell wymaga podwyższonego poziomu uprawnień, więc musisz uruchomić sesję jako superużytkownik:</span><span class="sxs-lookup"><span data-stu-id="fb50b-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="fb50b-120">Aby zainstalować program Azure PowerShell, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="fb50b-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="fb50b-121">Moduł `AzureRM`, szczegółowo opisany w innych artykułach, nie jest przeznaczony dla platformy .NET Core i nie będzie współdziałać z programem PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="fb50b-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="fb50b-122">Moduły `AzureRM` i `AzureRM.NetCore` używają tych samych nazw poleceń cmdlet, więc jedyną różnicą jest nazwa modułu zbiorczego i wersja platformy .NET, z pomocą której je utworzono.</span><span class="sxs-lookup"><span data-stu-id="fb50b-122">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="fb50b-123">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="fb50b-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="fb50b-124">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="fb50b-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="fb50b-125">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="fb50b-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="fb50b-126">Logowanie</span><span class="sxs-lookup"><span data-stu-id="fb50b-126">Sign in</span></span>

<span data-ttu-id="fb50b-127">Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `AzureRM.Netcore` w sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fb50b-127">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="fb50b-128">Zaimportowanie modułu __nie__ wymaga podwyższonego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="fb50b-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="fb50b-129">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="fb50b-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="fb50b-130">Automatyczne zaimportowanie modułu `AzureRM` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="fb50b-130">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="fb50b-131">W systemach macOS i Linux należy pracować z profilem, używając zmiennej środowiskowej `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="fb50b-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="fb50b-132">Aby dowiedzieć się, jak można utrwalić swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="fb50b-132">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="fb50b-133">Dostępne polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="fb50b-133">Available cmdlets</span></span>

<span data-ttu-id="fb50b-134">Moduły programu Azure PowerShell dla platformy .NET Core są ciągle w fazie opracowywania.</span><span class="sxs-lookup"><span data-stu-id="fb50b-134">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="fb50b-135">Nie oferują one pełnego zestawu poleceń cmdlet dostępnych w modułach w wersji dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="fb50b-135">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="fb50b-136">Następujące funkcje są implementowane w modułach AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="fb50b-136">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="fb50b-137">Zarządzanie kontami</span><span class="sxs-lookup"><span data-stu-id="fb50b-137">Account management</span></span>
  * <span data-ttu-id="fb50b-138">Logowanie się przy użyciu konta Microsoft, konta organizacji lub jednostki usługi za pośrednictwem usługi Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fb50b-138">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="fb50b-139">Zapisywanie poświadczeń na dysku poleceniem Save-AzureRmContext i ładowanie zapisanych poświadczeń poleceniem Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="fb50b-139">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="fb50b-140">Środowisko</span><span class="sxs-lookup"><span data-stu-id="fb50b-140">Environment</span></span>
  * <span data-ttu-id="fb50b-141">Pobieranie różnych gotowych środowisk platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="fb50b-141">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="fb50b-142">Dodawanie/ustawianie/usuwanie dostosowanych środowisk (takich jak środowiska Azure Stack lub Windows Azure Pack)</span><span class="sxs-lookup"><span data-stu-id="fb50b-142">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="fb50b-143">Polecenia cmdlet płaszczyzny zarządzania dla usług platformy Azure korzystających z interfejsów menedżera zasobów i zarządzania usługami.</span><span class="sxs-lookup"><span data-stu-id="fb50b-143">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="fb50b-144">Maszyna wirtualna</span><span class="sxs-lookup"><span data-stu-id="fb50b-144">Virtual Machine</span></span>
  * <span data-ttu-id="fb50b-145">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="fb50b-145">App Service (Websites)</span></span>
  * <span data-ttu-id="fb50b-146">SQL Database</span><span class="sxs-lookup"><span data-stu-id="fb50b-146">SQL Database</span></span>
  * <span data-ttu-id="fb50b-147">Magazyn</span><span class="sxs-lookup"><span data-stu-id="fb50b-147">Storage</span></span>
  * <span data-ttu-id="fb50b-148">Sieć</span><span class="sxs-lookup"><span data-stu-id="fb50b-148">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="fb50b-149">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="fb50b-149">Next Steps</span></span>

<span data-ttu-id="fb50b-150">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="fb50b-150">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
