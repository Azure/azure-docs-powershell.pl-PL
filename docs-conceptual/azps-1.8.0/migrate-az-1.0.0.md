---
title: Wszystkie różnice między modułem AzureRM i modułem Az 1.0.0 programu Azure PowerShell
description: Ten przewodnik migracji zawiera listę zmian powodujących niezgodność wprowadzonych w wersji 1 modułu Az programu Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: ea7593cf2b753b210ff2955b7bd450030ad83596
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/05/2020
ms.locfileid: "75035833"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="0dc49-103">Zmiany powodujące niezgodność w module Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0dc49-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="0dc49-104">Ten dokument zawiera szczegółowe informacje na temat różnic między modułem AzureRM w wersji 6.x i nowym modułem Az w wersji 1.x i nowszych.</span><span class="sxs-lookup"><span data-stu-id="0dc49-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="0dc49-105">Spis treści pomoże przeprowadzić Cię przez pełną ścieżkę migracji, w tym zmiany specyficzne dla modułu, które mogą mieć wpływ na skrypty.</span><span class="sxs-lookup"><span data-stu-id="0dc49-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="0dc49-106">Aby uzyskać ogólne porady dotyczące rozpoczynania pracy z migracją z modułu AzureRM do modułu Az, zobacz [Rozpoczynanie migracji z modułu AzureRM do modułu Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="0dc49-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="0dc49-107">Spis treści</span><span class="sxs-lookup"><span data-stu-id="0dc49-107">Table of Contents</span></span>

- [<span data-ttu-id="0dc49-108">Ogólne zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="0dc49-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="0dc49-109">Zmiany prefiksów poleceń cmdlet w postaci rzeczownika</span><span class="sxs-lookup"><span data-stu-id="0dc49-109">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="0dc49-110">Zmiany nazw modułów</span><span class="sxs-lookup"><span data-stu-id="0dc49-110">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="0dc49-111">Usunięte moduły</span><span class="sxs-lookup"><span data-stu-id="0dc49-111">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="0dc49-112">Windows PowerShell 5.1 i .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="0dc49-112">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="0dc49-113">Tymczasowe usunięcie logowania użytkowników przy użyciu obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="0dc49-113">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="0dc49-114">Domyślne logowanie za pomocą kodu urządzenia zamiast monitu przeglądarki internetowej</span><span class="sxs-lookup"><span data-stu-id="0dc49-114">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="0dc49-115">Zmiany powodujące niezgodność modułów</span><span class="sxs-lookup"><span data-stu-id="0dc49-115">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="0dc49-116">Az.ApiManagement (wcześniej AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="0dc49-116">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="0dc49-117">Az.Billing (wcześniej AzureRM.Billing, AzureRM.Consumption i AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="0dc49-117">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="0dc49-118">Az.CognitiveServices (wcześniej AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="0dc49-118">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="0dc49-119">Az.Compute (wcześniej AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="0dc49-119">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="0dc49-120">Az.DataFactory (wcześniej AzureRM.DataFactories i AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="0dc49-120">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="0dc49-121">Az.DataLakeAnalytics (wcześniej AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="0dc49-121">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="0dc49-122">Az.DataLakeStore (wcześniej AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="0dc49-122">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="0dc49-123">Az.KeyVault (wcześniej AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="0dc49-123">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="0dc49-124">Az.Media (wcześniej AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="0dc49-124">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="0dc49-125">Az.Monitor (wcześniej AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="0dc49-125">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="0dc49-126">Az.Network (wcześniej AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="0dc49-126">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="0dc49-127">Az.OperationalInsights (wcześniej AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="0dc49-127">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="0dc49-128">Az.RecoveryServices (wcześniej AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup i AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="0dc49-128">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="0dc49-129">Az.Resources (wcześniej AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="0dc49-129">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="0dc49-130">Az.ServiceFabric (wcześniej AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="0dc49-130">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="0dc49-131">Az.Sql (wcześniej AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="0dc49-131">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="0dc49-132">Az.Storage (wcześniej Azure.Storage i AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="0dc49-132">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="0dc49-133">Az.Websites (wcześniej AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="0dc49-133">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="0dc49-134">Ogólne zmiany powodujące niezgodność</span><span class="sxs-lookup"><span data-stu-id="0dc49-134">General breaking changes</span></span>

<span data-ttu-id="0dc49-135">W tej sekcji przedstawiono ogólne zmiany powodujące niezgodność wprowadzone w ramach przeprojektowania modułu Az.</span><span class="sxs-lookup"><span data-stu-id="0dc49-135">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="0dc49-136">Zmiany prefiksów poleceń cmdlet w postaci rzeczownika</span><span class="sxs-lookup"><span data-stu-id="0dc49-136">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="0dc49-137">W module AzureRM polecenia cmdlet używały ciągu `AzureRM` lub `Azure` jako prefiksu w postaci rzeczownika.</span><span class="sxs-lookup"><span data-stu-id="0dc49-137">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="0dc49-138">Moduł Az upraszcza i normalizuje nazwy poleceń cmdlet, więc wszystkie polecenia cmdlet mają prefiks w postaci rzeczownika „Az”.</span><span class="sxs-lookup"><span data-stu-id="0dc49-138">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="0dc49-139">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="0dc49-139">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="0dc49-140">Zmieniono na:</span><span class="sxs-lookup"><span data-stu-id="0dc49-140">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="0dc49-141">Aby ułatwić przejście na te nowe nazwy poleceń cmdlet, moduł Az wprowadza dwa nowe polecenia cmdlet, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) i [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="0dc49-141">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="0dc49-142">Polecenie cmdlet `Enable-AzureRmAlias` tworzy aliasy dla starszych nazw poleceń cmdlet w module AzureRM mapowane na nowsze nazwy poleceń cmdlet w module Az.</span><span class="sxs-lookup"><span data-stu-id="0dc49-142">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="0dc49-143">Argument `-Scope` polecenia cmdlet `Enable-AzureRmAlias` pozwala wybrać, gdzie aliasy zostaną włączone.</span><span class="sxs-lookup"><span data-stu-id="0dc49-143">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="0dc49-144">Na przykład poniższy skrypt w module AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0dc49-144">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="0dc49-145">Może zostać uruchomiony tylko z niewielkimi zmianami, jeśli zostanie użyte polecenie cmdlet `Enable-AzureRmAlias`:</span><span class="sxs-lookup"><span data-stu-id="0dc49-145">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="0dc49-146">Uruchomienie polecenia cmdlet `Enable-AzureRmAlias -Scope CurrentUser` spowoduje włączenie aliasów dla wszystkich otwieranych sesji programu PowerShell, więc po jego wykonaniu nie trzeba w ogóle zmieniać skryptów podobnych do poniższego:</span><span class="sxs-lookup"><span data-stu-id="0dc49-146">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="0dc49-147">Aby uzyskać szczegółowe informacje dotyczące użycia aliasów poleceń cmdlet, zobacz [Dokumentacja polecenia cmdlet Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="0dc49-147">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="0dc49-148">Gdy wszystko będzie gotowe do wyłączenia aliasów, możesz usunąć utworzone aliasy za pomocą polecenia cmdlet `Disable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="0dc49-148">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="0dc49-149">Aby uzyskać szczegółowe informacje, zobacz [Dokumentacja polecenia cmdlet Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="0dc49-149">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0dc49-150">Podczas wyłączania aliasów upewnij się, że zostaną one wyłączone dla _wszystkich_ zakresów, w których je włączono.</span><span class="sxs-lookup"><span data-stu-id="0dc49-150">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="0dc49-151">Zmiany nazw modułów</span><span class="sxs-lookup"><span data-stu-id="0dc49-151">Module Name Changes</span></span>

<span data-ttu-id="0dc49-152">Nazwy modułów zostały zmienione z `AzureRM.*` na `Az.*`, z wyjątkiem następujących modułów:</span><span class="sxs-lookup"><span data-stu-id="0dc49-152">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="0dc49-153">Moduł AzureRM</span><span class="sxs-lookup"><span data-stu-id="0dc49-153">AzureRM module</span></span> | <span data-ttu-id="0dc49-154">Moduł Az</span><span class="sxs-lookup"><span data-stu-id="0dc49-154">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="0dc49-155">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0dc49-155">Azure.Storage</span></span> | <span data-ttu-id="0dc49-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0dc49-156">Az.Storage</span></span> |
| <span data-ttu-id="0dc49-157">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0dc49-157">Azure.AnalysisServices</span></span> | <span data-ttu-id="0dc49-158">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0dc49-158">Az.AnalysisServices</span></span> |
| <span data-ttu-id="0dc49-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0dc49-159">AzureRM.Profile</span></span> | <span data-ttu-id="0dc49-160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0dc49-160">Az.Accounts</span></span> |
| <span data-ttu-id="0dc49-161">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="0dc49-161">AzureRM.Insights</span></span> | <span data-ttu-id="0dc49-162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0dc49-162">Az.Monitor</span></span> |
| <span data-ttu-id="0dc49-163">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="0dc49-163">AzureRM.DataFactories</span></span> | <span data-ttu-id="0dc49-164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0dc49-164">Az.DataFactory</span></span> |
| <span data-ttu-id="0dc49-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0dc49-165">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="0dc49-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0dc49-166">Az.DataFactory</span></span> |
| <span data-ttu-id="0dc49-167">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0dc49-167">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="0dc49-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0dc49-168">Az.RecoveryServices</span></span> |
| <span data-ttu-id="0dc49-169">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0dc49-169">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="0dc49-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0dc49-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="0dc49-171">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="0dc49-171">AzureRM.Tags</span></span> | <span data-ttu-id="0dc49-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0dc49-172">Az.Resources</span></span> |
| <span data-ttu-id="0dc49-173">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0dc49-173">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="0dc49-174">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0dc49-174">Az.MachineLearning</span></span> |
| <span data-ttu-id="0dc49-175">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="0dc49-175">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="0dc49-176">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0dc49-176">Az.Billing</span></span> |
| <span data-ttu-id="0dc49-177">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="0dc49-177">AzureRM.Consumption</span></span> | <span data-ttu-id="0dc49-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0dc49-178">Az.Billing</span></span> |

<span data-ttu-id="0dc49-179">Zmiany nazw modułów oznaczają, że każdy skrypt, który używa instrukcji `#Requires` lub `Import-Module` do ładowania określonych modułów, będzie trzeba zmienić tak, aby używał nowego modułu.</span><span class="sxs-lookup"><span data-stu-id="0dc49-179">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="0dc49-180">Jeśli dla danego modułu sufiks polecenia cmdlet pozostał taki sam, oznacza to, że chociaż nazwa modułu się zmieniła, to sufiks wskazujący obszar operacji _nie_ uległ zmianie.</span><span class="sxs-lookup"><span data-stu-id="0dc49-180">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="0dc49-181">Migrowanie instrukcji #Requires i Import-Module</span><span class="sxs-lookup"><span data-stu-id="0dc49-181">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="0dc49-182">Skrypty używające instrukcji `#Requires` lub `Import-Module` do deklarowania zależności od modułów AzureRM należy zaktualizować tak, aby używały nowych nazw modułów.</span><span class="sxs-lookup"><span data-stu-id="0dc49-182">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="0dc49-183">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="0dc49-183">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="0dc49-184">Należy zmienić na:</span><span class="sxs-lookup"><span data-stu-id="0dc49-184">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="0dc49-185">Instrukcję `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="0dc49-185">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="0dc49-186">Należy zmienić na:</span><span class="sxs-lookup"><span data-stu-id="0dc49-186">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="0dc49-187">Migrowanie w pełni kwalifikowanych wywołań poleceń cmdlet</span><span class="sxs-lookup"><span data-stu-id="0dc49-187">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="0dc49-188">Skrypty używające wywołań poleceń cmdlet kwalifikowanych za pomocą modułu, takie jak:</span><span class="sxs-lookup"><span data-stu-id="0dc49-188">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="0dc49-189">Należy zmienić tak, aby używały nowych nazw modułów i poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0dc49-189">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="0dc49-190">Migrowanie zależności manifestu modułów</span><span class="sxs-lookup"><span data-stu-id="0dc49-190">Migrating module manifest dependencies</span></span>

<span data-ttu-id="0dc49-191">W przypadku modułów, w których zależności od modułów AzureRM są wyrażane za pomocą pliku manifestu modułów (psd1), należy zaktualizować nazwy modułów w sekcji `RequiredModules`:</span><span class="sxs-lookup"><span data-stu-id="0dc49-191">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="0dc49-192">Należy zmienić na:</span><span class="sxs-lookup"><span data-stu-id="0dc49-192">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="0dc49-193">Usunięte moduły</span><span class="sxs-lookup"><span data-stu-id="0dc49-193">Removed modules</span></span>

<span data-ttu-id="0dc49-194">Następujące moduły zostały usunięte:</span><span class="sxs-lookup"><span data-stu-id="0dc49-194">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="0dc49-195">Narzędzia dla tych usług nie są już aktywnie wspierane.</span><span class="sxs-lookup"><span data-stu-id="0dc49-195">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="0dc49-196">Zachęcamy klientów do jak najszybszego przechodzenia do alternatywnych usług.</span><span class="sxs-lookup"><span data-stu-id="0dc49-196">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="0dc49-197">Windows PowerShell 5.1 i .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="0dc49-197">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="0dc49-198">Korzystanie z modułu Az w programie PowerShell 5.1 dla systemu Windows wymaga zainstalowania programu .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="0dc49-198">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="0dc49-199">Jeśli używasz programu PowerShell Core w wersji 6.x lub nowszej, program .NET Framework nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0dc49-199">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="0dc49-200">Tymczasowe usunięcie logowania użytkowników przy użyciu obiektu PSCredential</span><span class="sxs-lookup"><span data-stu-id="0dc49-200">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="0dc49-201">Ze względu na zmiany w przepływie uwierzytelniania dla platformy .NET Standard tymczasowo usuwamy możliwość logowania użytkownika za pomocą obiektu PSCredential.</span><span class="sxs-lookup"><span data-stu-id="0dc49-201">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="0dc49-202">Ta możliwość zostanie ponownie udostępniona w wersji dla programu PowerShell 5.1 dla systemu Windows opublikowanej 15.01.2019.</span><span class="sxs-lookup"><span data-stu-id="0dc49-202">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="0dc49-203">Ta kwestia została szczegółowo omówiona w ramach [tego problemu w usłudze GitHub.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="0dc49-203">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="0dc49-204">Domyślne logowanie za pomocą kodu urządzenia zamiast monitu przeglądarki internetowej</span><span class="sxs-lookup"><span data-stu-id="0dc49-204">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="0dc49-205">Ze względu na zmiany w przepływie uwierzytelniania dla platformy .NET Standard używamy logowania urządzenia jako domyślnego przepływu logowania podczas logowania interakcyjnego.</span><span class="sxs-lookup"><span data-stu-id="0dc49-205">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="0dc49-206">Logowanie oparte na przeglądarce internetowej ponownie stanie się domyślne dla programu PowerShell 5.1 dla systemu Windows w wersji opublikowanej 15.01.2019.</span><span class="sxs-lookup"><span data-stu-id="0dc49-206">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="0dc49-207">Użytkownicy będą wtedy mogli wybrać logowanie urządzenia za pomocą parametru przełącznika.</span><span class="sxs-lookup"><span data-stu-id="0dc49-207">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="0dc49-208">Zmiany powodujące niezgodność modułów</span><span class="sxs-lookup"><span data-stu-id="0dc49-208">Module breaking changes</span></span>

<span data-ttu-id="0dc49-209">W tej sekcji szczegółowo opisano konkretne zmiany powodujące niezgodność w poszczególnych modułach i poleceniach cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dc49-209">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="0dc49-210">Az.ApiManagement (wcześniej AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="0dc49-210">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="0dc49-211">Usunięto następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0dc49-211">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="0dc49-212">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dc49-212">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="0dc49-213">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="0dc49-213">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="0dc49-214">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="0dc49-214">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="0dc49-215">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="0dc49-215">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="0dc49-216">Zamiast nich do ustawiania tych właściwości użyj polecenia cmdlet **Set-AzApiManagement**</span><span class="sxs-lookup"><span data-stu-id="0dc49-216">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="0dc49-217">Usunięto następujące właściwości:</span><span class="sxs-lookup"><span data-stu-id="0dc49-217">Removed the following properties:</span></span>
  - <span data-ttu-id="0dc49-218">Usunięto właściwości `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` i `ScmHostnameConfiguration` typu `PsApiManagementHostnameConfiguration` z klasy `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="0dc49-218">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="0dc49-219">Zamiast nich używaj właściwości `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` i `ScmCustomHostnameConfiguration` typu `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0dc49-219">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="0dc49-220">Usunięto właściwość `StaticIPs` z klasy PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0dc49-220">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="0dc49-221">Właściwość została podzielona na właściwości `PublicIPAddresses` i `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="0dc49-221">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="0dc49-222">Usunięto wymaganą właściwość `Location` z polecenia cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="0dc49-222">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="0dc49-223">Az.Billing (wcześniej AzureRM.Billing, AzureRM.Consumption i AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="0dc49-223">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="0dc49-224">Parametr `InvoiceName` został usunięty z polecenia cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="0dc49-224">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="0dc49-225">W skryptach będzie trzeba używać innych parametrów tożsamości na potrzeby faktury.</span><span class="sxs-lookup"><span data-stu-id="0dc49-225">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="0dc49-226">Az.CognitiveServices (wcześniej AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="0dc49-226">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="0dc49-227">Usunięto zestaw parametrów `GetSkusWithAccountParamSetName` z polecenia cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="0dc49-227">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="0dc49-228">Musisz uzyskiwać jednostki SKU według typu konta i lokalizacji, a nie nazwy grupy zasobów i nazwy konta.</span><span class="sxs-lookup"><span data-stu-id="0dc49-228">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="0dc49-229">Az.Compute (wcześniej AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="0dc49-229">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="0dc49-230">Pole `IdentityIds` zostało usunięte z właściwości `Identity` w obiektach `PSVirtualMachine` i `PSVirtualMachineScaleSet`. Skrypty nie powinny już używać wartości tego pola do podejmowania decyzji dotyczących przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="0dc49-230">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="0dc49-231">Typ właściwości `InstanceView` obiektu `PSVirtualMachineScaleSetVM` został zmieniony z `VirtualMachineInstanceView` na `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="0dc49-231">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="0dc49-232">Właściwości `AutoOSUpgradePolicy` i `AutomaticOSUpgrade` zostały usunięte z właściwości `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="0dc49-232">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="0dc49-233">Typ właściwości `Sku` w obiekcie `PSSnapshotUpdate` został zmieniony z `DiskSku` na `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="0dc49-233">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="0dc49-234">Zestaw `VmScaleSetVMParameterSet` został usunięty z polecenia cmdlet `Add-AzVMDataDisk`. Nie można już dodawać pojedynczego dysku danych do maszyny wirtualnej w zestawie skalowania.</span><span class="sxs-lookup"><span data-stu-id="0dc49-234">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="0dc49-235">Az.DataFactory (wcześniej AzureRM.DataFactories i AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="0dc49-235">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="0dc49-236">Parametr `GatewayName` stał się obowiązkowy w poleceniu cmdlet `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="0dc49-236">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="0dc49-237">Usunięto polecenie cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="0dc49-237">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="0dc49-238">Usunięto parametr `LinkedServiceName` z polecenia cmdlet `Get-AzDataFactoryV2ActivityRun`. Skrypty nie powinny już używać wartości tego pola do podejmowania decyzji dotyczących przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="0dc49-238">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="0dc49-239">Az.DataLakeAnalytics (wcześniej AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="0dc49-239">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="0dc49-240">Usunięto przestarzałe polecenia cmdlet: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` i `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="0dc49-240">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="0dc49-241">Az.DataLakeStore (wcześniej AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="0dc49-241">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="0dc49-242">W następujących poleceniach cmdlet typ parametru `Encoding` został zmieniony z `FileSystemCmdletProviderEncoding` na `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="0dc49-242">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="0dc49-243">W ramach tej zmiany usunięto wartości kodowania `String` i `Oem`.</span><span class="sxs-lookup"><span data-stu-id="0dc49-243">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="0dc49-244">Nadal dostępne są wszystkie pozostałe wcześniejsze wartości kodowania.</span><span class="sxs-lookup"><span data-stu-id="0dc49-244">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="0dc49-245">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0dc49-245">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="0dc49-246">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="0dc49-246">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="0dc49-247">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="0dc49-247">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="0dc49-248">Usunięto przestarzały alias właściwości `Tags` z poleceń cmdlet `New-AzDataLakeStoreAccount` i `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="0dc49-248">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="0dc49-249">Skrypty używające kodu</span><span class="sxs-lookup"><span data-stu-id="0dc49-249">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="0dc49-250">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="0dc49-250">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="0dc49-251">Usunięto przestarzałe właściwości `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` i `FirewallAllowAzureIps` z obiektu `PSDataLakeStoreAccountBasic`.</span><span class="sxs-lookup"><span data-stu-id="0dc49-251">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="0dc49-252">Żaden skrypt, który używa obiektu `PSDatalakeStoreAccount` zwróconego przez polecenie `Get-AzDataLakeStoreAccount`, nie powinien odwoływać się do tych właściwości.</span><span class="sxs-lookup"><span data-stu-id="0dc49-252">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="0dc49-253">Az.KeyVault (wcześniej AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="0dc49-253">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="0dc49-254">Właściwość `PurgeDisabled` została usunięta z obiektów `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` i `PSKeyVaultSecretAttributes`. Skrypty nie powinny już odwoływać się do właściwości ```PurgeDisabled``` w celu podejmowania decyzji dotyczących przetwarzania.</span><span class="sxs-lookup"><span data-stu-id="0dc49-254">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="0dc49-255">Az.Media (wcześniej AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="0dc49-255">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="0dc49-256">Usunięto przestarzały alias właściwości `Tags` z polecenia cmdlet `New-AzMediaService`. Skrypty używające kodu</span><span class="sxs-lookup"><span data-stu-id="0dc49-256">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="0dc49-257">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="0dc49-257">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="0dc49-258">Az.Monitor (wcześniej AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="0dc49-258">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="0dc49-259">Z polecenia cmdlet `Set-AzDiagnosticSetting` usunięto parametry o nazwach w liczbie mnogiej `Categories` i `Timegrains`, aby zastąpić je nazwami parametrów w liczbie pojedynczej. Skrypty używające kodu</span><span class="sxs-lookup"><span data-stu-id="0dc49-259">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="0dc49-260">Należy zmienić na</span><span class="sxs-lookup"><span data-stu-id="0dc49-260">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="0dc49-261">Az.Network (wcześniej AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="0dc49-261">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="0dc49-262">Usunięto przestarzały parametr `ResourceId` z polecenia cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="0dc49-262">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="0dc49-263">Usunięto przestarzałą właściwość `EnableVmProtection` z obiektu `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="0dc49-263">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="0dc49-264">Usunięto przestarzałe polecenie cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="0dc49-264">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="0dc49-265">Skrypty nie powinny już podejmować decyzji dotyczących przetwarzania na podstawie wartości tych pól.</span><span class="sxs-lookup"><span data-stu-id="0dc49-265">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="0dc49-266">Az.OperationalInsights (wcześniej AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="0dc49-266">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="0dc49-267">Usunięto domyślny zestaw parametrów dla polecenia `Get-AzOperationalInsightsDataSource`, a zestaw `ByWorkspaceNameByKind` stał się domyślnym zestawem parametrów</span><span class="sxs-lookup"><span data-stu-id="0dc49-267">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="0dc49-268">Skrypty zwracające listę źródeł danych przy użyciu polecenia</span><span class="sxs-lookup"><span data-stu-id="0dc49-268">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="0dc49-269">Należy zmienić tak, aby określały rodzaj</span><span class="sxs-lookup"><span data-stu-id="0dc49-269">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="0dc49-270">Az.RecoveryServices (wcześniej AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup i AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="0dc49-270">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="0dc49-271">Usunięto parametr `Encryption` z polecenia cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="0dc49-271">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="0dc49-272">Parametr `TargetStorageAccountName` jest teraz obowiązkowy na potrzeby przywracania dysku zarządzanego w poleceniu cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="0dc49-272">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="0dc49-273">Usunięto parametry `StorageAccountName` i `StorageAccountResourceGroupName` w poleceniu cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="0dc49-273">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="0dc49-274">Usunięto parametr `Name` w poleceniu cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="0dc49-274">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="0dc49-275">Az.Resources (wcześniej AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="0dc49-275">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="0dc49-276">Usunięto parametr `Sku` z polecenia cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="0dc49-276">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="0dc49-277">Usunięto parametr `Password` z poleceń cmdlet `New-AzADServicePrincipal` i `New-AzADSpCredential`. Hasła są generowane automatycznie, a skrypty, które podawały hasło:</span><span class="sxs-lookup"><span data-stu-id="0dc49-277">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="0dc49-278">Należy zmienić tak, aby uzyskiwały hasło z danych wyjściowych:</span><span class="sxs-lookup"><span data-stu-id="0dc49-278">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="0dc49-279">Az.ServiceFabric (wcześniej AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="0dc49-279">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="0dc49-280">Zmieniono następujące zwracane typy poleceń cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0dc49-280">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="0dc49-281">Właściwość `ServiceTypeHealthPolicies` typu `ApplicationHealthPolicy` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0dc49-281">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="0dc49-282">Właściwość `ApplicationHealthPolicies` typu `ClusterUpgradeDeltaHealthPolicy` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0dc49-282">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="0dc49-283">Właściwość `OverrideUserUpgradePolicy` typu `ClusterUpgradePolicy` została usunięta.</span><span class="sxs-lookup"><span data-stu-id="0dc49-283">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="0dc49-284">Te zmiany mają wpływ na następujące polecenia cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0dc49-284">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="0dc49-285">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0dc49-285">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="0dc49-286">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0dc49-286">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="0dc49-287">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0dc49-287">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="0dc49-288">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0dc49-288">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="0dc49-289">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0dc49-289">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="0dc49-290">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0dc49-290">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="0dc49-291">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0dc49-291">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="0dc49-292">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0dc49-292">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="0dc49-293">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0dc49-293">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="0dc49-294">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0dc49-294">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="0dc49-295">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0dc49-295">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="0dc49-296">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="0dc49-296">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="0dc49-297">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="0dc49-297">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="0dc49-298">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="0dc49-298">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="0dc49-299">Az.Sql (wcześniej AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="0dc49-299">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="0dc49-300">Usunięto parametry `State` i `ResourceId` z polecenia cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="0dc49-300">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="0dc49-301">Usunięto przestarzałe polecenia cmdlet: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing` i `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="0dc49-301">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="0dc49-302">Usunięto przestarzały parametr `Current` z polecenia cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="0dc49-302">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="0dc49-303">Usunięto przestarzały parametr `DatabaseName` z polecenia cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="0dc49-303">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="0dc49-304">Usunięto przestarzały parametr `PrivilegedLogin` z polecenia cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="0dc49-304">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="0dc49-305">Az.Storage (wcześniej Azure.Storage i AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="0dc49-305">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="0dc49-306">Aby obsługiwać tworzenie kontekstu magazynu OAuth za pomocą tylko nazwy konta magazynu, domyślny zestaw parametrów został zmieniony na `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="0dc49-306">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="0dc49-307">Przykład: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="0dc49-307">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="0dc49-308">Parametr `Location` stał się obowiązkowy w poleceniu cmdlet `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="0dc49-308">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="0dc49-309">Metody interfejsu API magazynu używają teraz wzorca asynchronicznego opartego na zadaniach zamiast synchronicznych wywołań interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0dc49-309">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="0dc49-310">W poniższych przykładach pokazano nowe polecenia asynchroniczne:</span><span class="sxs-lookup"><span data-stu-id="0dc49-310">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="0dc49-311">Migawka obiektu blob</span><span class="sxs-lookup"><span data-stu-id="0dc49-311">Blob Snapshot</span></span>

<span data-ttu-id="0dc49-312">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0dc49-312">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="0dc49-313">Az:</span><span class="sxs-lookup"><span data-stu-id="0dc49-313">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="0dc49-314">Udostępnianie migawki</span><span class="sxs-lookup"><span data-stu-id="0dc49-314">Share Snapshot</span></span>

<span data-ttu-id="0dc49-315">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0dc49-315">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="0dc49-316">Az:</span><span class="sxs-lookup"><span data-stu-id="0dc49-316">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="0dc49-317">Cofanie usunięcia nietrwale usuniętego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="0dc49-317">Undelete soft-deleted blob</span></span>

<span data-ttu-id="0dc49-318">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0dc49-318">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="0dc49-319">Az:</span><span class="sxs-lookup"><span data-stu-id="0dc49-319">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="0dc49-320">Ustawianie warstwy obiektu blob</span><span class="sxs-lookup"><span data-stu-id="0dc49-320">Set Blob Tier</span></span>

<span data-ttu-id="0dc49-321">AzureRM:</span><span class="sxs-lookup"><span data-stu-id="0dc49-321">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="0dc49-322">Az:</span><span class="sxs-lookup"><span data-stu-id="0dc49-322">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="0dc49-323">Az.Websites (wcześniej AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="0dc49-323">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="0dc49-324">Usunięto przestarzałe właściwości z obiektów `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` i `PSSite`</span><span class="sxs-lookup"><span data-stu-id="0dc49-324">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
