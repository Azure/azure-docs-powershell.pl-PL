---
title: Instalowanie programu Azure PowerShell w systemie macOS lub Linux
description: Jak zainstalować program Azure PowerShell w systemie macOS lub Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323173"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="9674c-103">Instalowanie programu Azure PowerShell w systemie macOS lub Linux</span><span class="sxs-lookup"><span data-stu-id="9674c-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="9674c-104">W przypadku platform innych niż Windows program Azure PowerShell można uruchomić, bazując na programie PowerShell Core w wersji 6.</span><span class="sxs-lookup"><span data-stu-id="9674c-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="9674c-105">W przeciwieństwie do standardowego programu Azure PowerShell utworzonego na podstawie programu .NET Framework dla systemu Windows ten produkt jest utworzony pod kątem platformy .NET Core i może działać na dowolnej platformie, która obsługuje środowisko uruchomieniowe .Net Core.</span><span class="sxs-lookup"><span data-stu-id="9674c-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="9674c-106">W tej chwili oba programy, PowerShell Core w wersji 6 i Azure PowerShell for .NET Core, są wciąż w wersji beta.</span><span class="sxs-lookup"><span data-stu-id="9674c-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="9674c-107">Wsparcie dla tych produktów jest ograniczone.</span><span class="sxs-lookup"><span data-stu-id="9674c-107">Support for these products is limited.</span></span> <span data-ttu-id="9674c-108">Jeśli napotkasz problemy lub odkryjesz usterkę, prześlij zgłoszenie w witrynie GitHub.</span><span class="sxs-lookup"><span data-stu-id="9674c-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="9674c-109">Problemy z programem PowerShell Core w wersji 6</span><span class="sxs-lookup"><span data-stu-id="9674c-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="9674c-110">Problemy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9674c-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="9674c-111">Instalowanie programu PowerShell Core w wersji 6</span><span class="sxs-lookup"><span data-stu-id="9674c-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="9674c-112">Proces instalowania programu PowerShell Core w wersji 6 w systemie Linux lub macOS różni się zależnie od dystrybucji systemu Linux i wersji systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="9674c-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="9674c-113">Szczegółowe instrukcje można znaleźć w następujących artykułach:</span><span class="sxs-lookup"><span data-stu-id="9674c-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="9674c-114">Instalowanie programu PowerShell Core w systemie macOS</span><span class="sxs-lookup"><span data-stu-id="9674c-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="9674c-115">Instalowanie programu PowerShell Core w systemie Linux</span><span class="sxs-lookup"><span data-stu-id="9674c-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="9674c-116">Instalowanie programu Azure PowerShell dla platformy .NET Core</span><span class="sxs-lookup"><span data-stu-id="9674c-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="9674c-117">Program PowerShell Core w wersji 6 jest dostarczany z już zainstalowanym modułem PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9674c-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="9674c-118">Ułatwia to instalację modułów opublikowanych w galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9674c-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="9674c-119">Aby zainstalować program Azure PowerShell, otwórz nową sesję programu PowerShell i uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="9674c-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="9674c-120">Ładowanie modułu AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="9674c-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="9674c-121">Gdy moduł jest zainstalowany, musisz załadować moduł do swojej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9674c-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="9674c-122">Moduły są w następujący sposób ładowane przy użyciu polecenia cmdlet `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="9674c-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="9674c-123">Po zakończeniu importowania można przetestować nowo zainstalowany moduł, próbując zalogować się do platformy Azure przy użyciu następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="9674c-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="9674c-124">Powyższe polecenie powinno poprosić o przejście na stronę `https://aka.ms/devicelogin` i wprowadzenie udostępnionego kodu.</span><span class="sxs-lookup"><span data-stu-id="9674c-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="9674c-125">Dostępne polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="9674c-125">Available cmdlets</span></span>

<span data-ttu-id="9674c-126">Moduły programu Azure PowerShell dla platformy .NET Standard są ciągle w fazie opracowywania.</span><span class="sxs-lookup"><span data-stu-id="9674c-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="9674c-127">Nie oferują one pełnego zestawu poleceń cmdlet dostępnych w modułach w wersji dla systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="9674c-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="9674c-128">Następujące funkcje są implementowane w modułach AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="9674c-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="9674c-129">Zarządzanie kontami</span><span class="sxs-lookup"><span data-stu-id="9674c-129">Account management</span></span>
  - <span data-ttu-id="9674c-130">Logowanie się przy użyciu konta Microsoft, konta organizacji lub jednostki usługi za pośrednictwem usługi Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9674c-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="9674c-131">Zapisywanie poświadczeń na dysku poleceniem Save-AzureRmContext i ładowanie zapisanych poświadczeń poleceniem Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="9674c-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="9674c-132">Środowisko</span><span class="sxs-lookup"><span data-stu-id="9674c-132">Environment</span></span>
  - <span data-ttu-id="9674c-133">Pobieranie różnych gotowych środowisk platformy Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="9674c-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="9674c-134">Dodawanie/ustawianie/usuwanie dostosowanych środowisk (takich jak środowiska Azure Stack lub Windows Azure Pack)</span><span class="sxs-lookup"><span data-stu-id="9674c-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="9674c-135">Polecenia cmdlet płaszczyzny zarządzania dla usług platformy Azure korzystających z interfejsów menedżera zasobów i zarządzania usługami.</span><span class="sxs-lookup"><span data-stu-id="9674c-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="9674c-136">Maszyna wirtualna</span><span class="sxs-lookup"><span data-stu-id="9674c-136">Virtual Machine</span></span>
  - <span data-ttu-id="9674c-137">App Service (Websites)</span><span class="sxs-lookup"><span data-stu-id="9674c-137">App Service (Websites)</span></span>
  - <span data-ttu-id="9674c-138">SQL Database</span><span class="sxs-lookup"><span data-stu-id="9674c-138">SQL Database</span></span>
  - <span data-ttu-id="9674c-139">Magazyn</span><span class="sxs-lookup"><span data-stu-id="9674c-139">Storage</span></span>
  - <span data-ttu-id="9674c-140">Sieć</span><span class="sxs-lookup"><span data-stu-id="9674c-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="9674c-141">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="9674c-141">Next Steps</span></span>

<span data-ttu-id="9674c-142">Aby uzyskać więcej informacji o korzystaniu z programu Azure PowerShell, zobacz artykuł [Rozpoczynanie pracy z programem Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9674c-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
