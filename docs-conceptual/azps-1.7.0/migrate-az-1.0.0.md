---
title: Zmiany powodujące niezgodność dotyczące modułu Az 1.0.0 programu Microsoft Azure PowerShell
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 1 modułu Az programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/18/2019
ms.locfileid: "59364152"
---
# <a name="migration-guide-for-az-100"></a><span data-ttu-id="c5ba0-103">Przewodnik migracji modułu Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="c5ba0-103">Migration Guide for Az 1.0.0</span></span>

<span data-ttu-id="c5ba0-104">W tym dokumencie opisano różnice między wersjami 6.x modułu AzureRM i wersją 1.0.0 modułu Az.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-104">This document describes the changes between the 6.x versions of AzureRM and Az version 1.0.0.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="c5ba0-105">Spis treści</span><span class="sxs-lookup"><span data-stu-id="c5ba0-105">Table of Contents</span></span>
- [<span data-ttu-id="c5ba0-106">Ogólne zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="c5ba0-106">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="c5ba0-107">Zmiany prefiksów poleceń cmdlet w postaci rzeczownika</span><span class="sxs-lookup"><span data-stu-id="c5ba0-107">Cmdlet Noun Prefix Changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="c5ba0-108">Zmiany nazw modułów</span><span class="sxs-lookup"><span data-stu-id="c5ba0-108">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="c5ba0-109">Usunięte moduły</span><span class="sxs-lookup"><span data-stu-id="c5ba0-109">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="c5ba0-110">Windows PowerShell 5.1 i .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="c5ba0-110">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="c5ba0-111">Tymczasowe usunięcie logowania użytkowników przy użyciu obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="c5ba0-111">Temporary removal of User login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="c5ba0-112">Domyślne logowanie za pomocą kodu urządzenia zamiast monitu przeglądarki internetowej</span><span class="sxs-lookup"><span data-stu-id="c5ba0-112">Default Device Code login instead of Web Browser prompt</span></span>](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="c5ba0-113">Zmiany powodujące niezgodność modułów</span><span class="sxs-lookup"><span data-stu-id="c5ba0-113">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="c5ba0-114">Az.ApiManagement (wcześniej AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-114">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="c5ba0-115">Az.Billing (wcześniej AzureRM.Billing, AzureRM.Consumption i AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-115">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="c5ba0-116">Az.CognitiveServices (wcześniej AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-116">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="c5ba0-117">Az.Compute (wcześniej AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-117">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="c5ba0-118">Az.DataFactory (wcześniej AzureRM.DataFactories i AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-118">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="c5ba0-119">Az.DataLakeAnalytics (wcześniej AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-119">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="c5ba0-120">Az.DataLakeStore (wcześniej AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-120">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="c5ba0-121">Az.KeyVault (wcześniej AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-121">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="c5ba0-122">Az.Media (wcześniej AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-122">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="c5ba0-123">Az.Monitor (wcześniej AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-123">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="c5ba0-124">Az.Network (wcześniej AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-124">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="c5ba0-125">Az.OperationalInsights (wcześniej AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-125">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="c5ba0-126">Az.RecoveryServices (wcześniej AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup i AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-126">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="c5ba0-127">Az.Resources (wcześniej AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-127">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="c5ba0-128">Az.ServiceFabric (wcześniej AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-128">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="c5ba0-129">Az.Sql (wcześniej AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-129">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="c5ba0-130">Az.Storage (wcześniej Azure.Storage i AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-130">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="c5ba0-131">Az.Websites (wcześniej AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-131">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="c5ba0-132">Ogólne zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="c5ba0-132">General breaking changes</span></span>
### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="c5ba0-133">Zmiany prefiksów poleceń cmdlet w postaci rzeczownika</span><span class="sxs-lookup"><span data-stu-id="c5ba0-133">Cmdlet Noun Prefix Changes</span></span>
<span data-ttu-id="c5ba0-134">W module AzureRM polecenia cmdlet używały prefiksu w postaci rzeczownika „AzureRM” lub „Azure”.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-134">In AzureRM, cmdlets used either 'AzureRM' or 'Azure' as a noun prefix.</span></span>  <span data-ttu-id="c5ba0-135">Moduł Az upraszcza i normalizuje nazwy poleceń cmdlet, więc wszystkie polecenia cmdlet mają prefiks w postaci rzeczownika „Az”.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-135">Az simplifies and normalizes cmndlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="c5ba0-136">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-136">For example:</span></span>
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="c5ba0-137">Zmieniono na:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-137">Have changed to</span></span>
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="c5ba0-138">Aby ułatwić przejście na te nowe nazwy poleceń cmdlet, moduł Az wprowadza dwa nowe polecenia cmdlet: ```Enable-AzureRmAlias``` i ```Disable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-138">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, ```Enable-AzureRmAlias``` and ```Disable-AzureRmAlias```.</span></span>  <span data-ttu-id="c5ba0-139">Polecenie cmdlet ```Enable-AzureRmAlias``` tworzy aliasy dla starszych nazw poleceń cmdlet w module AzureRM wskazujące nowsze nazwy poleceń cmdlet w module Az.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-139">```Enable-AzureRmAlias``` creates aliases from the older cmdlet names in AzureRM to the newer Az cmdlet names.</span></span>  <span data-ttu-id="c5ba0-140">Polecenie cmdlet umożliwia tworzenie aliasów w bieżącej sesji albo we wszystkich sesjach przez zmianę profilu użytkownika lub maszyny.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-140">The cmdlet allows creating aliases in the current session, or across all sessions by changing your user or machine profile.</span></span> 

<span data-ttu-id="c5ba0-141">Na przykład poniższy skrypt w module AzureRM:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-141">For example, the following script in AzureRM:</span></span>
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="c5ba0-142">Może zostać uruchomiony tylko z niewielkimi zmianami, jeśli zostanie użyte polecenie cmdlet ```Enable-AzureRmAlias```:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-142">Could be run with minimal changes using ```Enable-AzureRmAlias```:</span></span>
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="c5ba0-143">Uruchomienie polecenia cmdlet ```Enable-AzureRmAlias -Scope CurrentUser``` spowoduje włączenie aliasów dla wszystkich otwieranych sesji programu PowerShell, więc po jego wykonaniu nie trzeba w ogóle zmieniać skryptów podobnych do poniższego:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-143">Running ```Enable-AzureRmAlias -Scope CurrentUser``` will enable the aliases for all powershell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="c5ba0-144">Aby uzyskać szczegółowe informacje dotyczące użycia aliasów poleceń cmdlet, wykonaj polecenie ```Get-Help -Online Enable-AzureRmAlias``` w wierszu polecenia programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-144">For complete details on the usage of the alias cmdlets, execute ```Get-Help -Online Enable-AzureRmAlias``` from the powershell prompt.</span></span>

<span data-ttu-id="c5ba0-145">Polecenie ```Disable-AzureRmAlias``` usuwa aliasy poleceń cmdlet modułu AzureRM utworzone przez polecenie ```Enable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-145">```Disable-AzureRmAlias``` removes AzureRM cmdlet aliases created by ```Enable-AzureRmAlias```.</span></span>  <span data-ttu-id="c5ba0-146">Aby uzyskać szczegółowe informacje, wykonaj polecenie ```Get-Help -Online Disable-AzureRmAlias``` w wierszu polecenia programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-146">For complete details, execute ```Get-Help -Online Disable-AzureRmAlias``` from the powershell prompt.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="c5ba0-147">Zmiany nazw modułów</span><span class="sxs-lookup"><span data-stu-id="c5ba0-147">Module Name Changes</span></span>
- <span data-ttu-id="c5ba0-148">Nazwy modułów zostały zmienione z `AzureRM.*` na `Az.*`, z wyjątkiem następujących modułów:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-148">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

<span data-ttu-id="c5ba0-149">Zmiany nazw modułów oznaczają, że każdy skrypt, który używa instrukcji ```#Requires``` lub ```Import-Module``` do ładowania określonych modułów, będzie trzeba zmienić tak, aby używał nowego modułu.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-149">The changes in module names mean that any script that uses ```#Requires``` or ```Import-Module``` to load specific modules will need to be changed to use the new module instead.</span></span>

#### <a name="migrating-requires-statements"></a><span data-ttu-id="c5ba0-150">Migrowanie instrukcji #Requires</span><span class="sxs-lookup"><span data-stu-id="c5ba0-150">Migrating #Requires Statements</span></span>
<span data-ttu-id="c5ba0-151">Skrypty używające instrukcji #Requires do deklarowania zależności od modułów AzureRM należy zaktualizować tak, aby używały nowych nazw modułów</span><span class="sxs-lookup"><span data-stu-id="c5ba0-151">Scripts that use #Requires to declare a dependency on AzureRM modules should be updated to use the new module names</span></span>
```powershell
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="c5ba0-152">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="c5ba0-152">Should be changed to</span></span>
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a><span data-ttu-id="c5ba0-153">Migrowanie instrukcji Import-Module</span><span class="sxs-lookup"><span data-stu-id="c5ba0-153">Migrating Import-Module Statements</span></span>
<span data-ttu-id="c5ba0-154">Skrypty używające instrukcji ```Import-Module``` do ładowania modułów AzureRM należy zaktualizować tak, aby odzwierciedlały nowe nazwy modułów.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-154">Scripts that use ```Import-Module``` to load AzureRM modules will need to be updated to reflect the new module names.</span></span>
```powershell
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="c5ba0-155">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="c5ba0-155">Should be changed to</span></span>
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="c5ba0-156">Migrowanie w pełni kwalifikowanych wywołań poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="c5ba0-156">Migrating Fully-Qualified Cmdlet Invocations</span></span>
<span data-ttu-id="c5ba0-157">Skrypty używające wywołań poleceń cmdlet kwalifikowanych za pomocą modułu, np.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-157">Scripts that use module-qualified cmdlet invocations, like</span></span>
```powershell
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="c5ba0-158">Należy zmienić tak, aby używały nowych nazw modułów i poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="c5ba0-158">Should be changed to use the new module and cmdlet names</span></span>
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="c5ba0-159">Migrowanie zależności manifestu modułów</span><span class="sxs-lookup"><span data-stu-id="c5ba0-159">Migrating Module Manifest Dependencies</span></span>
<span data-ttu-id="c5ba0-160">W przypadku modułów, w których zależności od modułów AzureRM są wyrażane za pomocą pliku manifestu modułów (psd1), należy zaktualizować nazwy modułów w sekcji „RequiredModules”</span><span class="sxs-lookup"><span data-stu-id="c5ba0-160">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their 'RequiredModules' section</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="c5ba0-161">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="c5ba0-161">Should be changed to</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="c5ba0-162">Usunięte moduły</span><span class="sxs-lookup"><span data-stu-id="c5ba0-162">Removed modules</span></span>
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="c5ba0-163">Narzędzia dla tych usług nie są już aktywnie wspierane.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-163">The tooling for these services are no longer actively supported.</span></span>  <span data-ttu-id="c5ba0-164">Zachęcamy klientów do jak najszybszego przechodzenia do alternatywnych usług.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-164">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="c5ba0-165">Windows PowerShell 5.1 i .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="c5ba0-165">Windows PowerShell 5.1 and .NET 4.7.2</span></span>
- <span data-ttu-id="c5ba0-166">W celu korzystania z modułu Az w programie Windows PowerShell 5.1 konieczna jest instalacja programu .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-166">Using Az with Windows PowerShell 5.1 requires the installation of .NET 4.7.2.</span></span> <span data-ttu-id="c5ba0-167">Jednak używanie modułu Az w programie PowerShell Core nie wymaga programu .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-167">However, using Az with PowerShell Core does not require .NET 4.7.2.</span></span> 

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="c5ba0-168">Tymczasowe usunięcie logowania użytkowników przy użyciu obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="c5ba0-168">Temporary removal of User login using PSCredential</span></span>
- <span data-ttu-id="c5ba0-169">Ze względu na zmiany w przepływie uwierzytelniania dla platformy .NET Standard tymczasowo usuwamy możliwość logowania użytkownika za pomocą obiektu PSCredential.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-169">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="c5ba0-170">Ta możliwość zostanie ponownie udostępniona w wersji dla programu Windows PowerShell 5.1 opublikowanej 15.01.2019.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-170">This capability will be re-introduced in the 1/15/2019 release for Windows PowerShell 5.1.</span></span> <span data-ttu-id="c5ba0-171">Ta kwestia została szczegółowo omówiona w ramach [tego problemu.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-171">This is duscussed in detail in [this issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="c5ba0-172">Domyślne logowanie za pomocą kodu urządzenia zamiast monitu przeglądarki internetowej</span><span class="sxs-lookup"><span data-stu-id="c5ba0-172">Default Device Code login instead of Web Browser prompt</span></span>
- <span data-ttu-id="c5ba0-173">Ze względu na zmiany w przepływie uwierzytelniania dla platformy .NET Standard używamy logowania urządzenia jako domyślnego przepływu logowania podczas logowania interakcyjnego.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-173">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="c5ba0-174">Logowanie oparte na przeglądarce internetowej ponownie stanie się domyślne dla programu Windows PowerShell 5.1 w wersji opublikowanej 15.01.2019.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-174">Web browser based login will be re-introduced for Windows PowerShell 5.1 as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="c5ba0-175">Użytkownicy będą wtedy mogli wybrać logowanie urządzenia za pomocą parametru przełącznika.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-175">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="c5ba0-176">Zmiany powodujące niezgodność modułów</span><span class="sxs-lookup"><span data-stu-id="c5ba0-176">Module breaking changes</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="c5ba0-177">Az.ApiManagement (wcześniej AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-177">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>
- <span data-ttu-id="c5ba0-178">Usunięto następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-178">Removing the following cmdlets:</span></span>
  - <span data-ttu-id="c5ba0-179">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5ba0-179">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="c5ba0-180">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c5ba0-180">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="c5ba0-181">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c5ba0-181">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="c5ba0-182">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c5ba0-182">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="c5ba0-183">Zamiast nich do ustawiania tych właściwości użyj polecenia cmdlet **Set-AzApiManagement**</span><span class="sxs-lookup"><span data-stu-id="c5ba0-183">Use **Set-AzApiManagement** cmdlet to set these properites instead</span></span>
- <span data-ttu-id="c5ba0-184">Usunięto następujące właściwości</span><span class="sxs-lookup"><span data-stu-id="c5ba0-184">Following properties were removed</span></span>
  - <span data-ttu-id="c5ba0-185">Usunięto właściwości `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` i `ScmHostnameConfiguration` typu `PsApiManagementHostnameConfiguration` z klasy `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-185">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="c5ba0-186">Zamiast nich używaj właściwości `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` i `ScmCustomHostnameConfiguration` typu `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-186">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="c5ba0-187">Usunięto właściwość `StaticIPs` z klasy PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-187">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="c5ba0-188">Właściwość została podzielona na właściwości `PublicIPAddresses` i `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-188">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="c5ba0-189">Usunięto wymaganą właściwość `Location` z polecenia cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-189">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="c5ba0-190">Az.Billing (wcześniej AzureRM.Billing, AzureRM.Consumption i AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-190">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>
- <span data-ttu-id="c5ba0-191">Parametr `InvoiceName` został usunięty z polecenia cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-191">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="c5ba0-192">W skryptach będzie trzeba używać innych parametrów tożsamości na potrzeby faktury.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-192">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="c5ba0-193">Az.CognitiveServices (wcześniej AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-193">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>
- <span data-ttu-id="c5ba0-194">Usunięto zestaw parametrów `GetSkusWithAccountParamSetName` z polecenia cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-194">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="c5ba0-195">Musisz uzyskiwać jednostki SKU według typu konta i lokalizacji, a nie nazwy grupy zasobów i nazwy konta.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-195">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="c5ba0-196">Az.Compute (wcześniej AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-196">Az.Compute (previously AzureRM.Compute)</span></span>
- <span data-ttu-id="c5ba0-197">Pole `IdentityIds` zostało usunięte z właściwości `Identity` w obiektach `PSVirtualMachine` i `PSVirtualMachineScaleSet`. Skrypty nie powinny już używać wartości tego pola do podejmowania decyzji dotyczących przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-197">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="c5ba0-198">Typ właściwości `InstanceView` obiektu `PSVirtualMachineScaleSetVM` został zmieniony z `VirtualMachineInstanceView` na `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-198">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="c5ba0-199">Właściwości `AutoOSUpgradePolicy` i `AutomaticOSUpgrade` zostały usunięte z właściwości `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-199">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="c5ba0-200">Typ właściwości `Sku` w obiekcie `PSSnapshotUpdate` został zmieniony z `DiskSku` na `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-200">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="c5ba0-201">Zestaw `VmScaleSetVMParameterSet` został usunięty z polecenia cmdlet `Add-AzVMDataDisk`. Nie można już dodawać pojedynczego dysku danych do maszyny wirtualnej w zestawie skalowania.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-201">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="c5ba0-202">Az.DataFactory (wcześniej AzureRM.DataFactories i AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-202">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>
- <span data-ttu-id="c5ba0-203">Parametr `GatewayName` stał się obowiązkowy w poleceniu cmdlet `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-203">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="c5ba0-204">Usunięto polecenie cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-204">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="c5ba0-205">Usunięto parametr `LinkedServiceName` z polecenia cmdlet `Get-AzDataFactoryV2ActivityRun`. Skrypty nie powinny już używać wartości tego pola do podejmowania decyzji dotyczących przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-205">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="c5ba0-206">Az.DataLakeAnalytics (wcześniej AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-206">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>
- <span data-ttu-id="c5ba0-207">Usunięto przestarzałe polecenia cmdlet: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` i `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-207">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="c5ba0-208">Az.DataLakeStore (wcześniej AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-208">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>
- <span data-ttu-id="c5ba0-209">W następujących poleceniach cmdlet typ parametru `Encoding` został zmieniony z `FileSystemCmdletProviderEncoding` na `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-209">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="c5ba0-210">W ramach tej zmiany usunięto wartości kodowania `String` i `Oem`.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-210">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="c5ba0-211">Nadal dostępne są wszystkie pozostałe wcześniejsze wartości kodowania.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-211">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="c5ba0-212">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c5ba0-212">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="c5ba0-213">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="c5ba0-213">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="c5ba0-214">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="c5ba0-214">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="c5ba0-215">Usunięto przestarzały alias właściwości `Tags` z poleceń cmdlet `New-AzDataLakeStoreAccount` i `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-215">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="c5ba0-216">Skrypty używające kodu</span><span class="sxs-lookup"><span data-stu-id="c5ba0-216">Scripts using</span></span>
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="c5ba0-217">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="c5ba0-217">Should be changed to</span></span>
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="c5ba0-218">Usunięto przestarzałe właściwości ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier``` i ```FirewallAllowAzureIps``` z obiektu ```PSDataLakeStoreAccountBasic```.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-218">Removed deprecated properties ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` from ```PSDataLakeStoreAccountBasic``` object.</span></span>  <span data-ttu-id="c5ba0-219">Żaden skrypt, który używa obiektu ```PSDatalakeStoreAccount``` zwróconego przez polecenie ```Get-AzDataLakeStoreAccount```, nie powinien odwoływać się do tych właściwości.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-219">Any script that uses the ```PSDatalakeStoreAccount``` returned from ```Get-AzDataLakeStoreAccount``` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="c5ba0-220">Az.KeyVault (wcześniej AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-220">Az.KeyVault (previously AzureRM.KeyVault)</span></span>
- <span data-ttu-id="c5ba0-221">Właściwość `PurgeDisabled` została usunięta z obiektów `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` i `PSKeyVaultSecretAttributes`. Skrypty nie powinny już odwoływać się do właściwości ```PurgeDisabled``` w celu podejmowania decyzji dotyczących przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-221">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts shoudl no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="c5ba0-222">Az.Media (wcześniej AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-222">Az.Media (previously AzureRM.Media)</span></span>
- <span data-ttu-id="c5ba0-223">Usunięto przestarzały alias właściwości `Tags` z polecenia cmdlet `New-AzMediaService`. Skrypty używające kodu</span><span class="sxs-lookup"><span data-stu-id="c5ba0-223">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="c5ba0-224">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="c5ba0-224">Should be changed to</span></span>
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="c5ba0-225">Az.Monitor (wcześniej AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-225">Az.Monitor (previously AzureRM.Insights)</span></span>
- <span data-ttu-id="c5ba0-226">Z polecenia cmdlet `Set-AzDiagnosticSetting` usunięto parametry o nazwach w liczbie mnogiej `Categories` i `Timegrains`, aby zastąpić je nazwami parametrów w liczbie pojedynczej. Skrypty używające kodu</span><span class="sxs-lookup"><span data-stu-id="c5ba0-226">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="c5ba0-227">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="c5ba0-227">Should be changed to</span></span>
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="c5ba0-228">Az.Network (wcześniej AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-228">Az.Network (previously AzureRM.Network)</span></span>
- <span data-ttu-id="c5ba0-229">Usunięto przestarzały parametr `ResourceId` z polecenia cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-229">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="c5ba0-230">Usunięto przestarzałą właściwość `EnableVmProtection` z obiektu `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-230">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="c5ba0-231">Usunięto przestarzałe polecenie cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-231">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="c5ba0-232">Skrypty nie powinny już podejmować decyzji dotyczących przetwarzania na podstawie wartości tych pól.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-232">Scripts shoudl no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="c5ba0-233">Az.OperationalInsights (wcześniej AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-233">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>
- <span data-ttu-id="c5ba0-234">Usunięto domyślny zestaw parametrów dla polecenia `Get-AzOperationalInsightsDataSource`, a zestaw `ByWorkspaceNameByKind` stał się domyślnym zestawem parametrów</span><span class="sxs-lookup"><span data-stu-id="c5ba0-234">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="c5ba0-235">Skrypty zwracające listę źródeł danych przy użyciu polecenia</span><span class="sxs-lookup"><span data-stu-id="c5ba0-235">Scripts that listed data sources using</span></span>
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="c5ba0-236">Należy zmienić tak, aby określały rodzaj</span><span class="sxs-lookup"><span data-stu-id="c5ba0-236">Should be changed to specify a Kind</span></span>
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c5ba0-237">Az.RecoveryServices (wcześniej AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup i AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-237">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>
- <span data-ttu-id="c5ba0-238">Usunięto parametr `Encryption` z polecenia cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-238">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="c5ba0-239">Parametr `TargetStorageAccountName` jest teraz obowiązkowy na potrzeby przywracania dysku zarządzanego w poleceniu cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-239">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="c5ba0-240">Usunięto parametry `StorageAccountName` i `StorageAccountResourceGroupName` w poleceniu cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-240">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="c5ba0-241">Usunięto parametr `Name` w poleceniu cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-241">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="c5ba0-242">Az.Resources (wcześniej AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-242">Az.Resources (previously AzureRM.Resources)</span></span>
- <span data-ttu-id="c5ba0-243">Usunięto parametr `Sku` z polecenia cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-243">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="c5ba0-244">Usunięto parametr `Password` z poleceń cmdlet `New-AzADServicePrincipal` i `New-AzADSpCredential`. Hasła są generowane automatycznie, a skrypty, które podawały hasło:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-244">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="c5ba0-245">Należy zmienić tak, aby uzyskiwały hasło z danych wyjściowych:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-245">Should be changed to retriedve the password from the output:</span></span>
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="c5ba0-246">Az.ServiceFabric (wcześniej AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-246">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>
- <span data-ttu-id="c5ba0-247">Zmieniono następujące zwracane typy poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-247">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="c5ba0-248">Właściwość `SerivceTypeHealthPolicies` typu `ApplicationHealthPolicy` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-248">The property `SerivceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="c5ba0-249">Właściwość `ApplicationHealthPolicies` typu `ClusterUpgradeDeltaHealthPolicy` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-249">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="c5ba0-250">Właściwość `OverrideUserUpgradePolicy` typu `ClusterUpgradePolicy` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-250">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="c5ba0-251">Te zmiany mają wpływ na następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-251">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="c5ba0-252">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c5ba0-252">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="c5ba0-253">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c5ba0-253">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="c5ba0-254">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c5ba0-254">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="c5ba0-255">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="c5ba0-255">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="c5ba0-256">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c5ba0-256">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="c5ba0-257">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c5ba0-257">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="c5ba0-258">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c5ba0-258">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="c5ba0-259">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c5ba0-259">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="c5ba0-260">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="c5ba0-260">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="c5ba0-261">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="c5ba0-261">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="c5ba0-262">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="c5ba0-262">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="c5ba0-263">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="c5ba0-263">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="c5ba0-264">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="c5ba0-264">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="c5ba0-265">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="c5ba0-265">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="c5ba0-266">Az.Sql (wcześniej AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-266">Az.Sql (previously AzureRM.Sql)</span></span>
- <span data-ttu-id="c5ba0-267">Usunięto parametry `State` i `ResourceId` z polecenia cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-267">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="c5ba0-268">Usunięto przestarzałe polecenia cmdlet: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` i `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-268">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="c5ba0-269">Usunięto przestarzały parametr `Current` z polecenia cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-269">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="c5ba0-270">Usunięto przestarzały parametr `DatabaseName` z polecenia cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-270">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="c5ba0-271">Usunięto przestarzały parametr `PrivilegedLogin` z polecenia cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-271">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="c5ba0-272">Az.Storage (wcześniej Azure.Storage i AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-272">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>
- <span data-ttu-id="c5ba0-273">Aby obsługiwać tworzenie kontekstu magazynu OAuth za pomocą tylko nazwy konta magazynu, domyślny zestaw parametrów został zmieniony na `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-273">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="c5ba0-274">Przykład: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-274">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="c5ba0-275">Parametr `Location` stał się obowiązkowy w poleceniu cmdlet `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-275">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="c5ba0-276">Metody interfejsu API magazynu używają teraz wzorca asynchronicznego opartego na zadaniach zamiast synchronicznych wywołań interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c5ba0-276">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span>
#### <a name="1-blob-snapshot"></a><span data-ttu-id="c5ba0-277">1. Migawka obiektu blob</span><span class="sxs-lookup"><span data-stu-id="c5ba0-277">1. Blob Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="c5ba0-278">Przed:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-278">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a><span data-ttu-id="c5ba0-279">Po:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-279">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a><span data-ttu-id="c5ba0-280">2. Udostępnianie migawki</span><span class="sxs-lookup"><span data-stu-id="c5ba0-280">2. Share Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="c5ba0-281">Przed:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-281">Before:</span></span>
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a><span data-ttu-id="c5ba0-282">Po:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-282">After:</span></span>
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a><span data-ttu-id="c5ba0-283">3. Cofanie usuwania nietrwale usuniętego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="c5ba0-283">3. Undelete a soft delete blob</span></span>
##### <a name="before"></a><span data-ttu-id="c5ba0-284">Przed:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-284">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a><span data-ttu-id="c5ba0-285">Po:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-285">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a><span data-ttu-id="c5ba0-286">4. Ustawianie warstwy obiektu blob</span><span class="sxs-lookup"><span data-stu-id="c5ba0-286">4. Set Blob Tier</span></span>
##### <a name="before"></a><span data-ttu-id="c5ba0-287">Przed:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-287">Before:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a><span data-ttu-id="c5ba0-288">Po:</span><span class="sxs-lookup"><span data-stu-id="c5ba0-288">After:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="c5ba0-289">Az.Websites (wcześniej AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="c5ba0-289">Az.Websites (previously AzureRM.Websites)</span></span>
- <span data-ttu-id="c5ba0-290">Usunięto przestarzałe właściwości z obiektów `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` i `PSSite`</span><span class="sxs-lookup"><span data-stu-id="c5ba0-290">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>