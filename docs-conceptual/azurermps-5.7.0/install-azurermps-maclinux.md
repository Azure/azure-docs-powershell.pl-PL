---
title: Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux | Microsoft Docs
description: Jak zainstalować i skonfigurować program Azure PowerShell do pierwszego użycia w systemach macOS i Linux.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 7228ca9791f174cb3554dd359b3723e98589ee17
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="0732e-103">Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux</span><span class="sxs-lookup"><span data-stu-id="0732e-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="0732e-104">Teraz jest możliwa instalacja programów PowerShell Core w wersji 6 i Azure PowerShell na platformach innych niż Windows.</span><span class="sxs-lookup"><span data-stu-id="0732e-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="0732e-105">Proces instalowania programu Azure PowerShell w systemach macOS i Linux nie różni się zbytnio od instalowania w systemie Windows, należy jednak najpierw zainstalować program PowerShell Core w wersji 6.</span><span class="sxs-lookup"><span data-stu-id="0732e-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="0732e-106">W tej chwili oba programy, PowerShell Core w wersji 6 i Azure PowerShell for .NET Core, są wciąż w wersji beta.</span><span class="sxs-lookup"><span data-stu-id="0732e-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="0732e-107">Wsparcie dla tych produktów jest ograniczone.</span><span class="sxs-lookup"><span data-stu-id="0732e-107">Support for these products is limited.</span></span> <span data-ttu-id="0732e-108">Jeśli napotkasz problemy lub odkryjesz usterkę, zarejestruj problemy w witrynie GitHub.</span><span class="sxs-lookup"><span data-stu-id="0732e-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="0732e-109">Problemy z programem PowerShell Core w wersji 6</span><span class="sxs-lookup"><span data-stu-id="0732e-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="0732e-110">Problemy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0732e-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="0732e-111">Krok 1. Instalowanie programu PowerShell Core w wersji 6</span><span class="sxs-lookup"><span data-stu-id="0732e-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="0732e-112">Proces instalowania programu PowerShell Core w wersji 6 różni się zależnie od docelowego systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0732e-112">The process of installing PowerShell Core v6 varies depending on the target operating system.</span></span>
<span data-ttu-id="0732e-113">Chociaż istnieje możliwość zainstalowania programu PowerShell Core w wersji 6 w systemie Windows, ten artykuł koncentruje się na systemach macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="0732e-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="0732e-114">Jeśli chcesz korzystać z programu Azure PowerShell w systemie Windows, zobacz artykuł poświęcony [instalacji](./install-azurerm-ps.md) w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="0732e-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="0732e-115">Proces instalowania programu **PowerShell Core w wersji 6** w systemie Linux lub macOS różni się zależnie od dystrybucji systemu Linux i wersji systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="0732e-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="0732e-116">Szczegółowe instrukcje można znaleźć w następującym artykule:</span><span class="sxs-lookup"><span data-stu-id="0732e-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="0732e-117">Instalowanie programu PowerShell Core w systemach macOS i Linux</span><span class="sxs-lookup"><span data-stu-id="0732e-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="0732e-118">Krok 2. Instalowanie programu Azure PowerShell dla platformy .NET Core</span><span class="sxs-lookup"><span data-stu-id="0732e-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="0732e-119">Program PowerShell Core w wersji 6 jest dostarczany z już zainstalowanym modułem PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0732e-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="0732e-120">Ułatwia to instalację modułów opublikowanych w galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0732e-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="0732e-121">Aby zainstalować program Azure PowerShell, otwórz nową sesję programu PowerShell i uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="0732e-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="0732e-122">Krok 3. Ładowanie modułu AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="0732e-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="0732e-123">Gdy moduł jest zainstalowany, musisz załadować moduł do swojej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0732e-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="0732e-124">Moduły są w następujący sposób ładowane przy użyciu polecenia cmdlet `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="0732e-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="0732e-125">Po zakończeniu importowania można przetestować nowo zainstalowany moduł, próbując zalogować się do platformy Azure przy użyciu następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="0732e-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="0732e-126">Powyższe polecenie powinno poprosić o przejście na stronę `https://aka.ms/devicelogin` i wprowadzenie udostępnionego kodu.</span><span class="sxs-lookup"><span data-stu-id="0732e-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="0732e-127">Dostępne polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="0732e-127">Available cmdlets</span></span>

<span data-ttu-id="0732e-128">Moduły programu Azure PowerShell dla platformy .NET Standard są ciągle w fazie opracowywania.</span><span class="sxs-lookup"><span data-stu-id="0732e-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="0732e-129">Nie oferują one pełnego zestawu poleceń cmdlet dostępnych w modułach w wersji dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="0732e-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="0732e-130">Następujące funkcje są implementowane w modułach AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="0732e-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="0732e-131">Zarządzanie kontami</span><span class="sxs-lookup"><span data-stu-id="0732e-131">Account management</span></span>
  - <span data-ttu-id="0732e-132">Logowanie się przy użyciu konta Microsoft, konta organizacji lub jednostki usługi za pośrednictwem usługi Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0732e-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="0732e-133">Zapisywanie poświadczeń na dysku poleceniem Save-AzureRmContext i ładowanie zapisanych poświadczeń poleceniem Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="0732e-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="0732e-134">Środowisko</span><span class="sxs-lookup"><span data-stu-id="0732e-134">Environment</span></span>
  - <span data-ttu-id="0732e-135">Pobieranie różnych gotowych środowisk platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="0732e-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="0732e-136">Dodawanie/ustawianie/usuwanie dostosowanych środowisk (takich jak środowiska Azure Stack lub Windows Azure Pack)</span><span class="sxs-lookup"><span data-stu-id="0732e-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="0732e-137">Polecenia cmdlet płaszczyzny zarządzania dla usług platformy Azure korzystających z interfejsów menedżera zasobów i zarządzania usługami.</span><span class="sxs-lookup"><span data-stu-id="0732e-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="0732e-138">Maszyna wirtualna</span><span class="sxs-lookup"><span data-stu-id="0732e-138">Virtual Machine</span></span>
  - <span data-ttu-id="0732e-139">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="0732e-139">App Service (Websites)</span></span>
  - <span data-ttu-id="0732e-140">SQL Database</span><span class="sxs-lookup"><span data-stu-id="0732e-140">SQL Database</span></span>
  - <span data-ttu-id="0732e-141">Magazyn</span><span class="sxs-lookup"><span data-stu-id="0732e-141">Storage</span></span>
  - <span data-ttu-id="0732e-142">Sieć</span><span class="sxs-lookup"><span data-stu-id="0732e-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="0732e-143">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="0732e-143">Next Steps</span></span>

<span data-ttu-id="0732e-144">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0732e-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
