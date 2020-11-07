---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: c7519b6cf5f95f80a20f94bbae5ec097964bd01a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869944"
---
# <span data-ttu-id="f7f72-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="f7f72-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="f7f72-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7f72-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f72-103">Tworzy regułę NAT dla zapory.</span><span class="sxs-lookup"><span data-stu-id="f7f72-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="f7f72-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7f72-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f72-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7f72-105">DESCRIPTION</span></span>
<span data-ttu-id="f7f72-106">Polecenie cmdlet **New-AzFirewallNatRule** umożliwia utworzenie reguły NAT dla zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f72-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="f7f72-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7f72-107">EXAMPLES</span></span>

### <span data-ttu-id="f7f72-108">1: Utwórz regułę DNAT całego ruchu TCP z adresu 10.0.0.0/24 z docelowym 10.1.2.3:80 do lokalizacji docelowej 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="f7f72-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="f7f72-109">W tym przykładzie jest tworzona reguła, która będzie DNAT cały ruch pochodzący z adresu 10.0.0.0/24 z docelowym 10.1.2.3:80 do 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="f7f72-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="f7f72-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7f72-110">PARAMETERS</span></span>

### <span data-ttu-id="f7f72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f72-111">-DefaultProfile</span></span>
<span data-ttu-id="f7f72-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f72-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7f72-113">— Opis</span><span class="sxs-lookup"><span data-stu-id="f7f72-113">-Description</span></span>
<span data-ttu-id="f7f72-114">Umożliwia określenie opcjonalnego opisu tej reguły.</span><span class="sxs-lookup"><span data-stu-id="f7f72-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="f7f72-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f7f72-115">-DestinationAddress</span></span>
<span data-ttu-id="f7f72-116">Adresy docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="f7f72-116">The destination addresses of the rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f72-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f7f72-117">-DestinationPort</span></span>
<span data-ttu-id="f7f72-118">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="f7f72-118">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f72-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7f72-119">-Name</span></span>
<span data-ttu-id="f7f72-120">Określa nazwę tej reguły NAT.</span><span class="sxs-lookup"><span data-stu-id="f7f72-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="f7f72-121">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="f7f72-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="f7f72-122">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="f7f72-122">-Protocol</span></span>
<span data-ttu-id="f7f72-123">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="f7f72-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="f7f72-124">Obsługiwane protokoły to TCP i UDP.</span><span class="sxs-lookup"><span data-stu-id="f7f72-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="f7f72-125">Dozwolona jest specjalna wartość "any", co oznacza, że jest zgodna z portami TCP i UDP, ale nie innymi protokołami.</span><span class="sxs-lookup"><span data-stu-id="f7f72-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f72-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f7f72-126">-SourceAddress</span></span>
<span data-ttu-id="f7f72-127">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="f7f72-127">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f72-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="f7f72-128">-TranslatedAddress</span></span>
<span data-ttu-id="f7f72-129">Określa żądany wynik translacji adresów</span><span class="sxs-lookup"><span data-stu-id="f7f72-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="f7f72-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="f7f72-130">-TranslatedPort</span></span>
<span data-ttu-id="f7f72-131">Określa wymagany wynik translacji portów.</span><span class="sxs-lookup"><span data-stu-id="f7f72-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="f7f72-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7f72-132">-Confirm</span></span>
<span data-ttu-id="f7f72-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7f72-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f72-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f72-134">-WhatIf</span></span>
<span data-ttu-id="f7f72-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7f72-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f72-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7f72-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f72-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f72-137">CommonParameters</span></span>
<span data-ttu-id="f7f72-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f72-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f72-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f72-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f72-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7f72-140">INPUTS</span></span>

### <span data-ttu-id="f7f72-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f7f72-141">None</span></span>

## <span data-ttu-id="f7f72-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7f72-142">OUTPUTS</span></span>

### <span data-ttu-id="f7f72-143">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="f7f72-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="f7f72-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7f72-144">NOTES</span></span>

## <span data-ttu-id="f7f72-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7f72-145">RELATED LINKS</span></span>

[<span data-ttu-id="f7f72-146">Nowe — AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="f7f72-146">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="f7f72-147">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f7f72-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f7f72-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f7f72-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
