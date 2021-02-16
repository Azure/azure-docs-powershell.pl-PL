---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 031c926d25fe55a9572fe12922ccee26b6371a2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179714"
---
# <span data-ttu-id="df7b0-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="df7b0-101">New-AzFirewall</span></span>

## <span data-ttu-id="df7b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df7b0-102">SYNOPSIS</span></span>
<span data-ttu-id="df7b0-103">Tworzy nową Zaporę w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="df7b0-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="df7b0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="df7b0-104">SYNTAX</span></span>

### <span data-ttu-id="df7b0-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="df7b0-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df7b0-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="df7b0-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df7b0-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="df7b0-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df7b0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="df7b0-108">DESCRIPTION</span></span>
<span data-ttu-id="df7b0-109">Polecenie **cmdlet New-AzFirewall** tworzy zaporę platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="df7b0-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="df7b0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="df7b0-110">EXAMPLES</span></span>

### <span data-ttu-id="df7b0-111">Przykład 1. Tworzenie zapory dołączonej do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="df7b0-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="df7b0-112">W tym przykładzie w tej samej grupie zasobów co zapora jest łączona zapora dołączona do sieci wirtualnej "vnet".</span><span class="sxs-lookup"><span data-stu-id="df7b0-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="df7b0-113">Ponieważ nie określono żadnych reguł, zapora blokuje cały ruch (zachowanie domyślne).</span><span class="sxs-lookup"><span data-stu-id="df7b0-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="df7b0-114">Firma Threat Intel będzie również działać w trybie domyślnym — ostrzegawczym — co oznacza, że złośliwy ruch zostanie zarejestrowany, ale nie odrzucony.</span><span class="sxs-lookup"><span data-stu-id="df7b0-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="df7b0-115">Przykład 2. Tworzenie zapory zezwala na cały ruch HTTPS</span><span class="sxs-lookup"><span data-stu-id="df7b0-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="df7b0-116">W tym przykładzie jest organizacji zapory, która zezwala na cały ruch HTTPS na porcie 443.</span><span class="sxs-lookup"><span data-stu-id="df7b0-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="df7b0-117">Narzędzie Threat Intel będzie działać w trybie domyślnym — alert — co oznacza, że złośliwy ruch zostanie zarejestrowany, ale nie odrzucony.</span><span class="sxs-lookup"><span data-stu-id="df7b0-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="df7b0-118">Przykład 3. ZESZYT — przekierowywanie ruchu do kodu 10.1.2.3:80 do 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="df7b0-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="df7b0-119">W tym przykładzie utworzono zaporę, która tłumaczyła docelowy adres IP i port wszystkich pakietów przeznaczonych do 10.1.2.3:80 na 10.2.3.4:8080 Threat Intel jest w tym przykładzie wyłączona.</span><span class="sxs-lookup"><span data-stu-id="df7b0-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="df7b0-120">Przykład 4. Tworzenie zapory bez reguł i zagrożenia dla firmy Intel w trybie alertu</span><span class="sxs-lookup"><span data-stu-id="df7b0-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="df7b0-121">W tym przykładzie jest łączona Zapora, która blokuje cały ruch (zachowanie domyślne) i uruchamia w trybie alertu technologię Threat Intel.</span><span class="sxs-lookup"><span data-stu-id="df7b0-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="df7b0-122">Oznacza to, że dzienniki alertów są pomijane dla złośliwego ruchu przed zastosowaniem innych reguł (w tym przypadku tylko reguła domyślna — Odmów wszystkim)</span><span class="sxs-lookup"><span data-stu-id="df7b0-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="df7b0-123">Przykład 5. Utworzenie Zapory zezwala na cały ruch HTTP w porcie 8080, ale blokuje złośliwe domeny zidentyfikowane przez firmę Intel podszywających się pod firmę Threat</span><span class="sxs-lookup"><span data-stu-id="df7b0-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="df7b0-124">W tym przykładzie jest żona Zapora, która zezwala na cały ruch HTTP na porcie 8080, o ile nie jest uznawana za złośliwą przez firmę Intel.</span><span class="sxs-lookup"><span data-stu-id="df7b0-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="df7b0-125">W trybie odmów (inaczej niż w przypadku alertów) ruch uznawany przez firmę Intel za złośliwy jest nie tylko rejestrowany, ale także blokowany.</span><span class="sxs-lookup"><span data-stu-id="df7b0-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="df7b0-126">Przykład 6. Tworzenie zapory bez reguł i stref dostępności</span><span class="sxs-lookup"><span data-stu-id="df7b0-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="df7b0-127">W tym przykładzie jest strefy zapory ze wszystkimi dostępnymi strefami dostępności.</span><span class="sxs-lookup"><span data-stu-id="df7b0-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="df7b0-128">Przykład 7. Tworzenie zapory z co najmniej dwoma publicznymi adresami IP</span><span class="sxs-lookup"><span data-stu-id="df7b0-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="df7b0-129">W tym przykładzie jest łączona zapora dołączona do sieci wirtualnej "vnet" z dwoma publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="df7b0-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="df7b0-130">Przykład 8. Tworzenie zapory, która zezwala na ruch w języku MSSQL do konkretnej bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="df7b0-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="df7b0-131">W tym przykładzie jest organizacji zapory, która zezwala na ruch MSSQL na standardowym porcie 1433 do bazy danych SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="df7b0-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="df7b0-132">Przykład 9. Tworzenie zapory dołączonej do centrum wirtualnego</span><span class="sxs-lookup"><span data-stu-id="df7b0-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="df7b0-133">W tym przykładzie jest łączona zapora do centrum wirtualnego "vHub".</span><span class="sxs-lookup"><span data-stu-id="df7b0-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="df7b0-134">Do zapory $fp zasady zapory.</span><span class="sxs-lookup"><span data-stu-id="df7b0-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="df7b0-135">Ta zapora zezwala na ruch/blokuje go na podstawie reguł wymienionych w zasadach zapory, które $fp.</span><span class="sxs-lookup"><span data-stu-id="df7b0-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="df7b0-136">Centrum wirtualne i zapora powinny być w tych samych regionach.</span><span class="sxs-lookup"><span data-stu-id="df7b0-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="df7b0-137">Przykład 10. Tworzenie zapory z konfiguracją listy whitelist w analizie zagrożeń</span><span class="sxs-lookup"><span data-stu-id="df7b0-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="df7b0-138">W tym przykładzie jest białą listę "www.microsoft.com" i "8.8.8.8" z analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="df7b0-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="df7b0-139">Przykład 11. Tworzenie zapory z dostosowaną konfiguracją zakresu prywatnego</span><span class="sxs-lookup"><span data-stu-id="df7b0-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="df7b0-140">W tym przykładzie jest 66.66.0.0/16", która traktuje "99.99.99.99.0/24" i "66.66.0.0/16" jako prywatne zakresy adresów IP i nie przekieruje ruchu na te adresy.</span><span class="sxs-lookup"><span data-stu-id="df7b0-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="df7b0-141">Przykład 12. Tworzenie zapory z podsiecią zarządzania i publicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="df7b0-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="df7b0-142">W tym przykładzie w tej samej grupie zasobów co zapora jest łączona zapora dołączona do sieci wirtualnej "vnet".</span><span class="sxs-lookup"><span data-stu-id="df7b0-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="df7b0-143">Ponieważ nie określono żadnych reguł, zapora blokuje cały ruch (zachowanie domyślne).</span><span class="sxs-lookup"><span data-stu-id="df7b0-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="df7b0-144">Firma Threat Intel będzie również działać w trybie domyślnym — ostrzegawczym — co oznacza, że złośliwy ruch zostanie zarejestrowany, ale nie odrzucony.</span><span class="sxs-lookup"><span data-stu-id="df7b0-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="df7b0-145">W celu obsługi scenariuszy "wymuszonego korkowania" zapora będzie używać podsieci "AzureFirewallManagementSubnet" i publicznego adresu IP zarządzania na rzecz swojego ruchu zarządzania</span><span class="sxs-lookup"><span data-stu-id="df7b0-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="df7b0-146">Przykład 13. Tworzenie zapory z zasadami zapory dołączonymi do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="df7b0-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="df7b0-147">W tym przykładzie w tej samej grupie zasobów co zapora jest łączona zapora dołączona do sieci wirtualnej "vnet".</span><span class="sxs-lookup"><span data-stu-id="df7b0-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="df7b0-148">Reguły i analizy zagrożeń stosowane do zapory są stosowane z zasad zapory</span><span class="sxs-lookup"><span data-stu-id="df7b0-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="df7b0-149">Przykład 14. Tworzenie zapory z serwerem proxy DNS i serwerami DNS</span><span class="sxs-lookup"><span data-stu-id="df7b0-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="df7b0-150">W tym przykładzie w tej samej grupie zasobów co zapora jest łączona zapora dołączona do sieci wirtualnej "vnet".</span><span class="sxs-lookup"><span data-stu-id="df7b0-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="df7b0-151">Dla tej zapory jest włączony serwer proxy DNS i są dostępne dwa serwery DNS.</span><span class="sxs-lookup"><span data-stu-id="df7b0-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="df7b0-152">Ustawienie wymagania serwera proxy DNS dla reguł sieciowych jest tak ustawione, aby w przypadku jakichkolwiek reguł sieciowych z nazwami FQNS także były używane serwery proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="df7b0-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="df7b0-153">Przykład 15. Tworzenie zapory z wieloma ip.</span><span class="sxs-lookup"><span data-stu-id="df7b0-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="df7b0-154">Zapora może być skojarzona z centrum wirtualnym</span><span class="sxs-lookup"><span data-stu-id="df7b0-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="df7b0-155">W tym przykładzie zapora jest łączona z "centrum wirtualnym" w tej samej grupie zasobów co zapora.</span><span class="sxs-lookup"><span data-stu-id="df7b0-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="df7b0-156">Zapora zostanie przypisana do 2 publicznych ip, które są tworzone niejawnie.</span><span class="sxs-lookup"><span data-stu-id="df7b0-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="df7b0-157">16. Tworzenie zapory z zezwalanie na aktywny protokół FTP.</span><span class="sxs-lookup"><span data-stu-id="df7b0-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="df7b0-158">W tym przykładzie jest aktywna zapora z aktywną flagą FTP.</span><span class="sxs-lookup"><span data-stu-id="df7b0-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="df7b0-159">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df7b0-159">PARAMETERS</span></span>

### <span data-ttu-id="df7b0-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="df7b0-160">-AllowActiveFTP</span></span>
<span data-ttu-id="df7b0-161">Zezwala na aktywne konto FTP w zaporze.</span><span class="sxs-lookup"><span data-stu-id="df7b0-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="df7b0-162">Domyślnie jest ona wyłączona.</span><span class="sxs-lookup"><span data-stu-id="df7b0-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="df7b0-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="df7b0-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="df7b0-164">Określa kolekcje reguł aplikacji dla nowej Zapory.</span><span class="sxs-lookup"><span data-stu-id="df7b0-164">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="df7b0-165">— AsJob</span><span class="sxs-lookup"><span data-stu-id="df7b0-165">-AsJob</span></span>
<span data-ttu-id="df7b0-166">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="df7b0-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df7b0-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7b0-167">-DefaultProfile</span></span>
<span data-ttu-id="df7b0-168">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="df7b0-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df7b0-169">- DnsServer</span><span class="sxs-lookup"><span data-stu-id="df7b0-169">-DnsServer</span></span>
<span data-ttu-id="df7b0-170">Lista serwerów DNS, które mają być używane do rozpoznawania nazw DNS,</span><span class="sxs-lookup"><span data-stu-id="df7b0-170">The list of DNS Servers to be used for DNS resolution,</span></span>

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

### <span data-ttu-id="df7b0-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="df7b0-171">-EnableDnsProxy</span></span>
<span data-ttu-id="df7b0-172">Włącz serwer proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="df7b0-172">Enable DNS Proxy.</span></span> <span data-ttu-id="df7b0-173">Domyślnie jest ona wyłączona.</span><span class="sxs-lookup"><span data-stu-id="df7b0-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="df7b0-174">- FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="df7b0-174">-FirewallPolicyId</span></span>
<span data-ttu-id="df7b0-175">Zasady zapory dołączone do zapory</span><span class="sxs-lookup"><span data-stu-id="df7b0-175">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="df7b0-176">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="df7b0-176">-Force</span></span>
<span data-ttu-id="df7b0-177">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="df7b0-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="df7b0-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="df7b0-178">-HubIPAddress</span></span>
<span data-ttu-id="df7b0-179">Adresy IP zapory dołączonej do centrum wirtualnego</span><span class="sxs-lookup"><span data-stu-id="df7b0-179">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7b0-180">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="df7b0-180">-Location</span></span>
<span data-ttu-id="df7b0-181">Określa region zapory.</span><span class="sxs-lookup"><span data-stu-id="df7b0-181">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="df7b0-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="df7b0-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="df7b0-183">Jeden lub więcej publicznych adresów IP, których należy użyć do zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="df7b0-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="df7b0-184">Publiczne adresy IP muszą używać standardowej wersji SKU i muszą należeć do tej samej grupy zasobów, co Zapora.</span><span class="sxs-lookup"><span data-stu-id="df7b0-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="df7b0-185">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="df7b0-185">-Name</span></span>
<span data-ttu-id="df7b0-186">Określa nazwę zapory platformy Azure, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7b0-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="df7b0-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="df7b0-187">-NatRuleCollection</span></span>
<span data-ttu-id="df7b0-188">Lista elementów AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="df7b0-188">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="df7b0-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="df7b0-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="df7b0-190">Lista elementów AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="df7b0-190">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="df7b0-191">- PrivateRange</span><span class="sxs-lookup"><span data-stu-id="df7b0-191">-PrivateRange</span></span>
<span data-ttu-id="df7b0-192">Prywatne zakresy adresów IP, do których nie zostanie przenoszony ruch</span><span class="sxs-lookup"><span data-stu-id="df7b0-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="df7b0-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="df7b0-193">-PublicIpAddress</span></span>
<span data-ttu-id="df7b0-194">Co najmniej jeden publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="df7b0-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="df7b0-195">Publiczne adresy IP muszą używać standardowej wersji SKU i muszą należeć do tej samej grupy zasobów, co Zapora.</span><span class="sxs-lookup"><span data-stu-id="df7b0-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="df7b0-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="df7b0-196">-PublicIpName</span></span>
<span data-ttu-id="df7b0-197">Nazwa publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="df7b0-197">Public Ip Name.</span></span> <span data-ttu-id="df7b0-198">Publiczny adres IP musi korzystać ze standardowej wersji SKU i musi należeć do tej samej grupy zasobów, co Zapora.</span><span class="sxs-lookup"><span data-stu-id="df7b0-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="df7b0-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7b0-199">-ResourceGroupName</span></span>
<span data-ttu-id="df7b0-200">Określa nazwę grupy zasobów, która ma zawierać Zaporę.</span><span class="sxs-lookup"><span data-stu-id="df7b0-200">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="df7b0-201">-SKUName</span><span class="sxs-lookup"><span data-stu-id="df7b0-201">-SkuName</span></span>
<span data-ttu-id="df7b0-202">Nazwa sKU zapory</span><span class="sxs-lookup"><span data-stu-id="df7b0-202">The sku name for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Sku
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7b0-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="df7b0-203">-SkuTier</span></span>
<span data-ttu-id="df7b0-204">Warstwa SKU dla zapory</span><span class="sxs-lookup"><span data-stu-id="df7b0-204">The sku tier for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7b0-205">— Tag</span><span class="sxs-lookup"><span data-stu-id="df7b0-205">-Tag</span></span>
<span data-ttu-id="df7b0-206">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="df7b0-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="df7b0-207">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="df7b0-207">For example:</span></span>

<span data-ttu-id="df7b0-208">@{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="df7b0-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="df7b0-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="df7b0-209">-ThreatIntelMode</span></span>
<span data-ttu-id="df7b0-210">Określa tryb działania analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="df7b0-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="df7b0-211">Tryb domyślny to Alert, a nie Wył.</span><span class="sxs-lookup"><span data-stu-id="df7b0-211">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="df7b0-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="df7b0-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="df7b0-213">Lista na liście na temat analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="df7b0-213">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="df7b0-214">- VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="df7b0-214">-VirtualHubId</span></span>
<span data-ttu-id="df7b0-215">Centrum wirtualne, do których jest podłączona zapora</span><span class="sxs-lookup"><span data-stu-id="df7b0-215">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="df7b0-216">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df7b0-216">-VirtualNetwork</span></span>
<span data-ttu-id="df7b0-217">Sieć wirtualna</span><span class="sxs-lookup"><span data-stu-id="df7b0-217">Virtual Network</span></span>

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

### <span data-ttu-id="df7b0-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="df7b0-218">-VirtualNetworkName</span></span>
<span data-ttu-id="df7b0-219">Określa nazwę sieci wirtualnej, dla której zostanie wdrożona Zapora.</span><span class="sxs-lookup"><span data-stu-id="df7b0-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="df7b0-220">Sieć wirtualna i Zapora muszą należeć do tej samej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df7b0-220">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="df7b0-221">— Strefa</span><span class="sxs-lookup"><span data-stu-id="df7b0-221">-Zone</span></span>
<span data-ttu-id="df7b0-222">Lista stref dostępności oznaczających, skąd musi pochodzić zapora.</span><span class="sxs-lookup"><span data-stu-id="df7b0-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="df7b0-223">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df7b0-223">-Confirm</span></span>
<span data-ttu-id="df7b0-224">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="df7b0-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df7b0-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7b0-225">-WhatIf</span></span>
<span data-ttu-id="df7b0-226">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7b0-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df7b0-227">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="df7b0-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df7b0-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7b0-228">CommonParameters</span></span>
<span data-ttu-id="df7b0-229">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7b0-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7b0-230">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df7b0-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7b0-231">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df7b0-231">INPUTS</span></span>

### <span data-ttu-id="df7b0-232">System.String</span><span class="sxs-lookup"><span data-stu-id="df7b0-232">System.String</span></span>

### <span data-ttu-id="df7b0-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df7b0-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="df7b0-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span><span class="sxs-lookup"><span data-stu-id="df7b0-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="df7b0-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="df7b0-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="df7b0-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="df7b0-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="df7b0-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="df7b0-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="df7b0-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="df7b0-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="df7b0-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="df7b0-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="df7b0-240">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df7b0-240">OUTPUTS</span></span>

### <span data-ttu-id="df7b0-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="df7b0-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="df7b0-242">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="df7b0-242">NOTES</span></span>

## <span data-ttu-id="df7b0-243">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df7b0-243">RELATED LINKS</span></span>

[<span data-ttu-id="df7b0-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="df7b0-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="df7b0-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="df7b0-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="df7b0-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="df7b0-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="df7b0-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="df7b0-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="df7b0-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="df7b0-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="df7b0-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="df7b0-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
