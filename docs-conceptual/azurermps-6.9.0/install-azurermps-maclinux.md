---
title: Instalowanie programu Azure PowerShell w systemie macOS lub Linux
description: Jak zainstalować program Azure PowerShell w systemie macOS lub Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/24/2018
ms.openlocfilehash: 05e86d96b345455f3d3bb3fe6dedf933fff6187c
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179245"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="a4a6d-103">Instalowanie programu Azure PowerShell w systemie macOS lub Linux</span><span class="sxs-lookup"><span data-stu-id="a4a6d-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="a4a6d-104">W przypadku platform innych niż Windows program Azure PowerShell można uruchomić w programie PowerShell Core w wersji 6.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="a4a6d-105">Ta wersja programu PowerShell jest przeznaczona do użycia na każdej platformie, która obsługuje platformę .NET Core.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="a4a6d-106">W przypadku pracy z tymi platformami jest dostępna wersja programu Azure PowerShell obsługująca wersję platformy .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="a4a6d-107">W tej chwili oba programy, PowerShell Core w wersji 6 i Azure PowerShell for .NET Standard, są wciąż w wersji beta.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Standard are still in beta.</span></span>
> <span data-ttu-id="a4a6d-108">Wsparcie dla tych produktów jest ograniczone.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-108">Support for these products is limited.</span></span> <span data-ttu-id="a4a6d-109">Jeśli napotkasz problemy lub odkryjesz usterkę, prześlij zgłoszenie w witrynie GitHub.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="a4a6d-110">Problemy z programem PowerShell Core w wersji 6</span><span class="sxs-lookup"><span data-stu-id="a4a6d-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="a4a6d-111">Problemy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a4a6d-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="a4a6d-112">Instalowanie programu PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="a4a6d-112">Install PowerShell Core</span></span>

<span data-ttu-id="a4a6d-113">Instrukcje dotyczące instalacji programu PowerShell Core różnią się w przypadku systemu macOS i większości dystrybucji systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="a4a6d-114">Szczegółowe instrukcje można znaleźć w następujących artykułach:</span><span class="sxs-lookup"><span data-stu-id="a4a6d-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="a4a6d-115">Instalowanie programu PowerShell Core w systemie macOS</span><span class="sxs-lookup"><span data-stu-id="a4a6d-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="a4a6d-116">Instalowanie programu PowerShell Core w systemie Linux</span><span class="sxs-lookup"><span data-stu-id="a4a6d-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="a4a6d-117">Instalowanie programu Azure PowerShell dla platformy .NET Standard</span><span class="sxs-lookup"><span data-stu-id="a4a6d-117">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4a6d-118">Moduł `AzureRM` szczegółowo opisany w innych artykułach nie współpracuje z programem PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-118">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="a4a6d-119">Należy zainstalować moduł `Az`, aby uzyskać dostęp do funkcji Azure PowerShell w programie PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-119">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="a4a6d-120">Program PowerShell Core jest dostarczany z już zainstalowanym modułem PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-120">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="a4a6d-121">Uruchom program PowerShell przy użyciu następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="a4a6d-121">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="a4a6d-122">Aby zainstalować program Azure PowerShell, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="a4a6d-122">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="a4a6d-123">Jeśli podczas próby zainstalowania modułu wystąpi błąd uprawnień, być może trzeba będzie uruchomić program PowerShell w trybie administratora, aby zainstalować moduły.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-123">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="a4a6d-124">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-124">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="a4a6d-125">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="a4a6d-125">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="a4a6d-126">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-126">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="a4a6d-127">Włączanie aliasów</span><span class="sxs-lookup"><span data-stu-id="a4a6d-127">Enable aliases</span></span>

<span data-ttu-id="a4a6d-128">W celu zachowania zgodności z istniejącym modułem `AzureRM` nowy moduł `Az` może tworzyć aliasy zgodne z poprzednimi wersjami dla poleceń cmdlet `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-128">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="a4a6d-129">Przed rozpoczęciem korzystania z modułu po raz pierwszy należy ustawić te aliasy za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="a4a6d-129">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="a4a6d-130">Spowoduje to skonfigurowanie aliasów tylko dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-130">This sets up aliases for the current user only.</span></span> <span data-ttu-id="a4a6d-131">Sprawdź w pomocy dotyczącej poleceń cmdlet informacje na temat innych wartości, które można przekazać do opcji `-Scope` w celu skonfigurowania aliasów.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-131">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="a4a6d-132">Jeśli wystąpi błąd związany z lokalizacją ścieżki, upewnij się, czy istnieje ona w systemie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-132">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="a4a6d-133">W przypadku zakresu `CurrentUser` ten błąd można naprawić, uruchamiając następujące polecenie w narzędziu `bash`:</span><span class="sxs-lookup"><span data-stu-id="a4a6d-133">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="a4a6d-134">Logowanie</span><span class="sxs-lookup"><span data-stu-id="a4a6d-134">Sign in</span></span>

<span data-ttu-id="a4a6d-135">Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `Az` w sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-135">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="a4a6d-136">Zaimportowanie modułu __nie__ wymaga podwyższonego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-136">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="a4a6d-137">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-137">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="a4a6d-138">Automatyczne zaimportowanie modułu `Az` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="a4a6d-138">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="a4a6d-139">W systemach macOS i Linux należy pracować z profilem, używając zmiennej środowiskowej `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="a4a6d-139">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="a4a6d-140">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="a4a6d-140">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="a4a6d-141">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="a4a6d-141">Next Steps</span></span>

<span data-ttu-id="a4a6d-142">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="a4a6d-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
