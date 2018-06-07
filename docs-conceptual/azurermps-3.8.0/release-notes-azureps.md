---
title: Dziennik zmian w programie Azure PowerShell | Microsoft Docs
description: Jest to historia zmian wprowadzonych w programie Azure PowerShell w jego najnowszej wersji.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 2e17b6f7f62f25d8d91c4d32a4a1ae5c45b8665d
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821806"
---
# <a name="release-notes"></a><span data-ttu-id="d2e38-103">Informacje o wersji</span><span class="sxs-lookup"><span data-stu-id="d2e38-103">Release notes</span></span>

<span data-ttu-id="d2e38-104">To jest lista zmian wprowadzonych w programie Azure PowerShell w tym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="d2e38-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-380"></a><span data-ttu-id="d2e38-105">Wersja 3.8.0</span><span class="sxs-lookup"><span data-stu-id="d2e38-105">Version 3.8.0</span></span>
* <span data-ttu-id="d2e38-106">Wystąpienia obliczeniowe</span><span class="sxs-lookup"><span data-stu-id="d2e38-106">Compute</span></span>
  - <span data-ttu-id="d2e38-107">Naprawiono błąd w poleceniach cmdlet Get-\*, aby zezwolić na pobieranie wielu stron danych (więcej niż 120 elementów)</span><span class="sxs-lookup"><span data-stu-id="d2e38-107">Fix bug in Get-\* cmdlets, to allow retrieving multiple pages of data (more than 120 items)</span></span>
* <span data-ttu-id="d2e38-108">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d2e38-108">DataLakeAnalytics</span></span>
  - <span data-ttu-id="d2e38-109">Naprawiono pomoc dla niektórych poleceń tak, aby zawierała właściwe sformułowania i przykłady.</span><span class="sxs-lookup"><span data-stu-id="d2e38-109">Fix help for some commands to have the proper verbage and examples.</span></span>
* <span data-ttu-id="d2e38-110">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d2e38-110">DataLakeStore</span></span>
  - <span data-ttu-id="d2e38-111">Dodano obsługę rozpoczęcia i zakończenia polecenia cmdlet `Get-AzureRMDataLakeStoreItemContent`.</span><span class="sxs-lookup"><span data-stu-id="d2e38-111">Add support for head and tail to the `Get-AzureRMDataLakeStoreItemContent` cmdlet.</span></span> <span data-ttu-id="d2e38-112">Pozwala to zwracać N pierwszych lub N ostatnich wierszy tekstu rozdzielanych znakiem nowego wiersza, które mają być wyświetlone.</span><span class="sxs-lookup"><span data-stu-id="d2e38-112">This enables returning the top N or last N new line delimited rows to be displayed.</span></span>
* <span data-ttu-id="d2e38-113">HDInsight</span><span class="sxs-lookup"><span data-stu-id="d2e38-113">HDInsight</span></span>
  - <span data-ttu-id="d2e38-114">Dodano obsługę typu klastra RServer</span><span class="sxs-lookup"><span data-stu-id="d2e38-114">Added support for RServer cluster type</span></span>
    + <span data-ttu-id="d2e38-115">Rozmiar maszyny wirtualnej Edgenode można określić dla klastra oprogramowania RServer w poleceniu New-AzureRmHDInsightCluster lub New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d2e38-115">Edgenode VM size can be specified for RServer cluster in New-AzureRmHDInsightCluster or New-AzureRmHDInsightClusterConfig</span></span>
    + <span data-ttu-id="d2e38-116">Program RServer jest teraz opcją konfiguracji w poleceniu Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="d2e38-116">RServer is now a configuration option in Add-AzureRmHDInsightConfigValues.</span></span> <span data-ttu-id="d2e38-117">Umożliwia on ustawienie flagi RStudio w celu wskazania, że należy przeprowadzić instalację programu R Studio.</span><span class="sxs-lookup"><span data-stu-id="d2e38-117">It allows for RStudio flag to be set to indicate that R Studio installation should be done.</span></span>
* <span data-ttu-id="d2e38-118">LogicApp</span><span class="sxs-lookup"><span data-stu-id="d2e38-118">LogicApp</span></span>
  - <span data-ttu-id="d2e38-119">Polecenia cmdlet Set-AzureRmIntegrationAccountSchema i Set-AzureRmIntegrationAccountMap zostały naprawione dla problemu z elementem contentlink (ustawienie elementów content i contentlink powodowało niepowodzenie aktualizacji).</span><span class="sxs-lookup"><span data-stu-id="d2e38-119">Set-AzureRmIntegrationAccountSchema and Set-AzureRmIntegrationAccountMap cmdlets are fixed for the contentlink issue(Both content and contentlink were set resulting in update failure).</span></span>
* <span data-ttu-id="d2e38-120">Sieć</span><span class="sxs-lookup"><span data-stu-id="d2e38-120">Network</span></span>
  - <span data-ttu-id="d2e38-121">Do bram Application Gateway dodano obsługę nowych funkcji zapory aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="d2e38-121">Added support for new web application firewall features to Application Gateways</span></span>
    + <span data-ttu-id="d2e38-122">Dodano polecenie New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="d2e38-122">Added New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>
    + <span data-ttu-id="d2e38-123">Dodano polecenie Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span><span class="sxs-lookup"><span data-stu-id="d2e38-123">Added Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span></span>
    + <span data-ttu-id="d2e38-124">Zaktualizowano polecenie New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: dodano parametr -RuleSetType -RuleSetVersion i -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="d2e38-124">Updated New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
    + <span data-ttu-id="d2e38-125">Zaktualizowano polecenie Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: dodano parametr -RuleSetType -RuleSetVersion i -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="d2e38-125">Updated Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
  - <span data-ttu-id="d2e38-126">Dodano obsługę zasad protokołu IPSec do połączeń bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d2e38-126">Added support for IPSec policies to Virtual Network Gateway Connections</span></span>
  - <span data-ttu-id="d2e38-127">Dodano polecenie New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d2e38-127">Added New-AzureRmIpsecPolicy</span></span>
  - <span data-ttu-id="d2e38-128">Zaktualizowano polecenie New-AzureRmVirtualNetworkGatewayConnection: dodano parametr -IpsecPolicies i -UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="d2e38-128">Updated New-AzureRmVirtualNetworkGatewayConnection: Added parameter -IpsecPolicies and -UsePolicyBasedTrafficSelectors</span></span>
* <span data-ttu-id="d2e38-129">Profil</span><span class="sxs-lookup"><span data-stu-id="d2e38-129">Profile</span></span>
  - <span data-ttu-id="d2e38-130">*Przestarzałe*: Nazwa polecenia Save-AzureRmProfile została zmieniona na Save-AzureRmContext, przy czym istnieje alias dla starej nazwy polecenia cmdlet, który zostanie usunięty w następnej wersji.</span><span class="sxs-lookup"><span data-stu-id="d2e38-130">*Obsolete*: Save-AzureRmProfile is renamed to Save-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="d2e38-131">*Przestarzałe*: Nazwa polecenia Select-AzureRmProfile została zmieniona na Import-AzureRmContext, przy czym istnieje alias dla starej nazwy polecenia cmdlet, który zostanie usunięty w następnej wersji.</span><span class="sxs-lookup"><span data-stu-id="d2e38-131">*Obsolete*: Select-AzureRmProfile is renamed to Import-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="d2e38-132">Typy wyjściowe PSAzureContext i PSAzureProfile poleceń cmdlet profilu zostaną zmienione w następnej wersji.</span><span class="sxs-lookup"><span data-stu-id="d2e38-132">The PSAzureContext and PSAzureProfile output types of profile cmdlets will be changed in the next release.</span></span>
  - <span data-ttu-id="d2e38-133">Polecenie cmdlet Save-AzureRmContext nie będzie miało typu OutputType w następnej wersji.</span><span class="sxs-lookup"><span data-stu-id="d2e38-133">The Save-AzureRmContext cmdlet will have no OutputType in the next release.</span></span>
  - <span data-ttu-id="d2e38-134">Naprawiono błąd we wspólnym kodzie polecenia cmdlet dotyczący użycia zgodnego ze standardem FIPS algorytmu dla skrótów danych: https://github.com/Azure/azure-powershell/issues/3651</span><span class="sxs-lookup"><span data-stu-id="d2e38-134">Fix bug in cmdlet common code to use FIPS-compliant algorithm for data hashes: https://github.com/Azure/azure-powershell/issues/3651</span></span>
* <span data-ttu-id="d2e38-135">Sql</span><span class="sxs-lookup"><span data-stu-id="d2e38-135">Sql</span></span>
  - <span data-ttu-id="d2e38-136">Naprawiono błędy poleceń cmdlet grupy trybu failover platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d2e38-136">Bug fixes on Azure Failover Group Cmdlets</span></span>
  - <span data-ttu-id="d2e38-137">Poprawiono sondowanie operacji</span><span class="sxs-lookup"><span data-stu-id="d2e38-137">Fix for operation polling</span></span>
  - <span data-ttu-id="d2e38-138">Poprawiono wartość GracePeriodWithDataLossHour podczas ustawiania wartości właściwości FailoverPolicy na Manual</span><span class="sxs-lookup"><span data-stu-id="d2e38-138">Fix GracePeriodWithDataLossHour value when setting FailoverPolicy to Manual</span></span>
* <span data-ttu-id="d2e38-139">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d2e38-139">TrafficManager</span></span>
  - <span data-ttu-id="d2e38-140">Obsługa metody geograficznego routingu ruchu</span><span class="sxs-lookup"><span data-stu-id="d2e38-140">Support for the Geographic traffic routing method</span></span>
    + <span data-ttu-id="d2e38-141">Nowa wartość „Geographic” dla parametru TrafficRoutingMethod polecenia New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d2e38-141">New value 'Geographic' for the TrafficRoutingMethod parameter of New-AzureRmTrafficManagerProfile</span></span>
    + <span data-ttu-id="d2e38-142">Nowy parametr „GeoMapping” dla polecenia New-AzureRmTrafficManagerEndpoint i Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d2e38-142">New parameter 'GeoMapping' for the New-AzureRmTrafficManagerEndpoint and Add-AzureRmTrafficManagerEndpointConfig</span></span>
    + <span data-ttu-id="d2e38-143">Naprawiono przesyłanie potokowe dla polecenia Get-AzureRmTrafficManagerProfile, gdy zwraca ono kolekcję profilów</span><span class="sxs-lookup"><span data-stu-id="d2e38-143">Fix piping for Get-AzureRmTrafficManagerProfile when it returns a collection of profiles</span></span>
* <span data-ttu-id="d2e38-144">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="d2e38-144">ServiceManagement</span></span>
  - <span data-ttu-id="d2e38-145">Restart-AzureVM: dodano parametr InitiateMaintenance w celu przeprowadzania konserwacji podczas ponownego uruchamiania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d2e38-145">Restart-AzureVM: Added InitiateMaintenance parameter for performing maintenance during VM restart.</span></span>
  - <span data-ttu-id="d2e38-146">Get-AzureVM: dodano pole stanu konserwacji.</span><span class="sxs-lookup"><span data-stu-id="d2e38-146">Get-AzureVM: Added Maintenance Status field.</span></span>
  - <span data-ttu-id="d2e38-147">Dodano nowe polecenia cmdlet do obsługi uaktualnienia magazynu usługi Recovery Services</span><span class="sxs-lookup"><span data-stu-id="d2e38-147">Added new cmdlets to support Recovery Services vault upgrade</span></span>
    + <span data-ttu-id="d2e38-148">Test-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="d2e38-148">Test-AzureRecoveryServicesVaultUpgrade</span></span>
    + <span data-ttu-id="d2e38-149">Invoke-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="d2e38-149">Invoke-AzureRecoveryServicesVaultUpgrade</span></span>
