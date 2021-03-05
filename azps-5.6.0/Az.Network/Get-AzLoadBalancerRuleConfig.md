---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d5782ea85a97df723967d73cf2716d837477f01d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006426"
---
# <span data-ttu-id="e850d-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e850d-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="e850d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e850d-102">SYNOPSIS</span></span>
<span data-ttu-id="e850d-103">Pobiera konfigurację reguły dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e850d-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="e850d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e850d-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e850d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e850d-105">DESCRIPTION</span></span>
<span data-ttu-id="e850d-106">Polecenie **cmdlet Get-AzLoadBalancerRuleConfig** pobiera jedną lub więcej konfiguracji reguł dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e850d-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="e850d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e850d-107">EXAMPLES</span></span>

### <span data-ttu-id="e850d-108">Przykład 1. Uzyskiwanie konfiguracji reguły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e850d-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="e850d-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="e850d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e850d-110">Drugie polecenie pobiera skojarzoną konfigurację reguł o nazwie MyLBrulename z równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="e850d-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="e850d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e850d-111">PARAMETERS</span></span>

### <span data-ttu-id="e850d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e850d-112">-DefaultProfile</span></span>
<span data-ttu-id="e850d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e850d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e850d-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e850d-114">-LoadBalancer</span></span>
<span data-ttu-id="e850d-115">Określa równoważenie obciążenia skojarzone z konfiguracją reguły, która ma być skojarzona z jej konfiguracją.</span><span class="sxs-lookup"><span data-stu-id="e850d-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="e850d-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e850d-116">-Name</span></span>
<span data-ttu-id="e850d-117">Określa nazwę konfiguracji reguły do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="e850d-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="e850d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e850d-118">CommonParameters</span></span>
<span data-ttu-id="e850d-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e850d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e850d-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e850d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e850d-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e850d-121">INPUTS</span></span>

### <span data-ttu-id="e850d-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e850d-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e850d-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e850d-123">OUTPUTS</span></span>

### <span data-ttu-id="e850d-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="e850d-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="e850d-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e850d-125">NOTES</span></span>

## <span data-ttu-id="e850d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e850d-126">RELATED LINKS</span></span>

[<span data-ttu-id="e850d-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e850d-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="e850d-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e850d-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e850d-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e850d-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="e850d-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e850d-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


