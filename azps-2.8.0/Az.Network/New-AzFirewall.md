---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869948"
---
# <span data-ttu-id="0f639-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0f639-101">New-AzFirewall</span></span>

## <span data-ttu-id="0f639-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f639-102">SYNOPSIS</span></span>
<span data-ttu-id="0f639-103">Tworzy nową zaporę w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f639-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="0f639-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f639-104">SYNTAX</span></span>

### <span data-ttu-id="0f639-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0f639-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f639-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="0f639-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f639-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="0f639-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f639-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0f639-108">DESCRIPTION</span></span>
<span data-ttu-id="0f639-109">Polecenie cmdlet **New-AzFirewall** umożliwia utworzenie zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0f639-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="0f639-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f639-110">EXAMPLES</span></span>

### <span data-ttu-id="0f639-111">1: Tworzenie zapory dołączonej do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0f639-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="0f639-112">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="0f639-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="0f639-113">Ponieważ nie określono reguł, zapora blokuje cały ruch (zachowanie domyślne).</span><span class="sxs-lookup"><span data-stu-id="0f639-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="0f639-114">Zagrożenia procesor Intel będzie również uruchamiany w trybie domyślnym-alertu — co oznacza, że ruch złośliwy będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="0f639-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="0f639-115">2: Tworzenie zapory umożliwiającej cały ruch HTTPS</span><span class="sxs-lookup"><span data-stu-id="0f639-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="0f639-116">W tym przykładzie jest tworzona Zapora umożliwiająca wszystkim ruch HTTPS na porcie 443.</span><span class="sxs-lookup"><span data-stu-id="0f639-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="0f639-117">Działanie zagrożeń usługa Intel zostanie uruchomiona w trybie domyślnym-alertu — co oznacza, że złośliwy ruch będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="0f639-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="0f639-118">3: DNAT — Przekieruj ruch przeznaczony do 10.1.2.3:80 do 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="0f639-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="0f639-119">W tym przykładzie utworzono zaporę, która przetłumaczy docelowy adres IP i port wszystkich pakietów wysłanych do 10.1.2.3:80 do 10.2.3.4:8080 Threat Intel jest wyłączona w tym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="0f639-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="0f639-120">4: Tworzenie zapory bez reguł i zagrożeń z procesorem Intel w trybie alertu</span><span class="sxs-lookup"><span data-stu-id="0f639-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="0f639-121">W tym przykładzie jest tworzona Zapora, która blokuje cały ruch (zachowanie domyślne) i ma zagrożenia Intel działa w trybie alarmowym.</span><span class="sxs-lookup"><span data-stu-id="0f639-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="0f639-122">Oznacza to, że dzienniki alertów są wysyłane w celu uzyskania szkodliwego ruchu przed zastosowaniem innych reguł (w tym przypadku tylko reguła domyślna — Odmów wszystkich)</span><span class="sxs-lookup"><span data-stu-id="0f639-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="0f639-123">5: Tworzenie zapory, która zezwala na cały ruch HTTP na porcie 8080, ale blokuje szkodliwe domeny zidentyfikowane przez zagrożenie Intel</span><span class="sxs-lookup"><span data-stu-id="0f639-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="0f639-124">W tym przykładzie tworzona jest Zapora zezwalająca na cały ruch HTTP na porcie 8080, chyba że zostanie uznany za szkodliwy przez środowisko Intel.</span><span class="sxs-lookup"><span data-stu-id="0f639-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="0f639-125">W przypadku uruchamiania w trybie odmowy, w przeciwieństwie do alertu, ruch uważany za szkodliwy przez środowisko Intel nie jest rejestrowany, ale również zablokowany.</span><span class="sxs-lookup"><span data-stu-id="0f639-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="0f639-126">6: Tworzenie zapory bez reguł i stref dostępności</span><span class="sxs-lookup"><span data-stu-id="0f639-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="0f639-127">W tym przykładzie jest tworzona Zapora ze wszystkimi dostępnymi strefami dostępności.</span><span class="sxs-lookup"><span data-stu-id="0f639-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="0f639-128">7: Tworzenie zapory z co najmniej dwoma publicznymi adresami IP</span><span class="sxs-lookup"><span data-stu-id="0f639-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="0f639-129">W tym przykładzie jest tworzona Zapora podłączona do sieci wirtualnej "VNET" z dwoma publicznymi adresami IP.</span><span class="sxs-lookup"><span data-stu-id="0f639-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="0f639-130">8: Tworzenie zapory, która umożliwia ruch MSSQL do określonej bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0f639-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="0f639-131">W tym przykładzie tworzona jest Zapora zezwalająca na ruch MSSQL na porcie standardowym 1433 na bazę danych SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="0f639-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="0f639-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f639-132">PARAMETERS</span></span>

### <span data-ttu-id="0f639-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0f639-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="0f639-134">Określa kolekcje reguł aplikacji dla nowej zapory.</span><span class="sxs-lookup"><span data-stu-id="0f639-134">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="0f639-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f639-135">-AsJob</span></span>
<span data-ttu-id="0f639-136">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0f639-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f639-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f639-137">-DefaultProfile</span></span>
<span data-ttu-id="0f639-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f639-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f639-139">-Force</span><span class="sxs-lookup"><span data-stu-id="0f639-139">-Force</span></span>
<span data-ttu-id="0f639-140">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0f639-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f639-141">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0f639-141">-Location</span></span>
<span data-ttu-id="0f639-142">Określa region zapory.</span><span class="sxs-lookup"><span data-stu-id="0f639-142">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="0f639-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0f639-143">-Name</span></span>
<span data-ttu-id="0f639-144">Określa nazwę zapory systemu Azure, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f639-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0f639-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0f639-145">-NatRuleCollection</span></span>
<span data-ttu-id="0f639-146">Lista AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="0f639-146">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="0f639-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0f639-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="0f639-148">Lista AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="0f639-148">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="0f639-149">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0f639-149">-PublicIpAddress</span></span>
<span data-ttu-id="0f639-150">Co najmniej jeden publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="0f639-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="0f639-151">Publiczne adresy IP muszą używać standardowej jednostki SKU i muszą należeć do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="0f639-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="0f639-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="0f639-152">-PublicIpName</span></span>
<span data-ttu-id="0f639-153">Publiczna nazwa IP.</span><span class="sxs-lookup"><span data-stu-id="0f639-153">Public Ip Name.</span></span> <span data-ttu-id="0f639-154">Publiczny adres IP musi korzystać ze standardowej jednostki SKU i należy do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="0f639-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="0f639-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f639-155">-ResourceGroupName</span></span>
<span data-ttu-id="0f639-156">Określa nazwę grupy zasobów, która ma zawierać zaporę.</span><span class="sxs-lookup"><span data-stu-id="0f639-156">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="0f639-157">-Zone</span><span class="sxs-lookup"><span data-stu-id="0f639-157">-Zone</span></span>
<span data-ttu-id="0f639-158">Lista stref dostępności oznaczająca lokalizację, z której ma się pochodzić Zapora.</span><span class="sxs-lookup"><span data-stu-id="0f639-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="0f639-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f639-159">-Tag</span></span>
<span data-ttu-id="0f639-160">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0f639-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0f639-161">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="0f639-161">For example:</span></span>

<span data-ttu-id="0f639-162">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="0f639-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0f639-163">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="0f639-163">-ThreatIntelMode</span></span>
<span data-ttu-id="0f639-164">Określa tryb działania dla analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="0f639-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="0f639-165">Tryb domyślny to alarm, a nie wył.</span><span class="sxs-lookup"><span data-stu-id="0f639-165">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="0f639-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0f639-166">-VirtualNetwork</span></span>
<span data-ttu-id="0f639-167">Sieć wirtualna</span><span class="sxs-lookup"><span data-stu-id="0f639-167">Virtual Network</span></span>

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

### <span data-ttu-id="0f639-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0f639-168">-VirtualNetworkName</span></span>
<span data-ttu-id="0f639-169">Określa nazwę sieci wirtualnej, dla której będzie wdrażana Zapora.</span><span class="sxs-lookup"><span data-stu-id="0f639-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="0f639-170">Sieć wirtualna i Zapora muszą należeć do tej samej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f639-170">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="0f639-171">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f639-171">-Confirm</span></span>
<span data-ttu-id="0f639-172">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f639-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f639-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f639-173">-WhatIf</span></span>
<span data-ttu-id="0f639-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f639-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f639-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0f639-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f639-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f639-176">CommonParameters</span></span>
<span data-ttu-id="0f639-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f639-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f639-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f639-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f639-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f639-179">INPUTS</span></span>

### <span data-ttu-id="0f639-180">System. String</span><span class="sxs-lookup"><span data-stu-id="0f639-180">System.String</span></span>

### <span data-ttu-id="0f639-181">Microsoft. Azure. Commands. Network. models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0f639-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="0f639-182">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="0f639-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="0f639-183">Microsoft. Azure. Commands. Network. models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="0f639-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="0f639-184">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="0f639-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="0f639-185">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="0f639-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="0f639-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0f639-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0f639-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f639-187">OUTPUTS</span></span>

### <span data-ttu-id="0f639-188">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="0f639-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="0f639-189">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f639-189">NOTES</span></span>

## <span data-ttu-id="0f639-190">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f639-190">RELATED LINKS</span></span>

[<span data-ttu-id="0f639-191">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0f639-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="0f639-192">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0f639-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="0f639-193">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0f639-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="0f639-194">Nowe — AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0f639-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="0f639-195">Nowe — AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0f639-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="0f639-196">Nowe — AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="0f639-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
