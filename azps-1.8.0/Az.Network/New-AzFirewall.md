---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709311"
---
# <span data-ttu-id="f12a3-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f12a3-101">New-AzFirewall</span></span>

## <span data-ttu-id="f12a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f12a3-102">SYNOPSIS</span></span>
<span data-ttu-id="f12a3-103">Tworzy nową zaporę w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f12a3-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="f12a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f12a3-104">SYNTAX</span></span>

### <span data-ttu-id="f12a3-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f12a3-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f12a3-106">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="f12a3-106">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f12a3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f12a3-107">DESCRIPTION</span></span>
<span data-ttu-id="f12a3-108">Polecenie cmdlet **New-AzFirewall** umożliwia utworzenie zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f12a3-108">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="f12a3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f12a3-109">EXAMPLES</span></span>

### <span data-ttu-id="f12a3-110">1: Tworzenie zapory dołączonej do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f12a3-110">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="f12a3-111">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f12a3-111">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="f12a3-112">Ponieważ nie określono reguł, zapora blokuje cały ruch (zachowanie domyślne).</span><span class="sxs-lookup"><span data-stu-id="f12a3-112">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="f12a3-113">Zagrożenia procesor Intel będzie również uruchamiany w trybie domyślnym-alertu — co oznacza, że ruch złośliwy będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="f12a3-113">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="f12a3-114">2: Tworzenie zapory umożliwiającej cały ruch HTTPS</span><span class="sxs-lookup"><span data-stu-id="f12a3-114">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="f12a3-115">W tym przykładzie jest tworzona Zapora umożliwiająca wszystkim ruch HTTPS na porcie 443.</span><span class="sxs-lookup"><span data-stu-id="f12a3-115">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="f12a3-116">Działanie zagrożeń usługa Intel zostanie uruchomiona w trybie domyślnym-alertu — co oznacza, że złośliwy ruch będzie rejestrowany, ale nie zostanie odmówiony.</span><span class="sxs-lookup"><span data-stu-id="f12a3-116">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="f12a3-117">3: DNAT — Przekieruj ruch przeznaczony do 10.1.2.3:80 do 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="f12a3-117">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="f12a3-118">W tym przykładzie utworzono zaporę, która przetłumaczy docelowy adres IP i port wszystkich pakietów wysłanych do 10.1.2.3:80 do 10.2.3.4:8080 Threat Intel jest wyłączona w tym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="f12a3-118">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="f12a3-119">4: Tworzenie zapory bez reguł i zagrożeń z procesorem Intel w trybie alertu</span><span class="sxs-lookup"><span data-stu-id="f12a3-119">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

<span data-ttu-id="f12a3-120">W tym przykładzie jest tworzona Zapora, która blokuje cały ruch (zachowanie domyślne) i ma zagrożenia Intel działa w trybie alarmowym.</span><span class="sxs-lookup"><span data-stu-id="f12a3-120">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="f12a3-121">Oznacza to, że dzienniki alertów są wysyłane w celu uzyskania szkodliwego ruchu przed zastosowaniem innych reguł (w tym przypadku tylko reguła domyślna — Odmów wszystkich)</span><span class="sxs-lookup"><span data-stu-id="f12a3-121">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="f12a3-122">5: Tworzenie zapory, która zezwala na cały ruch HTTP na porcie 8080, ale blokuje szkodliwe domeny zidentyfikowane przez zagrożenie Intel</span><span class="sxs-lookup"><span data-stu-id="f12a3-122">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="f12a3-123">W tym przykładzie tworzona jest Zapora zezwalająca na cały ruch HTTP na porcie 8080, chyba że zostanie uznany za szkodliwy przez środowisko Intel.</span><span class="sxs-lookup"><span data-stu-id="f12a3-123">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="f12a3-124">W przypadku uruchamiania w trybie odmowy, w przeciwieństwie do alertu, ruch uważany za szkodliwy przez środowisko Intel nie jest rejestrowany, ale również zablokowany.</span><span class="sxs-lookup"><span data-stu-id="f12a3-124">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

## <span data-ttu-id="f12a3-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f12a3-125">PARAMETERS</span></span>

### <span data-ttu-id="f12a3-126">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f12a3-126">-ApplicationRuleCollection</span></span>
<span data-ttu-id="f12a3-127">Określa kolekcje reguł aplikacji dla nowej zapory.</span><span class="sxs-lookup"><span data-stu-id="f12a3-127">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="f12a3-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f12a3-128">-AsJob</span></span>
<span data-ttu-id="f12a3-129">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f12a3-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f12a3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f12a3-130">-DefaultProfile</span></span>
<span data-ttu-id="f12a3-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f12a3-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f12a3-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f12a3-132">-Force</span></span>
<span data-ttu-id="f12a3-133">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f12a3-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f12a3-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f12a3-134">-Location</span></span>
<span data-ttu-id="f12a3-135">Określa region zapory.</span><span class="sxs-lookup"><span data-stu-id="f12a3-135">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="f12a3-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f12a3-136">-Name</span></span>
<span data-ttu-id="f12a3-137">Określa nazwę zapory systemu Azure, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f12a3-137">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f12a3-138">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f12a3-138">-NatRuleCollection</span></span>
<span data-ttu-id="f12a3-139">Lista AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="f12a3-139">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="f12a3-140">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f12a3-140">-NetworkRuleCollection</span></span>
<span data-ttu-id="f12a3-141">Lista AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="f12a3-141">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="f12a3-142">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="f12a3-142">-PublicIpName</span></span>
<span data-ttu-id="f12a3-143">Publiczna nazwa IP.</span><span class="sxs-lookup"><span data-stu-id="f12a3-143">Public Ip Name.</span></span> <span data-ttu-id="f12a3-144">Publiczny adres IP musi korzystać ze standardowej jednostki SKU i należy do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="f12a3-144">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f12a3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f12a3-145">-ResourceGroupName</span></span>
<span data-ttu-id="f12a3-146">Określa nazwę grupy zasobów, która ma zawierać zaporę.</span><span class="sxs-lookup"><span data-stu-id="f12a3-146">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="f12a3-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="f12a3-147">-Tag</span></span>
<span data-ttu-id="f12a3-148">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f12a3-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f12a3-149">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="f12a3-149">For example:</span></span>

<span data-ttu-id="f12a3-150">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f12a3-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f12a3-151">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="f12a3-151">-ThreatIntelMode</span></span>
<span data-ttu-id="f12a3-152">Określa tryb działania dla analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="f12a3-152">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="f12a3-153">Tryb domyślny to alarm, a nie wył.</span><span class="sxs-lookup"><span data-stu-id="f12a3-153">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f12a3-154">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f12a3-154">-VirtualNetworkName</span></span>
<span data-ttu-id="f12a3-155">Określa nazwę sieci wirtualnej, dla której będzie wdrażana Zapora.</span><span class="sxs-lookup"><span data-stu-id="f12a3-155">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="f12a3-156">Sieć wirtualna i Zapora muszą należeć do tej samej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f12a3-156">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f12a3-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f12a3-157">-Confirm</span></span>
<span data-ttu-id="f12a3-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f12a3-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f12a3-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f12a3-159">-WhatIf</span></span>
<span data-ttu-id="f12a3-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f12a3-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f12a3-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f12a3-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f12a3-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f12a3-162">CommonParameters</span></span>
<span data-ttu-id="f12a3-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f12a3-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f12a3-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f12a3-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f12a3-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f12a3-165">INPUTS</span></span>

### <span data-ttu-id="f12a3-166">System. String</span><span class="sxs-lookup"><span data-stu-id="f12a3-166">System.String</span></span>

### <span data-ttu-id="f12a3-167">Microsoft. Azure. Commands. Network. models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="f12a3-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="f12a3-168">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="f12a3-168">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="f12a3-169">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="f12a3-169">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="f12a3-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f12a3-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f12a3-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f12a3-171">OUTPUTS</span></span>

### <span data-ttu-id="f12a3-172">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f12a3-172">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f12a3-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f12a3-173">NOTES</span></span>

## <span data-ttu-id="f12a3-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f12a3-174">RELATED LINKS</span></span>

[<span data-ttu-id="f12a3-175">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f12a3-175">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="f12a3-176">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f12a3-176">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="f12a3-177">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f12a3-177">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="f12a3-178">Nowe — AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f12a3-178">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="f12a3-179">Nowe — AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f12a3-179">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="f12a3-180">Nowe — AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f12a3-180">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
