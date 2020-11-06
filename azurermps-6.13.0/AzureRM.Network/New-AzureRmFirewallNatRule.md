---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547463"
---
# <span data-ttu-id="7d6f9-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="7d6f9-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="7d6f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6f9-103">Tworzy regułę NAT dla zapory.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d6f9-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6f9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d6f9-105">DESCRIPTION</span></span>
<span data-ttu-id="7d6f9-106">Polecenie cmdlet **New-AzureRmFirewallNatRule** umożliwia utworzenie reguły NAT dla zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="7d6f9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d6f9-107">EXAMPLES</span></span>

### <span data-ttu-id="7d6f9-108">1: Utwórz regułę DNAT całego ruchu TCP z adresu 10.0.0.0/24 z docelowym 10.1.2.3:80 do lokalizacji docelowej 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="7d6f9-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="7d6f9-109">W tym przykładzie jest tworzona reguła, która będzie DNAT cały ruch pochodzący z adresu 10.0.0.0/24 z docelowym 10.1.2.3:80 do 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="7d6f9-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="7d6f9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d6f9-110">PARAMETERS</span></span>

### <span data-ttu-id="7d6f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6f9-111">-DefaultProfile</span></span>
<span data-ttu-id="7d6f9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f9-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="7d6f9-113">-Description</span></span>
<span data-ttu-id="7d6f9-114">Umożliwia określenie opcjonalnego opisu tej reguły.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-114">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f9-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7d6f9-115">-DestinationAddress</span></span>
<span data-ttu-id="7d6f9-116">Adresy docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-116">The destination addresses of the rule.</span></span>

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

### <span data-ttu-id="7d6f9-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7d6f9-117">-DestinationPort</span></span>
<span data-ttu-id="7d6f9-118">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="7d6f9-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="7d6f9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d6f9-119">-Name</span></span>
<span data-ttu-id="7d6f9-120">Określa nazwę tej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="7d6f9-121">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-121">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f9-122">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="7d6f9-122">-Protocol</span></span>
<span data-ttu-id="7d6f9-123">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="7d6f9-124">Obsługiwane protokoły to TCP i UDP.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="7d6f9-125">Dozwolona jest specjalna wartość "any", co oznacza, że jest zgodna z portami TCP i UDP, ale nie innymi protokołami.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f9-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="7d6f9-126">-SourceAddress</span></span>
<span data-ttu-id="7d6f9-127">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="7d6f9-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="7d6f9-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="7d6f9-128">-TranslatedAddress</span></span>
<span data-ttu-id="7d6f9-129">Określa żądany wynik translacji adresów</span><span class="sxs-lookup"><span data-stu-id="7d6f9-129">Specifies the desired result of the address translation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f9-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="7d6f9-130">-TranslatedPort</span></span>
<span data-ttu-id="7d6f9-131">Określa wymagany wynik translacji portów.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-131">Specifies the desired result of the port translation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d6f9-132">-Confirm</span></span>
<span data-ttu-id="7d6f9-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d6f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6f9-134">-WhatIf</span></span>
<span data-ttu-id="7d6f9-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6f9-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d6f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6f9-137">CommonParameters</span></span>
<span data-ttu-id="7d6f9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6f9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6f9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6f9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d6f9-140">INPUTS</span></span>

### <span data-ttu-id="7d6f9-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7d6f9-141">None</span></span>
<span data-ttu-id="7d6f9-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7d6f9-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d6f9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d6f9-143">OUTPUTS</span></span>

### <span data-ttu-id="7d6f9-144">Microsoft. Azure. Commands. Network. models. PSFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="7d6f9-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="7d6f9-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d6f9-145">NOTES</span></span>

## <span data-ttu-id="7d6f9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d6f9-146">RELATED LINKS</span></span>

[<span data-ttu-id="7d6f9-147">Nowe — AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="7d6f9-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="7d6f9-148">Nowe — AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="7d6f9-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="7d6f9-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="7d6f9-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
