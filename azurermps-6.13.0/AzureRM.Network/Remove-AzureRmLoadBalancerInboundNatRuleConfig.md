---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d76803df11ff3f89e20ca7d849577ca51331416c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547452"
---
# <span data-ttu-id="74ef5-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74ef5-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="74ef5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="74ef5-103">Usuwa konfigurację reguły NAT dla ruchu przychodzącego z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="74ef5-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74ef5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74ef5-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74ef5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74ef5-105">DESCRIPTION</span></span>
<span data-ttu-id="74ef5-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerInboundNatRuleConfig** usuwa konfigurację reguły translacji adresów sieciowych (NAT) ze składnika Azure Load równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="74ef5-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="74ef5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74ef5-107">EXAMPLES</span></span>

### <span data-ttu-id="74ef5-108">1: Usuwanie reguły ruchu przychodzącego NAT z modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="74ef5-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="74ef5-109">Pierwsze polecenie ładuje już istniejący moduł równoważenia obciążenia o nazwie "mylb" i zapisuje go w zmiennej $load modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="74ef5-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="74ef5-110">Drugie polecenie usuwa regułę ruchu przychodzącego NAT skojarzoną z tym modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="74ef5-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="74ef5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74ef5-111">PARAMETERS</span></span>

### <span data-ttu-id="74ef5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ef5-112">-DefaultProfile</span></span>
<span data-ttu-id="74ef5-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74ef5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74ef5-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="74ef5-114">-LoadBalancer</span></span>
<span data-ttu-id="74ef5-115">Określa obiekt **modułu równoważenia obciążenia** zawierający konfigurację reguły przychodzącego NAT, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ef5-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74ef5-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74ef5-116">-Name</span></span>
<span data-ttu-id="74ef5-117">Określa nazwę konfiguracji przychodzącej reguły NAT, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ef5-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="74ef5-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74ef5-118">-Confirm</span></span>
<span data-ttu-id="74ef5-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ef5-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ef5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ef5-120">-WhatIf</span></span>
<span data-ttu-id="74ef5-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ef5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74ef5-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74ef5-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74ef5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ef5-123">CommonParameters</span></span>
<span data-ttu-id="74ef5-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74ef5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ef5-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74ef5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ef5-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74ef5-126">INPUTS</span></span>

### <span data-ttu-id="74ef5-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74ef5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="74ef5-128">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74ef5-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="74ef5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74ef5-129">OUTPUTS</span></span>

### <span data-ttu-id="74ef5-130">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="74ef5-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="74ef5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74ef5-131">NOTES</span></span>

## <span data-ttu-id="74ef5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74ef5-132">RELATED LINKS</span></span>

[<span data-ttu-id="74ef5-133">Dodaj-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74ef5-133">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="74ef5-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74ef5-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="74ef5-135">Nowe — AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74ef5-135">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="74ef5-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="74ef5-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


