---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541688"
---
# <span data-ttu-id="e4daa-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e4daa-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="e4daa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4daa-102">SYNOPSIS</span></span>
<span data-ttu-id="e4daa-103">Tworzy regułę sieciową zapory.</span><span class="sxs-lookup"><span data-stu-id="e4daa-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4daa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4daa-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4daa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4daa-105">DESCRIPTION</span></span>
<span data-ttu-id="e4daa-106">Polecenie cmdlet **New-AzureRmFirewallNetworkRule** tworzy regułę sieciową dla zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e4daa-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="e4daa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4daa-107">EXAMPLES</span></span>

### <span data-ttu-id="e4daa-108">1: Tworzenie reguły dla całego ruchu TCP</span><span class="sxs-lookup"><span data-stu-id="e4daa-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="e4daa-109">W tym przykładzie tworzona jest reguła dla całego ruchu TCP.</span><span class="sxs-lookup"><span data-stu-id="e4daa-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="e4daa-110">Użytkownik wymusza, czy ruch będzie dozwolony lub odmówiony dla reguły na podstawie kolekcji reguł, z którą jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="e4daa-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="e4daa-111">2: Tworzenie reguły dla całego ruchu TCP od 10.0.0.0 do 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="e4daa-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="e4daa-112">W tym przykładzie tworzona jest reguła dla całego ruchu TCP z 10.0.0.0 na 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="e4daa-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="e4daa-113">Użytkownik wymusza, czy ruch będzie dozwolony lub odmówiony dla reguły na podstawie kolekcji reguł, z którą jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="e4daa-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="e4daa-114">3: Tworzenie reguły dla całego ruchu TCP i ICMP z dowolnego źródła do 10.0.0.0/16</span><span class="sxs-lookup"><span data-stu-id="e4daa-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="e4daa-115">W tym przykładzie tworzona jest reguła dla całego ruchu TCP z 10.0.0.0 na 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="e4daa-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="e4daa-116">Użytkownik wymusza, czy ruch będzie dozwolony lub odmówiony dla reguły na podstawie kolekcji reguł, z którą jest skojarzona.</span><span class="sxs-lookup"><span data-stu-id="e4daa-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="e4daa-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4daa-117">PARAMETERS</span></span>

### <span data-ttu-id="e4daa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4daa-118">-DefaultProfile</span></span>
<span data-ttu-id="e4daa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4daa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4daa-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="e4daa-120">-Description</span></span>
<span data-ttu-id="e4daa-121">Umożliwia określenie opcjonalnego opisu tej reguły.</span><span class="sxs-lookup"><span data-stu-id="e4daa-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4daa-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e4daa-122">-DestinationAddress</span></span>
<span data-ttu-id="e4daa-123">Adresy docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="e4daa-123">The destination addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4daa-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e4daa-124">-DestinationPort</span></span>
<span data-ttu-id="e4daa-125">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="e4daa-125">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4daa-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4daa-126">-Name</span></span>
<span data-ttu-id="e4daa-127">Określa nazwę reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="e4daa-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="e4daa-128">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="e4daa-128">The name must be unique inside a rule collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4daa-129">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="e4daa-129">-Protocol</span></span>
<span data-ttu-id="e4daa-130">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="e4daa-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="e4daa-131">Możliwe wartości to protokoły TCP, UDP, ICMP i any.</span><span class="sxs-lookup"><span data-stu-id="e4daa-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4daa-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e4daa-132">-SourceAddress</span></span>
<span data-ttu-id="e4daa-133">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="e4daa-133">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4daa-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4daa-134">-Confirm</span></span>
<span data-ttu-id="e4daa-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4daa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4daa-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4daa-136">-WhatIf</span></span>
<span data-ttu-id="e4daa-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4daa-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4daa-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4daa-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4daa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4daa-139">CommonParameters</span></span>
<span data-ttu-id="e4daa-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4daa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4daa-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4daa-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4daa-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4daa-142">INPUTS</span></span>

### <span data-ttu-id="e4daa-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e4daa-143">None</span></span>
<span data-ttu-id="e4daa-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e4daa-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4daa-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4daa-145">OUTPUTS</span></span>

### <span data-ttu-id="e4daa-146">Microsoft. Azure. Commands. Network. models. PSFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e4daa-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="e4daa-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4daa-147">NOTES</span></span>

## <span data-ttu-id="e4daa-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4daa-148">RELATED LINKS</span></span>

[<span data-ttu-id="e4daa-149">Nowe — AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e4daa-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="e4daa-150">Nowe — AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e4daa-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="e4daa-151">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e4daa-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
