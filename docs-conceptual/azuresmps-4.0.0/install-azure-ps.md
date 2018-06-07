---
title: Instalowanie i konfigurowanie modułu zarządzania usługami programu Azure PowerShell | Microsoft Docs
description: Jak zainstalować i skonfigurować program Azure PowerShell do pierwszego użycia.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 52e7239e375032dbf8b48c2e7e54c5239fe7943a
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821466"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="65e1e-103">Instalowanie modułu zarządzania usługami programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="65e1e-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="65e1e-104">Instalowanie programu Azure PowerShell z [Galerii programu PowerShell](https://www.powershellgallery.com/) jest preferowaną metodą instalacji.</span><span class="sxs-lookup"><span data-stu-id="65e1e-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="65e1e-105">Krok 1. Zainstaluj moduł PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="65e1e-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="65e1e-106">Instalowanie elementów z Galerii programu PowerShell wymaga modułu PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="65e1e-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="65e1e-107">Upewnij się, że masz odpowiednią wersję modułu PowerShellGet oraz spełnione inne wymagania systemowe.</span><span class="sxs-lookup"><span data-stu-id="65e1e-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="65e1e-108">Uruchom następujące polecenie, aby sprawdzić, czy w Twoim systemie został zainstalowany moduł PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="65e1e-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="65e1e-109">Powinny zostać wyświetlone dane wyjściowe podobne do poniższych:</span><span class="sxs-lookup"><span data-stu-id="65e1e-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="65e1e-110">Jeśli nie masz zainstalowanego modułu PowerShellGet, zobacz sekcję [Jak uzyskać moduł PowerShellGet](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="65e1e-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="65e1e-111">Krok 2. Zainstaluj program Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="65e1e-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="65e1e-112">Uruchom następujące polecenie z poziomu konsoli programu Windows PowerShell jako administrator:</span><span class="sxs-lookup"><span data-stu-id="65e1e-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="65e1e-113">Moduł Azure to zbiorczy moduł poleceń cmdlet usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="65e1e-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="65e1e-114">Po zainstalowaniu modułu AzureRM każdy moduł platformy Azure, który nie został wcześniej zainstalowany, zostanie pobrany i zainstalowany z Galerii programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="65e1e-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="65e1e-115">Moduł zarządzania usługami platformy Azure udostępnia zależności z modułami usługi Azure PowerShell Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="65e1e-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="65e1e-116">Jeśli masz zainstalowane moduły usługi Azure PowerShell Resource Manager, musisz dodać parametr `-AllowClobber` do polecenia instalacji.</span><span class="sxs-lookup"><span data-stu-id="65e1e-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="65e1e-117">Umożliwi to aktualizowanie istniejących udostępnionych zależności.</span><span class="sxs-lookup"><span data-stu-id="65e1e-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="65e1e-118">Bez tego parametru nie można zainstalować modułu.</span><span class="sxs-lookup"><span data-stu-id="65e1e-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="65e1e-119">Po zainstalowaniu tego modułu należy zaimportować moduł za pomocą następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="65e1e-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="65e1e-120">Aby korzystać z poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="65e1e-120">To use the cmdlets</span></span>

<span data-ttu-id="65e1e-121">Aby rozpocząć pracę z poleceniami cmdlet zarządzania usługami platformy Azure, najpierw zaloguj się do konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="65e1e-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="65e1e-122">Aby zalogować się do konta, uruchom następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="65e1e-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="65e1e-123">Gdy zalogujesz się do platformy Azure, program Azure PowerShell utworzy kontekst dla danej sesji.</span><span class="sxs-lookup"><span data-stu-id="65e1e-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="65e1e-124">Ten kontekst zawiera środowisko, konto, dzierżawę i subskrypcję programu Azure PowerShell, które będą używane dla wszystkich poleceń cmdlet w tej sesji.</span><span class="sxs-lookup"><span data-stu-id="65e1e-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="65e1e-125">Teraz możesz używać poniższych modułów.</span><span class="sxs-lookup"><span data-stu-id="65e1e-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="65e1e-126">Polecenia cmdlet zarządzania usługami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="65e1e-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="65e1e-127">Moduły programu Azure PowerShell są często aktualizowane.</span><span class="sxs-lookup"><span data-stu-id="65e1e-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="65e1e-128">Jeśli zauważysz, że pomoc online do polecenia cmdlet zawiera polecenia cmdlet lub parametry, których nie ma w module, pobierz i zainstaluj najnowszą wersję modułu.</span><span class="sxs-lookup"><span data-stu-id="65e1e-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="65e1e-129">Aby znaleźć wersji modułu, wpisz: `(Get-Module Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="65e1e-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="65e1e-130">Przykładowe skrypty, które mogą pomóc zautomatyzować niektóre typowe zadania na platformie Azure, można znaleźć w temacie [Centrum skryptów Microsoft Azure](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="65e1e-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="65e1e-131">Ogólne informacje na temat instalowania, używania i dostosowywania środowiska programu Windows PowerShell oraz powiązanych szkoleń można znaleźć w temacie [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210) (Obsługa skryptów w programie Windows PowerShell).</span><span class="sxs-lookup"><span data-stu-id="65e1e-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="65e1e-132">Jak uzyskać moduł PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="65e1e-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="65e1e-133">Wersja systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="65e1e-133">OS Version</span></span>|<span data-ttu-id="65e1e-134">Instrukcje dotyczące instalacji</span><span class="sxs-lookup"><span data-stu-id="65e1e-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="65e1e-135">Mam system Windows 10 lub Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="65e1e-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="65e1e-136">Wbudowane w platformę Windows Management Framework (WMF) 5.0 zawartą w systemie operacyjnym</span><span class="sxs-lookup"><span data-stu-id="65e1e-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="65e1e-137">Chcę przeprowadzić uaktualnienie do programu PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="65e1e-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="65e1e-138">Zainstaluj najnowszą wersję platformy WMF</span><span class="sxs-lookup"><span data-stu-id="65e1e-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="65e1e-139">Używam wersji systemu Windows mającej program PowerShell 3 lub 4</span><span class="sxs-lookup"><span data-stu-id="65e1e-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="65e1e-140">Pobierz moduły PackageManagement</span><span class="sxs-lookup"><span data-stu-id="65e1e-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="65e1e-141">Sprawdzanie wersji programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="65e1e-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="65e1e-142">Chociaż zachęcamy do jak najszybszego uaktualnienia do najnowszej wersji, różne wersje programu Azure PowerShell są nadal obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="65e1e-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="65e1e-143">Aby ustalić zainstalowaną wersję programu Azure PowerShell, uruchom polecenie `Get-Module AzureRM` z wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="65e1e-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
