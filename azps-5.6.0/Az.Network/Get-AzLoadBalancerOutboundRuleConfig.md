---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: fc3b34e2fb9f91684aee2427d4271e6fab08843f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006449"
---
# <span data-ttu-id="99c10-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99c10-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="99c10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c10-102">SYNOPSIS</span></span>
<span data-ttu-id="99c10-103">Pobiera konfigurację reguł ruchu wychodzącego w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99c10-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="99c10-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99c10-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99c10-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="99c10-105">DESCRIPTION</span></span>
<span data-ttu-id="99c10-106">Polecenie **cmdlet Get-AzLoadBalancerOutboundRuleConfig** pobiera konfigurację reguły ruchu wychodzącego lub listę konfiguracji reguł ruchu wychodzącego w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99c10-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="99c10-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99c10-107">EXAMPLES</span></span>

### <span data-ttu-id="99c10-108">Przykład 1. Uzyskiwanie konfiguracji reguły ruchu wychodzącego w równoważeniu obciążenia</span><span class="sxs-lookup"><span data-stu-id="99c10-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="99c10-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="99c10-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="99c10-110">Drugie polecenie pobiera konfigurację reguły ruchu wychodzącego o nazwie MyRule skojarzoną z tym równoważeniem obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99c10-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="99c10-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99c10-111">PARAMETERS</span></span>

### <span data-ttu-id="99c10-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c10-112">-DefaultProfile</span></span>
<span data-ttu-id="99c10-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99c10-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99c10-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99c10-114">-LoadBalancer</span></span>
<span data-ttu-id="99c10-115">Odwołanie do zasobu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99c10-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="99c10-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99c10-116">-Name</span></span>
<span data-ttu-id="99c10-117">Nazwa reguły wychodzącej.</span><span class="sxs-lookup"><span data-stu-id="99c10-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="99c10-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c10-118">CommonParameters</span></span>
<span data-ttu-id="99c10-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c10-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c10-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99c10-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c10-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99c10-121">INPUTS</span></span>

### <span data-ttu-id="99c10-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99c10-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="99c10-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99c10-123">OUTPUTS</span></span>

### <span data-ttu-id="99c10-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="99c10-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="99c10-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99c10-125">NOTES</span></span>

## <span data-ttu-id="99c10-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99c10-126">RELATED LINKS</span></span>

[<span data-ttu-id="99c10-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99c10-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="99c10-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99c10-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="99c10-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99c10-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="99c10-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99c10-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
