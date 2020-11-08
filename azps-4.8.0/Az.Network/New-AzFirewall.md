---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: a7c38a264860ad4a8458dbdb3555980279a33ff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223827"
---
# <span data-ttu-id="f78ca-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f78ca-101">New-AzFirewall</span></span>

## <span data-ttu-id="f78ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f78ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f78ca-103">Tworzy nową zaporę w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f78ca-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="f78ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f78ca-104">SYNTAX</span></span>

### <span data-ttu-id="f78ca-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f78ca-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f78ca-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="f78ca-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f78ca-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="f78ca-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f78ca-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f78ca-108">DESCRIPTION</span></span>
<span data-ttu-id="f78ca-109">Polecenie cmdlet **New-AzFirewall** umożliwia utworzenie zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f78ca-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="f78ca-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f78ca-110">EXAMPLES</span></span>

### <span data-ttu-id="f78ca-111">Przykład 1. Tworzenie zapory dołączonej do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f78ca-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="f78ca-112">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f78ca-113">Ponieważ nie określono reguł, zapora blokuje cały ruch (zachowanie domyślne).</span><span class="sxs-lookup"><span data-stu-id="f78ca-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="f78ca-114">Zagrożenia procesor Intel będzie również uruchamiany w trybie domyślnym-alertu — co oznacza, że ruch złośliwy będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="f78ca-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="f78ca-115">Przykład 2: Tworzenie zapory zezwalającej na cały ruch HTTPS</span><span class="sxs-lookup"><span data-stu-id="f78ca-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="f78ca-116">W tym przykładzie jest tworzona Zapora umożliwiająca wszystkim ruch HTTPS na porcie 443.</span><span class="sxs-lookup"><span data-stu-id="f78ca-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="f78ca-117">Działanie zagrożeń usługa Intel zostanie uruchomiona w trybie domyślnym-alertu — co oznacza, że złośliwy ruch będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="f78ca-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="f78ca-118">Przykład 3: DNAT — Przekieruj ruch przeznaczony do 10.1.2.3:80 do 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="f78ca-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="f78ca-119">W tym przykładzie utworzono zaporę, która przetłumaczy docelowy adres IP i port wszystkich pakietów wysłanych do 10.1.2.3:80 do 10.2.3.4:8080 Threat Intel jest wyłączona w tym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="f78ca-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="f78ca-120">Przykład 4: Tworzenie zapory bez reguł i z zagrożeniami Intel w trybie alertu</span><span class="sxs-lookup"><span data-stu-id="f78ca-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="f78ca-121">W tym przykładzie jest tworzona Zapora, która blokuje cały ruch (zachowanie domyślne) i ma zagrożenia Intel działa w trybie alarmowym.</span><span class="sxs-lookup"><span data-stu-id="f78ca-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="f78ca-122">Oznacza to, że dzienniki alertów są wysyłane w celu uzyskania szkodliwego ruchu przed zastosowaniem innych reguł (w tym przypadku tylko reguła domyślna — Odmów wszystkich)</span><span class="sxs-lookup"><span data-stu-id="f78ca-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="f78ca-123">Przykład 5: Tworzenie zapory, która zezwala na cały ruch HTTP na porcie 8080, ale blokuje szkodliwe domeny zidentyfikowane przez zagrożenie Intel</span><span class="sxs-lookup"><span data-stu-id="f78ca-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="f78ca-124">W tym przykładzie tworzona jest Zapora zezwalająca na cały ruch HTTP na porcie 8080, chyba że zostanie uznany za szkodliwy przez środowisko Intel.</span><span class="sxs-lookup"><span data-stu-id="f78ca-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="f78ca-125">W przypadku uruchamiania w trybie odmowy, w przeciwieństwie do alertu, ruch uważany za szkodliwy przez środowisko Intel nie jest rejestrowany, ale również zablokowany.</span><span class="sxs-lookup"><span data-stu-id="f78ca-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="f78ca-126">Przykład 6: Tworzenie zapory bez reguł i stref dostępności</span><span class="sxs-lookup"><span data-stu-id="f78ca-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="f78ca-127">W tym przykładzie jest tworzona Zapora ze wszystkimi dostępnymi strefami dostępności.</span><span class="sxs-lookup"><span data-stu-id="f78ca-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="f78ca-128">Przykład 7: Tworzenie zapory z co najmniej dwoma publicznymi adresami IP</span><span class="sxs-lookup"><span data-stu-id="f78ca-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="f78ca-129">W tym przykładzie jest tworzona Zapora podłączona do sieci wirtualnej "VNET" z dwoma publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="f78ca-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="f78ca-130">Przykład 8: Tworzenie zapory, która umożliwia ruch MSSQL do określonej bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f78ca-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="f78ca-131">W tym przykładzie tworzona jest Zapora zezwalająca na ruch MSSQL na porcie standardowym 1433 na bazę danych SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="f78ca-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="f78ca-132">Przykład 9: Tworzenie zapory podłączonej do wirtualnego koncentratora</span><span class="sxs-lookup"><span data-stu-id="f78ca-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="f78ca-133">W tym przykładzie jest tworzona Zapora dołączona do wirtualnego centrum "vHub".</span><span class="sxs-lookup"><span data-stu-id="f78ca-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="f78ca-134">Do zapory zostanie dołączona $fp zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="f78ca-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="f78ca-135">Ta Zapora umożliwia/odrzuca ruch oparty na regułach wymienionych w zasadach zapory $fp.</span><span class="sxs-lookup"><span data-stu-id="f78ca-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="f78ca-136">Koncentrator wirtualny i Zapora powinny znajdować się w tym samym regionie.</span><span class="sxs-lookup"><span data-stu-id="f78ca-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="f78ca-137">Przykład 10: Tworzenie zapory przy użyciu konfiguracji whitelist analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="f78ca-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="f78ca-138">W tym przykładzie jest tworzona Zapora, która whitelist "www.microsoft.com" i "8.8.8.8" z analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="f78ca-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="f78ca-139">Przykład 11: Tworzenie zapory z dostosowanym ustawieniami zakresu prywatnego</span><span class="sxs-lookup"><span data-stu-id="f78ca-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="f78ca-140">W tym przykładzie jest tworzona Zapora, która traktuje "99.99.99.0/24" i "66.66.0.0/16" jako prywatne zakresy adresów IP, a nie powoduje, że ruch odchodzący do tych adresów</span><span class="sxs-lookup"><span data-stu-id="f78ca-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="f78ca-141">Przykład 12: Tworzenie zapory z podsiecią zarządzania i publicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="f78ca-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="f78ca-142">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f78ca-143">Ponieważ nie określono reguł, zapora blokuje cały ruch (zachowanie domyślne).</span><span class="sxs-lookup"><span data-stu-id="f78ca-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="f78ca-144">Zagrożenia procesor Intel będzie również uruchamiany w trybie domyślnym-alertu — co oznacza, że ruch złośliwy będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="f78ca-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="f78ca-145">Aby obsługiwać scenariusze "Wymuszone tunelowanie", ta zapora będzie korzystać z podsieci "AzureFirewallManagementSubnet" i publicznego adresu IP zarządzania dla ruchu związanego z zarządzaniem.</span><span class="sxs-lookup"><span data-stu-id="f78ca-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="f78ca-146">Przykład 13: Tworzenie zapory z zasadami zapory dołączonymi do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f78ca-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="f78ca-147">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f78ca-148">Reguły i analiza zagrożeń, które zostaną zastosowane do zapory, zostaną pobrane z zasad zapory</span><span class="sxs-lookup"><span data-stu-id="f78ca-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="f78ca-149">Przykład 14: Tworzenie zapory z serwerami proxy DNS i DNS</span><span class="sxs-lookup"><span data-stu-id="f78ca-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="f78ca-150">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f78ca-151">Serwer proxy DNS jest włączony dla tej zapory i są dostępne 2 serwery DNS.</span><span class="sxs-lookup"><span data-stu-id="f78ca-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="f78ca-152">Wymagane jest również skonfigurowanie serwera proxy DNS dla reguł sieciowych, jeśli istnieją jakieś reguły sieciowe z nazwami FQDN, wtedy serwer proxy DNS również będzie używany.</span><span class="sxs-lookup"><span data-stu-id="f78ca-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="f78ca-153">Przykład 15: Tworzenie zapory z wieloma adresami IP.</span><span class="sxs-lookup"><span data-stu-id="f78ca-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="f78ca-154">Zapora może być skojarzona z koncentratorem wirtualnym</span><span class="sxs-lookup"><span data-stu-id="f78ca-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -Sku AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="f78ca-155">W tym przykładzie jest tworzona Zapora podłączona do koncentratora wirtualnego "koncentrator" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f78ca-156">Zapora będzie przypisana 2 publiczne adresy IP, które są tworzone niejawnie.</span><span class="sxs-lookup"><span data-stu-id="f78ca-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="f78ca-157">16: Tworzenie zapory z opcją Zezwalaj na aktywną FTP.</span><span class="sxs-lookup"><span data-stu-id="f78ca-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="f78ca-158">W tym przykładzie jest tworzona Zapora z flagą Zezwalaj na aktywną FTP.</span><span class="sxs-lookup"><span data-stu-id="f78ca-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="f78ca-159">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f78ca-159">PARAMETERS</span></span>

### <span data-ttu-id="f78ca-160">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f78ca-160">-ApplicationRuleCollection</span></span>
<span data-ttu-id="f78ca-161">Określa kolekcje reguł aplikacji dla nowej zapory.</span><span class="sxs-lookup"><span data-stu-id="f78ca-161">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-162">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f78ca-162">-AsJob</span></span>
<span data-ttu-id="f78ca-163">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f78ca-163">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78ca-164">-DefaultProfile</span></span>
<span data-ttu-id="f78ca-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f78ca-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-166">-DnsProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f78ca-166">-DnsProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="f78ca-167">Wymaga funkcji proxy DNS dla nazw FQDN w regułach sieciowych.</span><span class="sxs-lookup"><span data-stu-id="f78ca-167">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-168">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="f78ca-168">-DnsServer</span></span>
<span data-ttu-id="f78ca-169">Lista serwerów DNS, które mają być używane do rozpoznawania nazw DNS</span><span class="sxs-lookup"><span data-stu-id="f78ca-169">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-170">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="f78ca-170">-EnableDnsProxy</span></span>
<span data-ttu-id="f78ca-171">Włącz serwer proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="f78ca-171">Enable DNS Proxy.</span></span> <span data-ttu-id="f78ca-172">Domyślnie jest on wyłączony.</span><span class="sxs-lookup"><span data-stu-id="f78ca-172">By default it is disabled.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-173">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="f78ca-173">-AllowActiveFTP</span></span>
<span data-ttu-id="f78ca-174">Zezwala na aktywną FTP na zaporze.</span><span class="sxs-lookup"><span data-stu-id="f78ca-174">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="f78ca-175">Domyślnie jest on wyłączony.</span><span class="sxs-lookup"><span data-stu-id="f78ca-175">By default it is disabled.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-176">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f78ca-176">-FirewallPolicyId</span></span>
<span data-ttu-id="f78ca-177">Zasady zapory podłączone do zapory</span><span class="sxs-lookup"><span data-stu-id="f78ca-177">The firewall policy attached to the firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-178">-Force</span><span class="sxs-lookup"><span data-stu-id="f78ca-178">-Force</span></span>
<span data-ttu-id="f78ca-179">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f78ca-179">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-180">-HubIPAddresses</span><span class="sxs-lookup"><span data-stu-id="f78ca-180">-HubIPAddresses</span></span>
<span data-ttu-id="f78ca-181">Adresy IP zapory podłączonej do wirtualnego koncentratora</span><span class="sxs-lookup"><span data-stu-id="f78ca-181">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-182">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f78ca-182">-Location</span></span>
<span data-ttu-id="f78ca-183">Określa region zapory.</span><span class="sxs-lookup"><span data-stu-id="f78ca-183">Specifies the region for the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-184">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f78ca-184">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="f78ca-185">Co najmniej jeden publiczny adres IP, który ma być używany do komunikacji z zarządzaniem.</span><span class="sxs-lookup"><span data-stu-id="f78ca-185">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="f78ca-186">Publiczne adresy IP muszą używać standardowej jednostki SKU i muszą należeć do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-186">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-187">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f78ca-187">-Name</span></span>
<span data-ttu-id="f78ca-188">Określa nazwę zapory systemu Azure, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f78ca-188">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-189">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f78ca-189">-NatRuleCollection</span></span>
<span data-ttu-id="f78ca-190">Lista AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="f78ca-190">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-191">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f78ca-191">-NetworkRuleCollection</span></span>
<span data-ttu-id="f78ca-192">Lista AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="f78ca-192">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-193">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="f78ca-193">-PrivateRange</span></span>
<span data-ttu-id="f78ca-194">Zakresy prywatnych adresów IP, do których nie można SNAT'ed ruchu</span><span class="sxs-lookup"><span data-stu-id="f78ca-194">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-195">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f78ca-195">-PublicIpAddress</span></span>
<span data-ttu-id="f78ca-196">Co najmniej jeden publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f78ca-196">One or more Public IP Addresses.</span></span> <span data-ttu-id="f78ca-197">Publiczne adresy IP muszą używać standardowej jednostki SKU i muszą należeć do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-197">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-198">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="f78ca-198">-PublicIpName</span></span>
<span data-ttu-id="f78ca-199">Publiczna nazwa IP.</span><span class="sxs-lookup"><span data-stu-id="f78ca-199">Public Ip Name.</span></span> <span data-ttu-id="f78ca-200">Publiczny adres IP musi korzystać ze standardowej jednostki SKU i należy do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-200">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-201">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f78ca-201">-ResourceGroupName</span></span>
<span data-ttu-id="f78ca-202">Określa nazwę grupy zasobów, która ma zawierać zaporę.</span><span class="sxs-lookup"><span data-stu-id="f78ca-202">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-203">-SKU</span><span class="sxs-lookup"><span data-stu-id="f78ca-203">-Sku</span></span>
<span data-ttu-id="f78ca-204">Typ SKU dla zapory</span><span class="sxs-lookup"><span data-stu-id="f78ca-204">The sku type for firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="f78ca-205">-Tag</span></span>
<span data-ttu-id="f78ca-206">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f78ca-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f78ca-207">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="f78ca-207">For example:</span></span>

<span data-ttu-id="f78ca-208">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f78ca-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="f78ca-209">-ThreatIntelMode</span></span>
<span data-ttu-id="f78ca-210">Określa tryb działania dla analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="f78ca-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="f78ca-211">Tryb domyślny to alarm, a nie wył.</span><span class="sxs-lookup"><span data-stu-id="f78ca-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="f78ca-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="f78ca-213">Whitelist dla analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="f78ca-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="f78ca-214">-VirtualHubId</span></span>
<span data-ttu-id="f78ca-215">Wirtualny koncentrator, do którego jest dołączona Zapora</span><span class="sxs-lookup"><span data-stu-id="f78ca-215">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f78ca-216">-VirtualNetwork</span></span>
<span data-ttu-id="f78ca-217">Sieć wirtualna</span><span class="sxs-lookup"><span data-stu-id="f78ca-217">Virtual Network</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f78ca-218">-VirtualNetworkName</span></span>
<span data-ttu-id="f78ca-219">Określa nazwę sieci wirtualnej, dla której będzie wdrażana Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="f78ca-220">Sieć wirtualna i Zapora muszą należeć do tej samej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f78ca-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="f78ca-221">-Zone</span></span>
<span data-ttu-id="f78ca-222">Lista stref dostępności oznaczająca lokalizację, z której ma się pochodzić Zapora.</span><span class="sxs-lookup"><span data-stu-id="f78ca-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-223">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f78ca-223">-Confirm</span></span>
<span data-ttu-id="f78ca-224">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f78ca-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f78ca-225">-WhatIf</span></span>
<span data-ttu-id="f78ca-226">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f78ca-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f78ca-227">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f78ca-227">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f78ca-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78ca-228">CommonParameters</span></span>
<span data-ttu-id="f78ca-229">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78ca-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78ca-230">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f78ca-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78ca-231">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f78ca-231">INPUTS</span></span>

### <span data-ttu-id="f78ca-232">System. String</span><span class="sxs-lookup"><span data-stu-id="f78ca-232">System.String</span></span>

### <span data-ttu-id="f78ca-233">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f78ca-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="f78ca-234">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="f78ca-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="f78ca-235">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f78ca-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="f78ca-236">Microsoft. Azure. Commands. Network. models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="f78ca-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="f78ca-237">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="f78ca-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="f78ca-238">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="f78ca-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="f78ca-239">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f78ca-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f78ca-240">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f78ca-240">OUTPUTS</span></span>

### <span data-ttu-id="f78ca-241">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f78ca-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f78ca-242">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f78ca-242">NOTES</span></span>

## <span data-ttu-id="f78ca-243">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f78ca-243">RELATED LINKS</span></span>

[<span data-ttu-id="f78ca-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f78ca-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="f78ca-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f78ca-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="f78ca-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f78ca-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="f78ca-247">Nowe — AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f78ca-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="f78ca-248">Nowe — AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f78ca-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="f78ca-249">Nowe — AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f78ca-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
