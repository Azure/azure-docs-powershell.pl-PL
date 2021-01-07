---
title: Wszystkie różnice między modułem AzureRM i modułem Az 1.0.0 programu Azure PowerShell
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 1 modułu Az programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 3ab12307f786c12422338835926802793a33713e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893973"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="aea72-103">Zmiany powodujące niezgodność w module Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="aea72-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="aea72-104">Ten dokument zawiera szczegółowe informacje na temat różnic między modułem AzureRM w wersji 6.x i nowym modułem Az w wersji 1.x i nowszych.</span><span class="sxs-lookup"><span data-stu-id="aea72-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="aea72-105">Spis treści pomoże przeprowadzić Cię przez pełną ścieżkę migracji, w tym zmiany specyficzne dla modułu, które mogą mieć wpływ na skrypty.</span><span class="sxs-lookup"><span data-stu-id="aea72-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="aea72-106">Aby uzyskać ogólne porady dotyczące rozpoczynania pracy z migracją z modułu AzureRM do modułu Az, zobacz [Rozpoczynanie migracji z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="aea72-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aea72-107">Także między wersją 1.0.0 i 2.0.0 modułu wprowadzono zmiany powodujące niezgodność.</span><span class="sxs-lookup"><span data-stu-id="aea72-107">There have been breaking changes between Az 1.0.0 and Az 2.0.0 as well.</span></span> <span data-ttu-id="aea72-108">Po wykonaniu instrukcji tego przewodnika w celu aktualizacji z modułu AzureRM do modułu Az, zobacz [Zmiany powodujące niezgodność w module Az 2.0.0](migrate-az-2.0.0.md), aby dowiedzieć się, czy musisz wprowadzić dodatkowe zmiany.</span><span class="sxs-lookup"><span data-stu-id="aea72-108">After following this guide for updating from AzureRM to Az, see the [Az 2.0.0 breaking changes](migrate-az-2.0.0.md) to find out if you need to make additional changes.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="aea72-109">Spis treści</span><span class="sxs-lookup"><span data-stu-id="aea72-109">Table of Contents</span></span>

- [<span data-ttu-id="aea72-110">Ogólne zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="aea72-110">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="aea72-111">Zmiany prefiksów poleceń cmdlet w postaci rzeczownika</span><span class="sxs-lookup"><span data-stu-id="aea72-111">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="aea72-112">Zmiany nazw modułów</span><span class="sxs-lookup"><span data-stu-id="aea72-112">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="aea72-113">Usunięte moduły</span><span class="sxs-lookup"><span data-stu-id="aea72-113">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="aea72-114">Windows PowerShell 5.1 i .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="aea72-114">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="aea72-115">Tymczasowe usunięcie logowania użytkowników przy użyciu obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="aea72-115">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="aea72-116">Domyślne logowanie za pomocą kodu urządzenia zamiast monitu przeglądarki internetowej</span><span class="sxs-lookup"><span data-stu-id="aea72-116">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="aea72-117">Zmiany powodujące niezgodność modułów</span><span class="sxs-lookup"><span data-stu-id="aea72-117">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="aea72-118">Az.ApiManagement (wcześniej AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="aea72-118">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="aea72-119">Az.Billing (wcześniej AzureRM.Billing, AzureRM.Consumption i AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="aea72-119">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="aea72-120">Az.CognitiveServices (wcześniej AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="aea72-120">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="aea72-121">Az.Compute (wcześniej AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="aea72-121">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="aea72-122">Az.DataFactory (wcześniej AzureRM.DataFactories i AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="aea72-122">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="aea72-123">Az.DataLakeAnalytics (wcześniej AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="aea72-123">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="aea72-124">Az.DataLakeStore (wcześniej AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="aea72-124">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="aea72-125">Az.KeyVault (wcześniej AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="aea72-125">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="aea72-126">Az.Media (wcześniej AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="aea72-126">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="aea72-127">Az.Monitor (wcześniej AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="aea72-127">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="aea72-128">Az.Network (wcześniej AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="aea72-128">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="aea72-129">Az.OperationalInsights (wcześniej AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="aea72-129">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="aea72-130">Az.RecoveryServices (wcześniej AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup i AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="aea72-130">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="aea72-131">Az.Resources (wcześniej AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="aea72-131">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="aea72-132">Az.ServiceFabric (wcześniej AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="aea72-132">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="aea72-133">Az.Sql (wcześniej AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="aea72-133">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="aea72-134">Az.Storage (wcześniej Azure.Storage i AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="aea72-134">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="aea72-135">Az.Websites (wcześniej AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="aea72-135">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="aea72-136">Ogólne zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="aea72-136">General breaking changes</span></span>

<span data-ttu-id="aea72-137">W tej sekcji przedstawiono ogólne zmiany powodujące niezgodność wprowadzone w ramach przeprojektowania modułu Az.</span><span class="sxs-lookup"><span data-stu-id="aea72-137">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="aea72-138">Zmiany prefiksów poleceń cmdlet w postaci rzeczownika</span><span class="sxs-lookup"><span data-stu-id="aea72-138">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="aea72-139">W module AzureRM polecenia cmdlet używały ciągu `AzureRM` lub `Azure` jako prefiksu w postaci rzeczownika.</span><span class="sxs-lookup"><span data-stu-id="aea72-139">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="aea72-140">Moduł Az upraszcza i normalizuje nazwy poleceń cmdlet, więc wszystkie polecenia cmdlet mają prefiks w postaci rzeczownika „Az”.</span><span class="sxs-lookup"><span data-stu-id="aea72-140">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="aea72-141">Przykład:</span><span class="sxs-lookup"><span data-stu-id="aea72-141">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="aea72-142">Zmieniono na:</span><span class="sxs-lookup"><span data-stu-id="aea72-142">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="aea72-143">Aby ułatwić przejście na te nowe nazwy poleceń cmdlet, moduł Az wprowadza dwa nowe polecenia cmdlet, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) i [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="aea72-143">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="aea72-144">Polecenie cmdlet `Enable-AzureRmAlias` tworzy aliasy dla starszych nazw poleceń cmdlet w module AzureRM mapowane na nowsze nazwy poleceń cmdlet w module Az.</span><span class="sxs-lookup"><span data-stu-id="aea72-144">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="aea72-145">Argument `-Scope` polecenia cmdlet `Enable-AzureRmAlias` pozwala wybrać, gdzie aliasy zostaną włączone.</span><span class="sxs-lookup"><span data-stu-id="aea72-145">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="aea72-146">Na przykład poniższy skrypt w module AzureRM:</span><span class="sxs-lookup"><span data-stu-id="aea72-146">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="aea72-147">Może zostać uruchomiony tylko z niewielkimi zmianami, jeśli zostanie użyte polecenie cmdlet `Enable-AzureRmAlias`:</span><span class="sxs-lookup"><span data-stu-id="aea72-147">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="aea72-148">Uruchomienie polecenia cmdlet `Enable-AzureRmAlias -Scope CurrentUser` spowoduje włączenie aliasów dla wszystkich otwieranych sesji programu PowerShell, więc po jego wykonaniu nie trzeba w ogóle zmieniać skryptów podobnych do poniższego:</span><span class="sxs-lookup"><span data-stu-id="aea72-148">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="aea72-149">Aby uzyskać szczegółowe informacje dotyczące użycia aliasów poleceń cmdlet, zobacz [Dokumentacja polecenia cmdlet Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="aea72-149">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="aea72-150">Gdy wszystko będzie gotowe do wyłączenia aliasów, możesz usunąć utworzone aliasy za pomocą polecenia cmdlet `Disable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="aea72-150">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="aea72-151">Aby uzyskać szczegółowe informacje, zobacz [Dokumentacja polecenia cmdlet Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="aea72-151">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aea72-152">Podczas wyłączania aliasów upewnij się, że zostaną one wyłączone dla _wszystkich_ zakresów, w których je włączono.</span><span class="sxs-lookup"><span data-stu-id="aea72-152">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="aea72-153">Zmiany nazw modułów</span><span class="sxs-lookup"><span data-stu-id="aea72-153">Module Name Changes</span></span>

<span data-ttu-id="aea72-154">Nazwy modułów zostały zmienione z `AzureRM.*` na `Az.*`, z wyjątkiem następujących modułów:</span><span class="sxs-lookup"><span data-stu-id="aea72-154">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="aea72-155">Moduł AzureRM</span><span class="sxs-lookup"><span data-stu-id="aea72-155">AzureRM module</span></span> | <span data-ttu-id="aea72-156">Moduł Az</span><span class="sxs-lookup"><span data-stu-id="aea72-156">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="aea72-157">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="aea72-157">Azure.Storage</span></span> | <span data-ttu-id="aea72-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="aea72-158">Az.Storage</span></span> |
| <span data-ttu-id="aea72-159">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aea72-159">Azure.AnalysisServices</span></span> | <span data-ttu-id="aea72-160">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="aea72-160">Az.AnalysisServices</span></span> |
| <span data-ttu-id="aea72-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="aea72-161">AzureRM.Profile</span></span> | <span data-ttu-id="aea72-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aea72-162">Az.Accounts</span></span> |
| <span data-ttu-id="aea72-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="aea72-163">AzureRM.Insights</span></span> | <span data-ttu-id="aea72-164">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="aea72-164">Az.Monitor</span></span> |
| <span data-ttu-id="aea72-165">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="aea72-165">AzureRM.DataFactories</span></span> | <span data-ttu-id="aea72-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aea72-166">Az.DataFactory</span></span> |
| <span data-ttu-id="aea72-167">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="aea72-167">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="aea72-168">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="aea72-168">Az.DataFactory</span></span> |
| <span data-ttu-id="aea72-169">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="aea72-169">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="aea72-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aea72-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="aea72-171">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="aea72-171">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="aea72-172">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="aea72-172">Az.RecoveryServices</span></span> |
| <span data-ttu-id="aea72-173">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="aea72-173">AzureRM.Tags</span></span> | <span data-ttu-id="aea72-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="aea72-174">Az.Resources</span></span> |
| <span data-ttu-id="aea72-175">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="aea72-175">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="aea72-176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="aea72-176">Az.MachineLearning</span></span> |
| <span data-ttu-id="aea72-177">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="aea72-177">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="aea72-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="aea72-178">Az.Billing</span></span> |
| <span data-ttu-id="aea72-179">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="aea72-179">AzureRM.Consumption</span></span> | <span data-ttu-id="aea72-180">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="aea72-180">Az.Billing</span></span> |

<span data-ttu-id="aea72-181">Zmiany nazw modułów oznaczają, że każdy skrypt, który używa instrukcji `#Requires` lub `Import-Module` do ładowania określonych modułów, będzie trzeba zmienić tak, aby używał nowego modułu.</span><span class="sxs-lookup"><span data-stu-id="aea72-181">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="aea72-182">Jeśli dla danego modułu sufiks polecenia cmdlet pozostał taki sam, oznacza to, że chociaż nazwa modułu się zmieniła, to sufiks wskazujący obszar operacji _nie_ uległ zmianie.</span><span class="sxs-lookup"><span data-stu-id="aea72-182">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="aea72-183">Migrowanie instrukcji #Requires i Import-Module</span><span class="sxs-lookup"><span data-stu-id="aea72-183">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="aea72-184">Skrypty używające instrukcji `#Requires` lub `Import-Module` do deklarowania zależności od modułów AzureRM należy zaktualizować tak, aby używały nowych nazw modułów.</span><span class="sxs-lookup"><span data-stu-id="aea72-184">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="aea72-185">Przykład:</span><span class="sxs-lookup"><span data-stu-id="aea72-185">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="aea72-186">Należy zmienić na:</span><span class="sxs-lookup"><span data-stu-id="aea72-186">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="aea72-187">Instrukcję `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="aea72-187">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="aea72-188">Należy zmienić na:</span><span class="sxs-lookup"><span data-stu-id="aea72-188">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="aea72-189">Migrowanie w pełni kwalifikowanych wywołań poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="aea72-189">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="aea72-190">Skrypty używające wywołań poleceń cmdlet kwalifikowanych za pomocą modułu, takie jak:</span><span class="sxs-lookup"><span data-stu-id="aea72-190">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="aea72-191">Należy zmienić tak, aby używały nowych nazw modułów i poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="aea72-191">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="aea72-192">Migrowanie zależności manifestu modułów</span><span class="sxs-lookup"><span data-stu-id="aea72-192">Migrating module manifest dependencies</span></span>

<span data-ttu-id="aea72-193">W przypadku modułów, w których zależności od modułów AzureRM są wyrażane za pomocą pliku manifestu modułów (psd1), należy zaktualizować nazwy modułów w sekcji `RequiredModules`:</span><span class="sxs-lookup"><span data-stu-id="aea72-193">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="aea72-194">Należy zmienić na:</span><span class="sxs-lookup"><span data-stu-id="aea72-194">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="aea72-195">Usunięte moduły</span><span class="sxs-lookup"><span data-stu-id="aea72-195">Removed modules</span></span>

<span data-ttu-id="aea72-196">Następujące moduły zostały usunięte:</span><span class="sxs-lookup"><span data-stu-id="aea72-196">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="aea72-197">Narzędzia dla tych usług nie są już aktywnie wspierane.</span><span class="sxs-lookup"><span data-stu-id="aea72-197">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="aea72-198">Zachęcamy klientów do jak najszybszego przechodzenia do alternatywnych usług.</span><span class="sxs-lookup"><span data-stu-id="aea72-198">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="aea72-199">Windows PowerShell 5.1 i .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="aea72-199">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="aea72-200">Korzystanie z modułu Az w programie PowerShell 5.1 dla systemu Windows wymaga zainstalowania programu .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="aea72-200">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="aea72-201">Jeśli używasz programu PowerShell Core w wersji 6.x lub nowszej, program .NET Framework nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="aea72-201">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="aea72-202">Tymczasowe usunięcie logowania użytkowników przy użyciu obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="aea72-202">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="aea72-203">Ze względu na zmiany w przepływie uwierzytelniania dla platformy .NET Standard tymczasowo usuwamy możliwość logowania użytkownika za pomocą obiektu PSCredential.</span><span class="sxs-lookup"><span data-stu-id="aea72-203">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="aea72-204">Ta możliwość zostanie ponownie udostępniona w wersji dla programu PowerShell 5.1 dla systemu Windows opublikowanej 15.01.2019.</span><span class="sxs-lookup"><span data-stu-id="aea72-204">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="aea72-205">Ta kwestia została szczegółowo omówiona w ramach [tego problemu w usłudze GitHub.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="aea72-205">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="aea72-206">Domyślne logowanie za pomocą kodu urządzenia zamiast monitu przeglądarki internetowej</span><span class="sxs-lookup"><span data-stu-id="aea72-206">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="aea72-207">Ze względu na zmiany w przepływie uwierzytelniania dla platformy .NET Standard używamy logowania urządzenia jako domyślnego przepływu logowania podczas logowania interakcyjnego.</span><span class="sxs-lookup"><span data-stu-id="aea72-207">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="aea72-208">Logowanie oparte na przeglądarce internetowej ponownie stanie się domyślne dla programu PowerShell 5.1 dla systemu Windows w wersji opublikowanej 15.01.2019.</span><span class="sxs-lookup"><span data-stu-id="aea72-208">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="aea72-209">Użytkownicy będą wtedy mogli wybrać logowanie urządzenia za pomocą parametru przełącznika.</span><span class="sxs-lookup"><span data-stu-id="aea72-209">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="aea72-210">Zmiany powodujące niezgodność modułów</span><span class="sxs-lookup"><span data-stu-id="aea72-210">Module breaking changes</span></span>

<span data-ttu-id="aea72-211">W tej sekcji szczegółowo opisano konkretne zmiany powodujące niezgodność w poszczególnych modułach i poleceniach cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aea72-211">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="aea72-212">Az.ApiManagement (wcześniej AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="aea72-212">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="aea72-213">Usunięto następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="aea72-213">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="aea72-214">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="aea72-214">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="aea72-215">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="aea72-215">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="aea72-216">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="aea72-216">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="aea72-217">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="aea72-217">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="aea72-218">Zamiast nich do ustawiania tych właściwości użyj polecenia cmdlet **Set-AzApiManagement**</span><span class="sxs-lookup"><span data-stu-id="aea72-218">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="aea72-219">Usunięto następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="aea72-219">Removed the following properties:</span></span>
  - <span data-ttu-id="aea72-220">Usunięto właściwości `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` i `ScmHostnameConfiguration` typu `PsApiManagementHostnameConfiguration` z klasy `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="aea72-220">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="aea72-221">Zamiast nich używaj właściwości `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` i `ScmCustomHostnameConfiguration` typu `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="aea72-221">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="aea72-222">Usunięto właściwość `StaticIPs` z klasy PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="aea72-222">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="aea72-223">Właściwość została podzielona na właściwości `PublicIPAddresses` i `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="aea72-223">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="aea72-224">Usunięto wymaganą właściwość `Location` z polecenia cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="aea72-224">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="aea72-225">Az.Billing (wcześniej AzureRM.Billing, AzureRM.Consumption i AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="aea72-225">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="aea72-226">Parametr `InvoiceName` został usunięty z polecenia cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="aea72-226">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="aea72-227">W skryptach będzie trzeba używać innych parametrów tożsamości na potrzeby faktury.</span><span class="sxs-lookup"><span data-stu-id="aea72-227">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="aea72-228">Az.CognitiveServices (wcześniej AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="aea72-228">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="aea72-229">Usunięto zestaw parametrów `GetSkusWithAccountParamSetName` z polecenia cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="aea72-229">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="aea72-230">Musisz uzyskiwać jednostki SKU według typu konta i lokalizacji, a nie nazwy grupy zasobów i nazwy konta.</span><span class="sxs-lookup"><span data-stu-id="aea72-230">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="aea72-231">Az.Compute (wcześniej AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="aea72-231">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="aea72-232">Pole `IdentityIds` zostało usunięte z właściwości `Identity` w obiektach `PSVirtualMachine` i `PSVirtualMachineScaleSet`. Skrypty nie powinny już używać wartości tego pola do podejmowania decyzji dotyczących przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="aea72-232">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="aea72-233">Typ właściwości `InstanceView` obiektu `PSVirtualMachineScaleSetVM` został zmieniony z `VirtualMachineInstanceView` na `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="aea72-233">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="aea72-234">Właściwości `AutoOSUpgradePolicy` i `AutomaticOSUpgrade` zostały usunięte z właściwości `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="aea72-234">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="aea72-235">Typ właściwości `Sku` w obiekcie `PSSnapshotUpdate` został zmieniony z `DiskSku` na `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="aea72-235">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="aea72-236">Zestaw `VmScaleSetVMParameterSet` został usunięty z polecenia cmdlet `Add-AzVMDataDisk`. Nie można już dodawać pojedynczego dysku danych do maszyny wirtualnej w zestawie skalowania.</span><span class="sxs-lookup"><span data-stu-id="aea72-236">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="aea72-237">Az.DataFactory (wcześniej AzureRM.DataFactories i AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="aea72-237">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="aea72-238">Parametr `GatewayName` stał się obowiązkowy w poleceniu cmdlet `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="aea72-238">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="aea72-239">Usunięto polecenie cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="aea72-239">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="aea72-240">Usunięto parametr `LinkedServiceName` z polecenia cmdlet `Get-AzDataFactoryV2ActivityRun`. Skrypty nie powinny już używać wartości tego pola do podejmowania decyzji dotyczących przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="aea72-240">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="aea72-241">Az.DataLakeAnalytics (wcześniej AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="aea72-241">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="aea72-242">Usunięto przestarzałe polecenia cmdlet: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` i `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="aea72-242">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="aea72-243">Az.DataLakeStore (wcześniej AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="aea72-243">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="aea72-244">W następujących poleceniach cmdlet typ parametru `Encoding` został zmieniony z `FileSystemCmdletProviderEncoding` na `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="aea72-244">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="aea72-245">W ramach tej zmiany usunięto wartości kodowania `String` i `Oem`.</span><span class="sxs-lookup"><span data-stu-id="aea72-245">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="aea72-246">Nadal dostępne są wszystkie pozostałe wcześniejsze wartości kodowania.</span><span class="sxs-lookup"><span data-stu-id="aea72-246">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="aea72-247">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aea72-247">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="aea72-248">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="aea72-248">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="aea72-249">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="aea72-249">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="aea72-250">Usunięto przestarzały alias właściwości `Tags` z poleceń cmdlet `New-AzDataLakeStoreAccount` i `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="aea72-250">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="aea72-251">Skrypty używające kodu</span><span class="sxs-lookup"><span data-stu-id="aea72-251">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="aea72-252">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="aea72-252">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="aea72-253">Usunięto przestarzałe właściwości `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` i `FirewallAllowAzureIps` z obiektu `PSDataLakeStoreAccountBasic`.</span><span class="sxs-lookup"><span data-stu-id="aea72-253">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="aea72-254">Żaden skrypt, który używa obiektu `PSDatalakeStoreAccount` zwróconego przez polecenie `Get-AzDataLakeStoreAccount`, nie powinien odwoływać się do tych właściwości.</span><span class="sxs-lookup"><span data-stu-id="aea72-254">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="aea72-255">Az.KeyVault (wcześniej AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="aea72-255">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="aea72-256">Właściwość `PurgeDisabled` została usunięta z obiektów `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` i `PSKeyVaultSecretAttributes`. Skrypty nie powinny już odwoływać się do właściwości ```PurgeDisabled``` w celu podejmowania decyzji dotyczących przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="aea72-256">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="aea72-257">Az.Media (wcześniej AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="aea72-257">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="aea72-258">Usunięto przestarzały alias właściwości `Tags` z polecenia cmdlet `New-AzMediaService`. Skrypty używające kodu</span><span class="sxs-lookup"><span data-stu-id="aea72-258">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="aea72-259">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="aea72-259">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="aea72-260">Az.Monitor (wcześniej AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="aea72-260">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="aea72-261">Z polecenia cmdlet `Set-AzDiagnosticSetting` usunięto parametry o nazwach w liczbie mnogiej `Categories` i `Timegrains`, aby zastąpić je nazwami parametrów w liczbie pojedynczej. Skrypty używające kodu</span><span class="sxs-lookup"><span data-stu-id="aea72-261">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="aea72-262">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="aea72-262">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="aea72-263">Az.Network (wcześniej AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="aea72-263">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="aea72-264">Usunięto przestarzały parametr `ResourceId` z polecenia cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="aea72-264">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="aea72-265">Usunięto przestarzałą właściwość `EnableVmProtection` z obiektu `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="aea72-265">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="aea72-266">Usunięto przestarzałe polecenie cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="aea72-266">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="aea72-267">Skrypty nie powinny już podejmować decyzji dotyczących przetwarzania na podstawie wartości tych pól.</span><span class="sxs-lookup"><span data-stu-id="aea72-267">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="aea72-268">Az.OperationalInsights (wcześniej AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="aea72-268">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="aea72-269">Usunięto domyślny zestaw parametrów dla polecenia `Get-AzOperationalInsightsDataSource`, a zestaw `ByWorkspaceNameByKind` stał się domyślnym zestawem parametrów</span><span class="sxs-lookup"><span data-stu-id="aea72-269">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="aea72-270">Skrypty zwracające listę źródeł danych przy użyciu polecenia</span><span class="sxs-lookup"><span data-stu-id="aea72-270">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="aea72-271">Należy zmienić tak, aby określały rodzaj</span><span class="sxs-lookup"><span data-stu-id="aea72-271">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="aea72-272">Az.RecoveryServices (wcześniej AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup i AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="aea72-272">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="aea72-273">Usunięto parametr `Encryption` z polecenia cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="aea72-273">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="aea72-274">Parametr `TargetStorageAccountName` jest teraz obowiązkowy na potrzeby przywracania dysku zarządzanego w poleceniu cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="aea72-274">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="aea72-275">Usunięto parametry `StorageAccountName` i `StorageAccountResourceGroupName` w poleceniu cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="aea72-275">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="aea72-276">Usunięto parametr `Name` w poleceniu cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="aea72-276">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="aea72-277">Az.Resources (wcześniej AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="aea72-277">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="aea72-278">Usunięto parametr `Sku` z polecenia cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="aea72-278">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="aea72-279">Usunięto parametr `Password` z poleceń cmdlet `New-AzADServicePrincipal` i `New-AzADSpCredential`. Hasła są generowane automatycznie, a skrypty, które podawały hasło:</span><span class="sxs-lookup"><span data-stu-id="aea72-279">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="aea72-280">Należy zmienić tak, aby uzyskiwały hasło z danych wyjściowych:</span><span class="sxs-lookup"><span data-stu-id="aea72-280">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="aea72-281">Az.ServiceFabric (wcześniej AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="aea72-281">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="aea72-282">Zmieniono następujące zwracane typy poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="aea72-282">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="aea72-283">Właściwość `ServiceTypeHealthPolicies` typu `ApplicationHealthPolicy` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="aea72-283">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="aea72-284">Właściwość `ApplicationHealthPolicies` typu `ClusterUpgradeDeltaHealthPolicy` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="aea72-284">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="aea72-285">Właściwość `OverrideUserUpgradePolicy` typu `ClusterUpgradePolicy` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="aea72-285">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="aea72-286">Te zmiany mają wpływ na następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="aea72-286">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="aea72-287">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="aea72-287">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="aea72-288">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="aea72-288">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="aea72-289">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="aea72-289">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="aea72-290">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="aea72-290">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="aea72-291">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="aea72-291">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="aea72-292">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="aea72-292">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="aea72-293">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="aea72-293">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="aea72-294">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="aea72-294">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="aea72-295">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="aea72-295">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="aea72-296">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="aea72-296">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="aea72-297">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="aea72-297">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="aea72-298">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="aea72-298">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="aea72-299">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="aea72-299">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="aea72-300">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="aea72-300">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="aea72-301">Az.Sql (wcześniej AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="aea72-301">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="aea72-302">Usunięto parametry `State` i `ResourceId` z polecenia cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="aea72-302">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="aea72-303">Usunięto przestarzałe polecenia cmdlet: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` i `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="aea72-303">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="aea72-304">Usunięto przestarzały parametr `Current` z polecenia cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="aea72-304">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="aea72-305">Usunięto przestarzały parametr `DatabaseName` z polecenia cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="aea72-305">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="aea72-306">Usunięto przestarzały parametr `PrivilegedLogin` z polecenia cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="aea72-306">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="aea72-307">Az.Storage (wcześniej Azure.Storage i AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="aea72-307">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="aea72-308">Aby obsługiwać tworzenie kontekstu magazynu OAuth za pomocą tylko nazwy konta magazynu, domyślny zestaw parametrów został zmieniony na `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="aea72-308">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="aea72-309">Przykład: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="aea72-309">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="aea72-310">Parametr `Location` stał się obowiązkowy w poleceniu cmdlet `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="aea72-310">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="aea72-311">Metody interfejsu API magazynu używają teraz wzorca asynchronicznego opartego na zadaniach zamiast synchronicznych wywołań interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="aea72-311">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="aea72-312">W poniższych przykładach pokazano nowe polecenia asynchroniczne:</span><span class="sxs-lookup"><span data-stu-id="aea72-312">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="aea72-313">Migawka obiektu blob</span><span class="sxs-lookup"><span data-stu-id="aea72-313">Blob Snapshot</span></span>

<span data-ttu-id="aea72-314">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="aea72-314">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="aea72-315">Az:</span><span class="sxs-lookup"><span data-stu-id="aea72-315">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="aea72-316">Udostępnianie migawki</span><span class="sxs-lookup"><span data-stu-id="aea72-316">Share Snapshot</span></span>

<span data-ttu-id="aea72-317">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="aea72-317">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="aea72-318">Az:</span><span class="sxs-lookup"><span data-stu-id="aea72-318">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="aea72-319">Cofanie usunięcia nietrwale usuniętego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="aea72-319">Undelete soft-deleted blob</span></span>

<span data-ttu-id="aea72-320">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="aea72-320">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="aea72-321">Az:</span><span class="sxs-lookup"><span data-stu-id="aea72-321">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="aea72-322">Ustawianie warstwy obiektu blob</span><span class="sxs-lookup"><span data-stu-id="aea72-322">Set Blob Tier</span></span>

<span data-ttu-id="aea72-323">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="aea72-323">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="aea72-324">Az:</span><span class="sxs-lookup"><span data-stu-id="aea72-324">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="aea72-325">Az.Websites (wcześniej AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="aea72-325">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="aea72-326">Usunięto przestarzałe właściwości z obiektów `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` i `PSSite`</span><span class="sxs-lookup"><span data-stu-id="aea72-326">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
