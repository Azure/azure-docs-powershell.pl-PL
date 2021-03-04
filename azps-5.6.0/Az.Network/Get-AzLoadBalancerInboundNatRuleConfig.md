---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 816c94281c246762dac41f2e69e080dfec70565d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954561"
---
# <span data-ttu-id="f4962-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4962-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f4962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4962-102">SYNOPSIS</span></span>
<span data-ttu-id="f4962-103">Pobiera konfigurację reguły nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f4962-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="f4962-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f4962-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4962-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f4962-105">DESCRIPTION</span></span>
<span data-ttu-id="f4962-106">Polecenie **cmdlet Get-AzLoadBalancerInboundNatRuleConfig** pobiera jedną lub więcej reguł translacji adresów sieciowych (NAT) w narzędzie do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4962-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="f4962-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f4962-107">EXAMPLES</span></span>

### <span data-ttu-id="f4962-108">Przykład 1. Uzyskiwanie konfiguracji reguły nat ruchu przychodzącego</span><span class="sxs-lookup"><span data-stu-id="f4962-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="f4962-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer i przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="f4962-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="f4962-110">Drugie polecenie pobiera skojarzoną regułę NAT o nazwie MyInboundNatRule1 z równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="f4962-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="f4962-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4962-111">PARAMETERS</span></span>

### <span data-ttu-id="f4962-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4962-112">-DefaultProfile</span></span>
<span data-ttu-id="f4962-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4962-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4962-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4962-114">-LoadBalancer</span></span>
<span data-ttu-id="f4962-115">Określa, jaka jest skojarzona z konfiguracją reguły nat ruchu przychodzącego, która ma być skojarzona z konfiguracją przychodzącego serwera NAT.</span><span class="sxs-lookup"><span data-stu-id="f4962-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="f4962-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f4962-116">-Name</span></span>
<span data-ttu-id="f4962-117">Określa nazwę konfiguracji przychodzącej reguły NAT do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="f4962-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="f4962-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4962-118">CommonParameters</span></span>
<span data-ttu-id="f4962-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4962-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4962-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4962-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4962-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4962-121">INPUTS</span></span>

### <span data-ttu-id="f4962-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4962-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f4962-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4962-123">OUTPUTS</span></span>

### <span data-ttu-id="f4962-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="f4962-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="f4962-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f4962-125">NOTES</span></span>

## <span data-ttu-id="f4962-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4962-126">RELATED LINKS</span></span>

[<span data-ttu-id="f4962-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4962-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f4962-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4962-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f4962-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4962-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f4962-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f4962-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


