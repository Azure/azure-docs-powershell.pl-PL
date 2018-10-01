---
title: Instalowanie programu Azure PowerShell w systemie macOS lub Linux
description: Jak zainstalować program Azure PowerShell w systemie macOS lub Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560120"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="1af35-103">Instalowanie programu Azure PowerShell w systemie macOS lub Linux</span><span class="sxs-lookup"><span data-stu-id="1af35-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="1af35-104">W przypadku platform innych niż Windows program Azure PowerShell można uruchomić w programie PowerShell Core w wersji 6.</span><span class="sxs-lookup"><span data-stu-id="1af35-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="1af35-105">Ta wersja programu PowerShell jest przeznaczona do użycia na każdej platformie, która obsługuje platformę .NET Core.</span><span class="sxs-lookup"><span data-stu-id="1af35-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="1af35-106">W przypadku pracy z tymi platformami jest dostępna wersja programu Azure PowerShell obsługująca wersję platformy .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="1af35-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="1af35-107">W tej chwili oba programy, PowerShell Core w wersji 6 i Azure PowerShell for .NET Core, są wciąż w wersji beta.</span><span class="sxs-lookup"><span data-stu-id="1af35-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="1af35-108">Wsparcie dla tych produktów jest ograniczone.</span><span class="sxs-lookup"><span data-stu-id="1af35-108">Support for these products is limited.</span></span> <span data-ttu-id="1af35-109">Jeśli napotkasz problemy lub odkryjesz usterkę, prześlij zgłoszenie w witrynie GitHub.</span><span class="sxs-lookup"><span data-stu-id="1af35-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="1af35-110">Problemy z programem PowerShell Core w wersji 6</span><span class="sxs-lookup"><span data-stu-id="1af35-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="1af35-111">Problemy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1af35-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="1af35-112">Instalowanie programu PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="1af35-112">Install PowerShell Core</span></span>

<span data-ttu-id="1af35-113">Instrukcje dotyczące instalacji programu PowerShell Core różnią się w przypadku systemu macOS i większości dystrybucji systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="1af35-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="1af35-114">Szczegółowe instrukcje można znaleźć w następujących artykułach:</span><span class="sxs-lookup"><span data-stu-id="1af35-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="1af35-115">Instalowanie programu PowerShell Core w systemie macOS</span><span class="sxs-lookup"><span data-stu-id="1af35-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="1af35-116">Instalowanie programu PowerShell Core w systemie Linux</span><span class="sxs-lookup"><span data-stu-id="1af35-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="1af35-117">Instalowanie programu Azure PowerShell dla platformy .NET Core</span><span class="sxs-lookup"><span data-stu-id="1af35-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="1af35-118">Program PowerShell Core jest dostarczany z już zainstalowanym modułem PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1af35-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="1af35-119">Instalacja modułów programu PowerShell wymaga podwyższonego poziomu uprawnień, więc musisz uruchomić sesję jako superużytkownik:</span><span class="sxs-lookup"><span data-stu-id="1af35-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="1af35-120">Aby zainstalować program Azure PowerShell, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="1af35-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!IMPORTANT]
> <span data-ttu-id="1af35-121">Moduł `AzureRM`, szczegółowo opisany w innych artykułach, nie jest przeznaczony dla platformy .NET Core i nie będzie współdziałać z programem PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="1af35-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="1af35-122">Moduły `Az` zawierają aliasy poleceń dla wszystkich poleceń cmdlet `AzureRM`, dlatego ma zastosowanie cała dokumentacja dotycząca usługi `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="1af35-122">The `Az` modules contain command aliases for all `AzureRM` cmdlets, so all of the documentation for `AzureRM` applies.</span></span>

<span data-ttu-id="1af35-123">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1af35-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="1af35-124">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="1af35-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="1af35-125">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="1af35-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="1af35-126">Logowanie</span><span class="sxs-lookup"><span data-stu-id="1af35-126">Sign in</span></span>

<span data-ttu-id="1af35-127">Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `Az` w sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1af35-127">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="1af35-128">Zaimportowanie modułu __nie__ wymaga podwyższonego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="1af35-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="1af35-129">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="1af35-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1af35-130">Automatyczne zaimportowanie modułu `Az` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="1af35-130">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="1af35-131">W systemach macOS i Linux należy pracować z profilem, używając zmiennej środowiskowej `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="1af35-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="1af35-132">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1af35-132">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="1af35-133">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="1af35-133">Next Steps</span></span>

<span data-ttu-id="1af35-134">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1af35-134">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
