---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193859"
---
# <span data-ttu-id="ae2a1-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae2a1-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ae2a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2a1-103">Pobiera konfigurację reguły nat ruchu przychodzącego dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ae2a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae2a1-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae2a1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae2a1-105">DESCRIPTION</span></span>
<span data-ttu-id="ae2a1-106">Polecenie **cmdlet Get-AzLoadBalancerInboundNatRuleConfig** pobiera jedną lub więcej reguł translacji adresów sieciowych (NAT) w narzędzie do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="ae2a1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae2a1-107">EXAMPLES</span></span>

### <span data-ttu-id="ae2a1-108">Przykład 1. Uzyskiwanie konfiguracji reguły nat ruchu przychodzącego</span><span class="sxs-lookup"><span data-stu-id="ae2a1-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="ae2a1-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer i przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="ae2a1-110">Drugie polecenie pobiera skojarzoną regułę NAT o nazwie MyInboundNatRule1 z równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="ae2a1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae2a1-111">PARAMETERS</span></span>

### <span data-ttu-id="ae2a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2a1-112">-DefaultProfile</span></span>
<span data-ttu-id="ae2a1-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae2a1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae2a1-114">-LoadBalancer</span></span>
<span data-ttu-id="ae2a1-115">Określa, jaka jest skojarzona z konfiguracją reguły nat ruchu przychodzącego, która ma być skojarzona z konfiguracją przychodzącego serwera NAT.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="ae2a1-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae2a1-116">-Name</span></span>
<span data-ttu-id="ae2a1-117">Określa nazwę konfiguracji reguły nat ruchu przychodzącego do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="ae2a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2a1-118">CommonParameters</span></span>
<span data-ttu-id="ae2a1-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae2a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2a1-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae2a1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2a1-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae2a1-121">INPUTS</span></span>

### <span data-ttu-id="ae2a1-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae2a1-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ae2a1-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae2a1-123">OUTPUTS</span></span>

### <span data-ttu-id="ae2a1-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="ae2a1-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="ae2a1-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae2a1-125">NOTES</span></span>

## <span data-ttu-id="ae2a1-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae2a1-126">RELATED LINKS</span></span>

[<span data-ttu-id="ae2a1-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae2a1-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ae2a1-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae2a1-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ae2a1-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae2a1-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ae2a1-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ae2a1-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


