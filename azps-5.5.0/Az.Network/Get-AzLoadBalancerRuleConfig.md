---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187123"
---
# <span data-ttu-id="203f9-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="203f9-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="203f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="203f9-102">SYNOPSIS</span></span>
<span data-ttu-id="203f9-103">Pobiera konfigurację reguły dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="203f9-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="203f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="203f9-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="203f9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="203f9-105">DESCRIPTION</span></span>
<span data-ttu-id="203f9-106">Polecenie **cmdlet Get-AzLoadBalancerRuleConfig** pobiera jedną lub więcej konfiguracji reguł dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="203f9-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="203f9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="203f9-107">EXAMPLES</span></span>

### <span data-ttu-id="203f9-108">Przykład 1. Uzyskiwanie konfiguracji reguły równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="203f9-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="203f9-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="203f9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="203f9-110">Drugie polecenie pobiera skojarzoną konfigurację reguł o nazwie MyLBrulename z równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="203f9-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="203f9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="203f9-111">PARAMETERS</span></span>

### <span data-ttu-id="203f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203f9-112">-DefaultProfile</span></span>
<span data-ttu-id="203f9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="203f9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="203f9-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="203f9-114">-LoadBalancer</span></span>
<span data-ttu-id="203f9-115">Określa równoważenie obciążenia skojarzone z konfiguracją reguły, która ma być skojarzona z jej konfiguracją.</span><span class="sxs-lookup"><span data-stu-id="203f9-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="203f9-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="203f9-116">-Name</span></span>
<span data-ttu-id="203f9-117">Określa nazwę konfiguracji reguły do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="203f9-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="203f9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203f9-118">CommonParameters</span></span>
<span data-ttu-id="203f9-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203f9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203f9-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="203f9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203f9-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="203f9-121">INPUTS</span></span>

### <span data-ttu-id="203f9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="203f9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="203f9-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="203f9-123">OUTPUTS</span></span>

### <span data-ttu-id="203f9-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="203f9-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="203f9-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="203f9-125">NOTES</span></span>

## <span data-ttu-id="203f9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="203f9-126">RELATED LINKS</span></span>

[<span data-ttu-id="203f9-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="203f9-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="203f9-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="203f9-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="203f9-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="203f9-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="203f9-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="203f9-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


