---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553511"
---
# <span data-ttu-id="74232-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="74232-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="74232-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74232-102">SYNOPSIS</span></span>
<span data-ttu-id="74232-103">Tworzy nową zaporę w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="74232-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74232-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74232-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74232-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74232-105">DESCRIPTION</span></span>
<span data-ttu-id="74232-106">Polecenie cmdlet **New-AzureRmFirewall** umożliwia utworzenie zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="74232-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="74232-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74232-107">EXAMPLES</span></span>

### <span data-ttu-id="74232-108">1: Tworzenie zapory dołączonej do sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="74232-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="74232-109">W tym przykładzie jest tworzona Zapora dołączona do sieci wirtualnej "VNET" w tej samej grupie zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="74232-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="74232-110">Ponieważ nie określono reguł, zapora blokuje cały ruch (zachowanie domyślne).</span><span class="sxs-lookup"><span data-stu-id="74232-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="74232-111">2: Tworzenie zapory umożliwiającej cały ruch HTTPS</span><span class="sxs-lookup"><span data-stu-id="74232-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="74232-112">W tym przykładzie jest tworzona Zapora umożliwiająca wszystkim ruch HTTPS na porcie 443.</span><span class="sxs-lookup"><span data-stu-id="74232-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="74232-113">3: DNAT — Przekieruj ruch przeznaczony do 10.1.2.3:80 do 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="74232-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="74232-114">W tym przykładzie utworzono zaporę, która przetłumaczy docelowy adres IP i port wszystkich pakietów wysłanych do 10.1.2.3:80 do 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="74232-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="74232-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74232-115">PARAMETERS</span></span>

### <span data-ttu-id="74232-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="74232-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="74232-117">Określa kolekcje reguł aplikacji dla nowej zapory.</span><span class="sxs-lookup"><span data-stu-id="74232-117">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74232-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74232-118">-AsJob</span></span>
<span data-ttu-id="74232-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="74232-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74232-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74232-120">-DefaultProfile</span></span>
<span data-ttu-id="74232-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74232-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74232-122">-Force</span><span class="sxs-lookup"><span data-stu-id="74232-122">-Force</span></span>
<span data-ttu-id="74232-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="74232-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74232-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="74232-124">-Location</span></span>
<span data-ttu-id="74232-125">Określa region zapory.</span><span class="sxs-lookup"><span data-stu-id="74232-125">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="74232-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74232-126">-Name</span></span>
<span data-ttu-id="74232-127">Określa nazwę zapory systemu Azure, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74232-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="74232-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="74232-128">-NatRuleCollection</span></span>
<span data-ttu-id="74232-129">Lista AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="74232-129">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74232-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="74232-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="74232-131">Lista AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="74232-131">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74232-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="74232-132">-PublicIpName</span></span>
<span data-ttu-id="74232-133">Publiczna nazwa IP.</span><span class="sxs-lookup"><span data-stu-id="74232-133">Public Ip Name.</span></span> <span data-ttu-id="74232-134">Publiczny adres IP musi korzystać ze standardowej jednostki SKU i należy do tej samej grupy zasobów co Zapora.</span><span class="sxs-lookup"><span data-stu-id="74232-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="74232-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74232-135">-ResourceGroupName</span></span>
<span data-ttu-id="74232-136">Określa nazwę grupy zasobów, która ma zawierać zaporę.</span><span class="sxs-lookup"><span data-stu-id="74232-136">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="74232-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="74232-137">-Tag</span></span>
<span data-ttu-id="74232-138">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="74232-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="74232-139">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="74232-139">For example:</span></span>

<span data-ttu-id="74232-140">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="74232-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="74232-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="74232-141">-VirtualNetworkName</span></span>
<span data-ttu-id="74232-142">Określa nazwę sieci wirtualnej, dla której będzie wdrażana Zapora.</span><span class="sxs-lookup"><span data-stu-id="74232-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="74232-143">Sieć wirtualna i Zapora muszą należeć do tej samej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74232-143">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="74232-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74232-144">-Confirm</span></span>
<span data-ttu-id="74232-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74232-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74232-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74232-146">-WhatIf</span></span>
<span data-ttu-id="74232-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74232-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74232-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74232-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74232-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74232-149">CommonParameters</span></span>
<span data-ttu-id="74232-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74232-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74232-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74232-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74232-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74232-152">INPUTS</span></span>

### <span data-ttu-id="74232-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="74232-153">None</span></span>
<span data-ttu-id="74232-154">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="74232-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74232-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74232-155">OUTPUTS</span></span>

### <span data-ttu-id="74232-156">Microsoft. Azure. Commands. Network. models. PSFirewall</span><span class="sxs-lookup"><span data-stu-id="74232-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="74232-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74232-157">NOTES</span></span>

## <span data-ttu-id="74232-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74232-158">RELATED LINKS</span></span>

[<span data-ttu-id="74232-159">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="74232-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="74232-160">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="74232-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="74232-161">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="74232-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="74232-162">Nowe — AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="74232-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="74232-163">Nowe — AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="74232-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="74232-164">Nowe — AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="74232-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
