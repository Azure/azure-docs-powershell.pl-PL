---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 3b4014b56a36228fe53221430ffe79a43118f8fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894162"
---
# <span data-ttu-id="e2e1d-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e2e1d-101">New-AzFirewall</span></span>

## <span data-ttu-id="e2e1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e1d-103">Tworzy nową zaporę w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="e2e1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2e1d-104">SYNTAX</span></span>

### <span data-ttu-id="e2e1d-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e2e1d-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2e1d-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="e2e1d-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2e1d-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="e2e1d-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e1d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e2e1d-108">DESCRIPTION</span></span>
<span data-ttu-id="e2e1d-109">Polecenie cmdlet **New-AzFirewall** umożliwia utworzenie zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="e2e1d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2e1d-110">EXAMPLES</span></span>

### <span data-ttu-id="e2e1d-111">1: Tworzenie zapory dołączonej do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e2e1d-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="e2e1d-112">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="e2e1d-113">Ponieważ nie określono reguł, zapora blokuje cały ruch (zachowanie domyślne).</span><span class="sxs-lookup"><span data-stu-id="e2e1d-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="e2e1d-114">Zagrożenia procesor Intel będzie również uruchamiany w trybie domyślnym-alertu — co oznacza, że ruch złośliwy będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="e2e1d-115">2: Tworzenie zapory umożliwiającej cały ruch HTTPS</span><span class="sxs-lookup"><span data-stu-id="e2e1d-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="e2e1d-116">W tym przykładzie jest tworzona Zapora umożliwiająca wszystkim ruch HTTPS na porcie 443.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="e2e1d-117">Działanie zagrożeń usługa Intel zostanie uruchomiona w trybie domyślnym-alertu — co oznacza, że złośliwy ruch będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="e2e1d-118">3: DNAT — Przekieruj ruch przeznaczony do 10.1.2.3:80 do 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="e2e1d-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="e2e1d-119">W tym przykładzie utworzono zaporę, która przetłumaczy docelowy adres IP i port wszystkich pakietów wysłanych do 10.1.2.3:80 do 10.2.3.4:8080 Threat Intel jest wyłączona w tym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="e2e1d-120">4: Tworzenie zapory bez reguł i zagrożeń z procesorem Intel w trybie alertu</span><span class="sxs-lookup"><span data-stu-id="e2e1d-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="e2e1d-121">W tym przykładzie jest tworzona Zapora, która blokuje cały ruch (zachowanie domyślne) i ma zagrożenia Intel działa w trybie alarmowym.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="e2e1d-122">Oznacza to, że dzienniki alertów są wysyłane w celu uzyskania szkodliwego ruchu przed zastosowaniem innych reguł (w tym przypadku tylko reguła domyślna — Odmów wszystkich)</span><span class="sxs-lookup"><span data-stu-id="e2e1d-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="e2e1d-123">5: Tworzenie zapory, która zezwala na cały ruch HTTP na porcie 8080, ale blokuje szkodliwe domeny zidentyfikowane przez zagrożenie Intel</span><span class="sxs-lookup"><span data-stu-id="e2e1d-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="e2e1d-124">W tym przykładzie tworzona jest Zapora zezwalająca na cały ruch HTTP na porcie 8080, chyba że zostanie uznany za szkodliwy przez środowisko Intel.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="e2e1d-125">W przypadku uruchamiania w trybie odmowy, w przeciwieństwie do alertu, ruch uważany za szkodliwy przez środowisko Intel nie jest rejestrowany, ale również zablokowany.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="e2e1d-126">6: Tworzenie zapory bez reguł i stref dostępności</span><span class="sxs-lookup"><span data-stu-id="e2e1d-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="e2e1d-127">W tym przykładzie jest tworzona Zapora ze wszystkimi dostępnymi strefami dostępności.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="e2e1d-128">7: Tworzenie zapory z co najmniej dwoma publicznymi adresami IP</span><span class="sxs-lookup"><span data-stu-id="e2e1d-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="e2e1d-129">W tym przykładzie jest tworzona Zapora podłączona do sieci wirtualnej "VNET" z dwoma publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="e2e1d-130">8: Tworzenie zapory, która umożliwia ruch MSSQL do określonej bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e2e1d-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="e2e1d-131">W tym przykładzie tworzona jest Zapora zezwalająca na ruch MSSQL na porcie standardowym 1433 na bazę danych SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="e2e1d-132">9: Tworzenie zapory podłączonej do wirtualnego koncentratora</span><span class="sxs-lookup"><span data-stu-id="e2e1d-132">9:  Create a Firewall attached to a virtual hub</span></span>
```
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="e2e1d-133">W tym przykładzie jest tworzona Zapora dołączona do wirtualnego centrum "vHub".</span><span class="sxs-lookup"><span data-stu-id="e2e1d-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="e2e1d-134">Do zapory zostanie dołączona $fp zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="e2e1d-135">Ta Zapora umożliwia/odrzuca ruch oparty na regułach wymienionych w zasadach zapory $fp.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="e2e1d-136">Koncentrator wirtualny i Zapora powinny znajdować się w tym samym regionie.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="e2e1d-137">10: Tworzenie zapory za pomocą Instalatora whitelist analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="e2e1d-137">10: Create a Firewall with threat intelligence whitelist setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="e2e1d-138">W tym przykładzie jest tworzona Zapora, która whitelist "www.microsoft.com" i "8.8.8.8" z analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="e2e1d-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="e2e1d-139">11: Tworzenie zapory z dostosowanym ustawieniami zakresu prywatnego</span><span class="sxs-lookup"><span data-stu-id="e2e1d-139">11: Create a Firewall with customized private range setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="e2e1d-140">W tym przykładzie jest tworzona Zapora, która traktuje "99.99.99.0/24" i "66.66.0.0/16" jako prywatne zakresy adresów IP, a nie powoduje, że ruch odchodzący do tych adresów</span><span class="sxs-lookup"><span data-stu-id="e2e1d-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="e2e1d-141">12: Tworzenie zapory z podsiecią zarządzania i publicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="e2e1d-141">12:  Create a Firewall with a management subnet and Public IP address</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="e2e1d-142">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="e2e1d-143">Ponieważ nie określono reguł, zapora blokuje cały ruch (zachowanie domyślne).</span><span class="sxs-lookup"><span data-stu-id="e2e1d-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="e2e1d-144">Zagrożenia procesor Intel będzie również uruchamiany w trybie domyślnym-alertu — co oznacza, że ruch złośliwy będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="e2e1d-145">Aby obsługiwać scenariusze "Wymuszone tunelowanie", ta zapora będzie korzystać z podsieci "AzureFirewallManagementSubnet" i publicznego adresu IP zarządzania dla ruchu związanego z zarządzaniem.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="e2e1d-146">13: Tworzenie zapory z zasadami zapory dołączonymi do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e2e1d-146">13:  Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="e2e1d-147">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="e2e1d-148">Reguły i analiza zagrożeń, które zostaną zastosowane do zapory, zostaną pobrane z zasad zapory</span><span class="sxs-lookup"><span data-stu-id="e2e1d-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

## <span data-ttu-id="e2e1d-149">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2e1d-149">PARAMETERS</span></span>

### <span data-ttu-id="e2e1d-150">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e2e1d-150">-ApplicationRuleCollection</span></span>
<span data-ttu-id="e2e1d-151">Określa kolekcje reguł aplikacji dla nowej zapory.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-151">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-152">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2e1d-152">-AsJob</span></span>
<span data-ttu-id="e2e1d-153">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e2e1d-153">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e1d-154">-DefaultProfile</span></span>
<span data-ttu-id="e2e1d-155">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-156">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e2e1d-156">-FirewallPolicyId</span></span>
<span data-ttu-id="e2e1d-157">Zasady zapory podłączone do zapory</span><span class="sxs-lookup"><span data-stu-id="e2e1d-157">The firewall policy attached to the firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-158">-Force</span><span class="sxs-lookup"><span data-stu-id="e2e1d-158">-Force</span></span>
<span data-ttu-id="e2e1d-159">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-159">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-160">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e2e1d-160">-Location</span></span>
<span data-ttu-id="e2e1d-161">Określa region zapory.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-161">Specifies the region for the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-162">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2e1d-162">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="e2e1d-163">Co najmniej jeden publiczny adres IP, który ma być używany do komunikacji z zarządzaniem.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-163">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="e2e1d-164">Publiczne adresy IP muszą używać standardowej jednostki SKU i muszą należeć do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-164">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-165">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2e1d-165">-Name</span></span>
<span data-ttu-id="e2e1d-166">Określa nazwę zapory systemu Azure, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-166">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-167">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e2e1d-167">-NatRuleCollection</span></span>
<span data-ttu-id="e2e1d-168">Lista AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="e2e1d-168">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-169">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e2e1d-169">-NetworkRuleCollection</span></span>
<span data-ttu-id="e2e1d-170">Lista AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="e2e1d-170">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-171">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="e2e1d-171">-PrivateRange</span></span>
<span data-ttu-id="e2e1d-172">Zakresy prywatnych adresów IP, do których nie można SNAT'ed ruchu</span><span class="sxs-lookup"><span data-stu-id="e2e1d-172">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-173">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2e1d-173">-PublicIpAddress</span></span>
<span data-ttu-id="e2e1d-174">Co najmniej jeden publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-174">One or more Public IP Addresses.</span></span> <span data-ttu-id="e2e1d-175">Publiczne adresy IP muszą używać standardowej jednostki SKU i muszą należeć do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-175">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-176">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="e2e1d-176">-PublicIpName</span></span>
<span data-ttu-id="e2e1d-177">Publiczna nazwa IP.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-177">Public Ip Name.</span></span> <span data-ttu-id="e2e1d-178">Publiczny adres IP musi korzystać ze standardowej jednostki SKU i należy do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-178">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e1d-179">-ResourceGroupName</span></span>
<span data-ttu-id="e2e1d-180">Określa nazwę grupy zasobów, która ma zawierać zaporę.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-180">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="e2e1d-181">-Sku</span></span>
<span data-ttu-id="e2e1d-182">Typ SKU dla zapory</span><span class="sxs-lookup"><span data-stu-id="e2e1d-182">The sku type for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-183">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2e1d-183">-Tag</span></span>
<span data-ttu-id="e2e1d-184">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e2e1d-185">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="e2e1d-185">For example:</span></span>

<span data-ttu-id="e2e1d-186">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="e2e1d-186">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-187">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="e2e1d-187">-ThreatIntelMode</span></span>
<span data-ttu-id="e2e1d-188">Określa tryb działania dla analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-188">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="e2e1d-189">Tryb domyślny to alarm, a nie wył.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-189">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-190">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="e2e1d-190">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="e2e1d-191">Whitelist dla analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="e2e1d-191">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-192">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="e2e1d-192">-VirtualHubId</span></span>
<span data-ttu-id="e2e1d-193">Wirtualny koncentrator, do którego jest dołączona Zapora</span><span class="sxs-lookup"><span data-stu-id="e2e1d-193">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-194">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e2e1d-194">-VirtualNetwork</span></span>
<span data-ttu-id="e2e1d-195">Sieć wirtualna</span><span class="sxs-lookup"><span data-stu-id="e2e1d-195">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-196">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e2e1d-196">-VirtualNetworkName</span></span>
<span data-ttu-id="e2e1d-197">Określa nazwę sieci wirtualnej, dla której będzie wdrażana Zapora.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-197">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="e2e1d-198">Sieć wirtualna i Zapora muszą należeć do tej samej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-198">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-199">-Zone</span><span class="sxs-lookup"><span data-stu-id="e2e1d-199">-Zone</span></span>
<span data-ttu-id="e2e1d-200">Lista stref dostępności oznaczająca lokalizację, z której ma się pochodzić Zapora.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-200">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-201">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2e1d-201">-Confirm</span></span>
<span data-ttu-id="e2e1d-202">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-202">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e1d-203">-WhatIf</span></span>
<span data-ttu-id="e2e1d-204">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2e1d-205">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-205">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e1d-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e1d-206">CommonParameters</span></span>
<span data-ttu-id="e2e1d-207">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e1d-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e1d-208">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e1d-208">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e1d-209">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2e1d-209">INPUTS</span></span>

### <span data-ttu-id="e2e1d-210">System. String</span><span class="sxs-lookup"><span data-stu-id="e2e1d-210">System.String</span></span>

### <span data-ttu-id="e2e1d-211">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e2e1d-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="e2e1d-212">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="e2e1d-212">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="e2e1d-213">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2e1d-213">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="e2e1d-214">Microsoft. Azure. Commands. Network. models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="e2e1d-214">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="e2e1d-215">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="e2e1d-215">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="e2e1d-216">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="e2e1d-216">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="e2e1d-217">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e2e1d-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e2e1d-218">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2e1d-218">OUTPUTS</span></span>

### <span data-ttu-id="e2e1d-219">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e2e1d-219">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="e2e1d-220">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2e1d-220">NOTES</span></span>

## <span data-ttu-id="e2e1d-221">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2e1d-221">RELATED LINKS</span></span>

[<span data-ttu-id="e2e1d-222">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e2e1d-222">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="e2e1d-223">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e2e1d-223">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="e2e1d-224">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e2e1d-224">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="e2e1d-225">Nowe — AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e2e1d-225">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="e2e1d-226">Nowe — AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e2e1d-226">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="e2e1d-227">Nowe — AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e2e1d-227">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
