---
title: Instalowanie programu Azure PowerShell w systemie macOS lub Linux
description: Jak zainstalować program Azure PowerShell w systemie macOS lub Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212895"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="bf9e1-103">Instalowanie programu Azure PowerShell w systemie macOS lub Linux</span><span class="sxs-lookup"><span data-stu-id="bf9e1-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="bf9e1-104">W przypadku platform innych niż Windows program Azure PowerShell można uruchomić w programie PowerShell Core w wersji 6.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="bf9e1-105">Ta wersja programu PowerShell jest przeznaczona do użycia na każdej platformie, która obsługuje platformę .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="bf9e1-106">W przypadku pracy z tymi platformami jest dostępna wersja programu Azure PowerShell obsługująca wersję platformy .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="bf9e1-107">Obecnie program Azure PowerShell dla platformy .NET Standard nadal jest w wersji beta.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-107">At this time, Azure PowerShell for .NET Standard is still in beta.</span></span>
> <span data-ttu-id="bf9e1-108">Jeśli napotkasz problemy lub odkryjesz usterkę, prześlij zgłoszenie w witrynie GitHub.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="bf9e1-109">Problemy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="bf9e1-109">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="bf9e1-110">Instalowanie programu PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="bf9e1-110">Install PowerShell Core</span></span>

<span data-ttu-id="bf9e1-111">Instrukcje dotyczące instalacji programu PowerShell Core różnią się w przypadku systemu macOS i większości dystrybucji systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-111">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="bf9e1-112">Szczegółowe instrukcje można znaleźć w następujących artykułach:</span><span class="sxs-lookup"><span data-stu-id="bf9e1-112">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="bf9e1-113">Instalowanie programu PowerShell Core w systemie macOS</span><span class="sxs-lookup"><span data-stu-id="bf9e1-113">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="bf9e1-114">Instalowanie programu PowerShell Core w systemie Linux</span><span class="sxs-lookup"><span data-stu-id="bf9e1-114">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="bf9e1-115">Instalowanie programu Azure PowerShell dla platformy .NET Standard</span><span class="sxs-lookup"><span data-stu-id="bf9e1-115">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf9e1-116">Moduł `AzureRM` szczegółowo opisany w innych artykułach nie współpracuje z programem PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-116">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="bf9e1-117">Należy zainstalować moduł `Az`, aby uzyskać dostęp do funkcji Azure PowerShell w programie PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-117">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="bf9e1-118">Program PowerShell Core jest dostarczany z już zainstalowanym modułem PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="bf9e1-119">Uruchom program PowerShell przy użyciu następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="bf9e1-119">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="bf9e1-120">Aby zainstalować program Azure PowerShell, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="bf9e1-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="bf9e1-121">Jeśli podczas próby zainstalowania modułu wystąpi błąd uprawnień, być może trzeba będzie uruchomić program PowerShell w trybie administratora, aby zainstalować moduły.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-121">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="bf9e1-122">Galeria programu PowerShell domyślnie nie jest skonfigurowana jako zaufane repozytorium modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="bf9e1-123">Po pierwszym użyciu Galerii programu PowerShell zostanie wyświetlony następujący komunikat:</span><span class="sxs-lookup"><span data-stu-id="bf9e1-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="bf9e1-124">Wybierz odpowiedź `Yes` lub `Yes to All`, aby kontynuować instalację.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="bf9e1-125">Włączanie aliasów</span><span class="sxs-lookup"><span data-stu-id="bf9e1-125">Enable aliases</span></span>

<span data-ttu-id="bf9e1-126">W celu zachowania zgodności z istniejącym modułem `AzureRM` nowy moduł `Az` może tworzyć aliasy zgodne z poprzednimi wersjami dla poleceń cmdlet `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-126">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="bf9e1-127">Przed rozpoczęciem korzystania z modułu po raz pierwszy należy ustawić te aliasy za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="bf9e1-127">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="bf9e1-128">Spowoduje to skonfigurowanie aliasów tylko dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-128">This sets up aliases for the current user only.</span></span> <span data-ttu-id="bf9e1-129">Sprawdź w pomocy dotyczącej poleceń cmdlet informacje na temat innych wartości, które można przekazać do opcji `-Scope` w celu skonfigurowania aliasów.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-129">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="bf9e1-130">Jeśli wystąpi błąd związany z lokalizacją ścieżki, upewnij się, czy istnieje ona w systemie lokalnym.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-130">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="bf9e1-131">W przypadku zakresu `CurrentUser` ten błąd można naprawić, uruchamiając następujące polecenie w narzędziu `bash`:</span><span class="sxs-lookup"><span data-stu-id="bf9e1-131">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="bf9e1-132">Logowanie</span><span class="sxs-lookup"><span data-stu-id="bf9e1-132">Sign in</span></span>

<span data-ttu-id="bf9e1-133">Aby rozpocząć pracę z programem Azure PowerShell, musisz załadować moduł `Az` w sesji programu PowerShell przy użyciu polecenia cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), a następnie zaloguj się przy użyciu swoich poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-133">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="bf9e1-134">Zaimportowanie modułu __nie__ wymaga podwyższonego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-134">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="bf9e1-135">Musisz powtórzyć te kroki dla każdej nowej sesji programu PowerShell, którą rozpoczniesz.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-135">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="bf9e1-136">Automatyczne zaimportowanie modułu `Az` wymaga skonfigurowania profilu programu PowerShell — więcej informacji na ten temat można znaleźć na stronie [About Profiles (Informacje o profilach)](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="bf9e1-136">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="bf9e1-137">W systemach macOS i Linux należy pracować z profilem, używając zmiennej środowiskowej `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="bf9e1-137">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="bf9e1-138">Aby dowiedzieć się, jak można utrwalić logowanie się do swojego konta platformy Azure w wielu sesjach, zobacz [Utrwalanie poświadczeń użytkownika między sesjami programu PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="bf9e1-138">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="bf9e1-139">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="bf9e1-139">Next Steps</span></span>

<span data-ttu-id="bf9e1-140">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="bf9e1-140">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
