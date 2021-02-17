---
title: Instalowanie i konfigurowanie modułu zarządzania usługami programu Azure PowerShell | Microsoft Docs
description: Jak zainstalować i skonfigurować program Azure PowerShell do pierwszego użycia.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 23ea4bcbd182cf1b063f2ae90921217de74a7044
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401525"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="b41ee-103">Instalowanie modułu zarządzania usługami programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b41ee-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="b41ee-104">Instalowanie programu Azure PowerShell z [Galerii programu PowerShell](https://www.powershellgallery.com/) jest preferowaną metodą instalacji.</span><span class="sxs-lookup"><span data-stu-id="b41ee-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="b41ee-105">Krok 1. Zainstaluj moduł PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="b41ee-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="b41ee-106">Instalowanie elementów z Galerii programu PowerShell wymaga modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="b41ee-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="b41ee-107">Upewnij się, że masz odpowiednią wersję modułu PowerShellGet oraz spełnione inne wymagania systemowe.</span><span class="sxs-lookup"><span data-stu-id="b41ee-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="b41ee-108">Uruchom następujące polecenie, aby sprawdzić, czy w Twoim systemie został zainstalowany moduł PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="b41ee-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

<span data-ttu-id="b41ee-109">Powinny zostać wyświetlone dane wyjściowe podobne do poniższych:</span><span class="sxs-lookup"><span data-stu-id="b41ee-109">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="b41ee-110">Jeśli nie masz zainstalowanego modułu PowerShellGet, zobacz sekcję [Jak uzyskać moduł PowerShellGet](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="b41ee-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="b41ee-111">Krok 2. Zainstaluj program Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b41ee-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="b41ee-112">Uruchom następujące polecenie z poziomu konsoli programu Windows PowerShell jako administrator:</span><span class="sxs-lookup"><span data-stu-id="b41ee-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="b41ee-113">Moduł Azure to zbiorczy moduł poleceń cmdlet usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b41ee-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="b41ee-114">Po zainstalowaniu modułu AzureRM każdy moduł platformy Azure, który nie został wcześniej zainstalowany, zostanie pobrany i zainstalowany z Galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b41ee-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="b41ee-115">Moduł zarządzania usługami platformy Azure udostępnia zależności z modułami usługi Azure PowerShell Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b41ee-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="b41ee-116">Jeśli masz zainstalowane moduły usługi Azure PowerShell Resource Manager, musisz dodać parametr `-AllowClobber` do polecenia instalacji.</span><span class="sxs-lookup"><span data-stu-id="b41ee-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="b41ee-117">Umożliwi to aktualizowanie istniejących udostępnionych zależności.</span><span class="sxs-lookup"><span data-stu-id="b41ee-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="b41ee-118">Bez tego parametru nie można zainstalować modułu.</span><span class="sxs-lookup"><span data-stu-id="b41ee-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="b41ee-119">Po zainstalowaniu tego modułu należy zaimportować moduł za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="b41ee-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="b41ee-120">Aby korzystać z poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="b41ee-120">To use the cmdlets</span></span>

<span data-ttu-id="b41ee-121">Aby rozpocząć pracę z poleceniami cmdlet zarządzania usługami platformy Azure, najpierw zaloguj się do konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b41ee-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="b41ee-122">Aby zalogować się do konta, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="b41ee-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="b41ee-123">Gdy zalogujesz się do platformy Azure, program Azure PowerShell utworzy kontekst dla danej sesji.</span><span class="sxs-lookup"><span data-stu-id="b41ee-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="b41ee-124">Ten kontekst zawiera środowisko, konto, dzierżawę i subskrypcję programu Azure PowerShell, które będą używane dla wszystkich poleceń cmdlet w tej sesji.</span><span class="sxs-lookup"><span data-stu-id="b41ee-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="b41ee-125">Teraz możesz używać poniższych modułów.</span><span class="sxs-lookup"><span data-stu-id="b41ee-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="b41ee-126">Polecenia cmdlet zarządzania usługami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b41ee-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="b41ee-127">Moduły programu Azure PowerShell są często aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="b41ee-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="b41ee-128">Jeśli zauważysz, że pomoc online do polecenia cmdlet zawiera polecenia cmdlet lub parametry, których nie ma w module, pobierz i zainstaluj najnowszą wersję modułu.</span><span class="sxs-lookup"><span data-stu-id="b41ee-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="b41ee-129">Aby znaleźć wersji modułu, wpisz: `(Get-InstalledModule Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="b41ee-129">To find the version of your module, type: `(Get-InstalledModule Azure).Version`.</span></span>

<span data-ttu-id="b41ee-130">Przykładowe skrypty, które mogą pomóc zautomatyzować niektóre typowe zadania na platformie Azure, można znaleźć w temacie [Centrum skryptów Microsoft Azure](https://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="b41ee-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](https://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="b41ee-131">Ogólne informacje na temat instalowania, używania i dostosowywania środowiska programu Windows PowerShell oraz powiązanych szkoleń można znaleźć w temacie [Scripting with Windows PowerShell](/powershell/scripting/learn/ps101/00-introduction) (Obsługa skryptów w programie Windows PowerShell).</span><span class="sxs-lookup"><span data-stu-id="b41ee-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](/powershell/scripting/learn/ps101/00-introduction).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="b41ee-132">Jak uzyskać moduł PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="b41ee-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="b41ee-133">Wersja systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="b41ee-133">OS Version</span></span>|<span data-ttu-id="b41ee-134">Instrukcje dotyczące instalacji</span><span class="sxs-lookup"><span data-stu-id="b41ee-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="b41ee-135">Mam system Windows 10 lub Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b41ee-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="b41ee-136">Wbudowane w platformę Windows Management Framework (WMF) 5.0 zawartą w systemie operacyjnym</span><span class="sxs-lookup"><span data-stu-id="b41ee-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="b41ee-137">Chcę przeprowadzić uaktualnienie do programu PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="b41ee-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="b41ee-138">Zainstaluj najnowszą wersję platformy WMF</span><span class="sxs-lookup"><span data-stu-id="b41ee-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="b41ee-139">Sprawdzanie wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b41ee-139">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="b41ee-140">Chociaż zachęcamy do jak najszybszego uaktualnienia do najnowszej wersji, różne wersje programu Azure PowerShell są nadal obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="b41ee-140">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="b41ee-141">Aby ustalić zainstalowaną wersję programu Azure PowerShell, uruchom polecenie `Get-InstalledModule Azure` z wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="b41ee-141">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule Azure` from your command line.</span></span>

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
