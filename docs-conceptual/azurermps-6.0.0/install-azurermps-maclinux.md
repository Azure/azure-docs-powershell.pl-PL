---
title: Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux | Microsoft Docs
description: Jak zainstalować i skonfigurować program Azure PowerShell do pierwszego użycia w systemach macOS i Linux.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: eed7a35fcf20a17c83d9e5e3272be4b77fa12c34
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="a4750-103">Instalowanie i konfigurowanie programu Azure PowerShell w systemach macOS i Linux</span><span class="sxs-lookup"><span data-stu-id="a4750-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="a4750-104">Teraz jest możliwa instalacja programów PowerShell Core w wersji 6 i Azure PowerShell na platformach innych niż Windows.</span><span class="sxs-lookup"><span data-stu-id="a4750-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="a4750-105">Proces instalowania programu Azure PowerShell w systemach macOS i Linux nie różni się zbytnio od instalowania w systemie Windows, należy jednak najpierw zainstalować program PowerShell Core w wersji 6.</span><span class="sxs-lookup"><span data-stu-id="a4750-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="a4750-106">W tej chwili oba programy, PowerShell Core w wersji 6 i Azure PowerShell for .NET Core, są wciąż w wersji beta.</span><span class="sxs-lookup"><span data-stu-id="a4750-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="a4750-107">Wsparcie dla tych produktów jest ograniczone.</span><span class="sxs-lookup"><span data-stu-id="a4750-107">Support for these products is limited.</span></span> <span data-ttu-id="a4750-108">Jeśli napotkasz problemy lub odkryjesz usterkę, zarejestruj problemy w witrynie GitHub.</span><span class="sxs-lookup"><span data-stu-id="a4750-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="a4750-109">Problemy z programem PowerShell Core w wersji 6</span><span class="sxs-lookup"><span data-stu-id="a4750-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="a4750-110">Problemy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a4750-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="a4750-111">Krok 1. Instalowanie programu PowerShell Core w wersji 6</span><span class="sxs-lookup"><span data-stu-id="a4750-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="a4750-112">Proces instalowania programu PowerShell Core w wersji 6 różni się zależnie od docelowego systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="a4750-112">The process of installing PowerShell Core v6 varies depending on the target operating system.</span></span>
<span data-ttu-id="a4750-113">Chociaż istnieje możliwość zainstalowania programu PowerShell Core w wersji 6 w systemie Windows, ten artykuł koncentruje się na systemach macOS i Linux.</span><span class="sxs-lookup"><span data-stu-id="a4750-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="a4750-114">Jeśli chcesz korzystać z programu Azure PowerShell w systemie Windows, zobacz artykuł poświęcony [instalacji](./install-azurerm-ps.md) w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="a4750-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="a4750-115">Proces instalowania programu **PowerShell Core w wersji 6** w systemie Linux lub macOS różni się zależnie od dystrybucji systemu Linux i wersji systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="a4750-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="a4750-116">Szczegółowe instrukcje można znaleźć w następującym artykule:</span><span class="sxs-lookup"><span data-stu-id="a4750-116">Detailed instructions can be found in the following article:</span></span>

- [<span data-ttu-id="a4750-117">Instalowanie programu PowerShell Core w systemach macOS i Linux</span><span class="sxs-lookup"><span data-stu-id="a4750-117">Installing PowerShell Core on macOS and Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="a4750-118">Krok 2. Instalowanie programu Azure PowerShell dla platformy .NET Core</span><span class="sxs-lookup"><span data-stu-id="a4750-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="a4750-119">Program PowerShell Core w wersji 6 jest dostarczany z już zainstalowanym modułem PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="a4750-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="a4750-120">Ułatwia to instalację modułów opublikowanych w galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4750-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="a4750-121">Aby zainstalować program Azure PowerShell, otwórz nową sesję programu PowerShell i uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="a4750-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="a4750-122">Krok 3. Ładowanie modułu AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="a4750-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="a4750-123">Gdy moduł jest zainstalowany, musisz załadować moduł do swojej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4750-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="a4750-124">Moduły są w następujący sposób ładowane przy użyciu polecenia cmdlet `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="a4750-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="a4750-125">Po zakończeniu importowania można przetestować nowo zainstalowany moduł, próbując zalogować się do platformy Azure przy użyciu następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="a4750-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="a4750-126">Powyższe polecenie powinno poprosić o przejście na stronę `https://aka.ms/devicelogin` i wprowadzenie udostępnionego kodu.</span><span class="sxs-lookup"><span data-stu-id="a4750-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="a4750-127">Dostępne polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="a4750-127">Available cmdlets</span></span>

<span data-ttu-id="a4750-128">Moduły programu Azure PowerShell dla platformy .NET Standard są ciągle w fazie opracowywania.</span><span class="sxs-lookup"><span data-stu-id="a4750-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="a4750-129">Nie oferują one pełnego zestawu poleceń cmdlet dostępnych w modułach w wersji dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="a4750-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="a4750-130">Następujące funkcje są implementowane w modułach AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="a4750-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="a4750-131">Zarządzanie kontami</span><span class="sxs-lookup"><span data-stu-id="a4750-131">Account management</span></span>
  - <span data-ttu-id="a4750-132">Logowanie się przy użyciu konta Microsoft, konta organizacji lub jednostki usługi za pośrednictwem usługi Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a4750-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="a4750-133">Zapisywanie poświadczeń na dysku poleceniem Save-AzureRmContext i ładowanie zapisanych poświadczeń poleceniem Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a4750-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="a4750-134">Środowisko</span><span class="sxs-lookup"><span data-stu-id="a4750-134">Environment</span></span>
  - <span data-ttu-id="a4750-135">Pobieranie różnych gotowych środowisk platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="a4750-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="a4750-136">Dodawanie/ustawianie/usuwanie dostosowanych środowisk (takich jak środowiska Azure Stack lub Windows Azure Pack)</span><span class="sxs-lookup"><span data-stu-id="a4750-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="a4750-137">Polecenia cmdlet płaszczyzny zarządzania dla usług platformy Azure korzystających z interfejsów menedżera zasobów i zarządzania usługami.</span><span class="sxs-lookup"><span data-stu-id="a4750-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="a4750-138">Maszyna wirtualna</span><span class="sxs-lookup"><span data-stu-id="a4750-138">Virtual Machine</span></span>
  - <span data-ttu-id="a4750-139">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="a4750-139">App Service (Websites)</span></span>
  - <span data-ttu-id="a4750-140">SQL Database</span><span class="sxs-lookup"><span data-stu-id="a4750-140">SQL Database</span></span>
  - <span data-ttu-id="a4750-141">Magazyn</span><span class="sxs-lookup"><span data-stu-id="a4750-141">Storage</span></span>
  - <span data-ttu-id="a4750-142">Sieć</span><span class="sxs-lookup"><span data-stu-id="a4750-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="a4750-143">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="a4750-143">Next Steps</span></span>

<span data-ttu-id="a4750-144">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="a4750-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
