---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193858"
---
# <span data-ttu-id="551b3-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="551b3-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="551b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="551b3-102">SYNOPSIS</span></span>
<span data-ttu-id="551b3-103">Pobiera konfigurację reguł ruchu wychodzącego w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="551b3-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="551b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="551b3-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="551b3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="551b3-105">DESCRIPTION</span></span>
<span data-ttu-id="551b3-106">Polecenie **cmdlet Get-AzLoadBalancerOutboundRuleConfig** pobiera konfigurację reguły ruchu wychodzącego lub listę konfiguracji reguł ruchu wychodzącego w równoważeniu obciążenia.</span><span class="sxs-lookup"><span data-stu-id="551b3-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="551b3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="551b3-107">EXAMPLES</span></span>

### <span data-ttu-id="551b3-108">Przykład 1. Uzyskiwanie konfiguracji reguły ruchu wychodzącego w równoważeniu obciążenia</span><span class="sxs-lookup"><span data-stu-id="551b3-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="551b3-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w zmiennym $slb.</span><span class="sxs-lookup"><span data-stu-id="551b3-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="551b3-110">Drugie polecenie pobiera konfigurację reguły ruchu wychodzącego o nazwie MyRule skojarzoną z tym równoważeniem obciążenia.</span><span class="sxs-lookup"><span data-stu-id="551b3-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="551b3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="551b3-111">PARAMETERS</span></span>

### <span data-ttu-id="551b3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551b3-112">-DefaultProfile</span></span>
<span data-ttu-id="551b3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="551b3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="551b3-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="551b3-114">-LoadBalancer</span></span>
<span data-ttu-id="551b3-115">Odwołanie do zasobu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="551b3-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="551b3-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="551b3-116">-Name</span></span>
<span data-ttu-id="551b3-117">Nazwa reguły wychodzącej.</span><span class="sxs-lookup"><span data-stu-id="551b3-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="551b3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551b3-118">CommonParameters</span></span>
<span data-ttu-id="551b3-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551b3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551b3-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="551b3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551b3-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="551b3-121">INPUTS</span></span>

### <span data-ttu-id="551b3-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="551b3-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="551b3-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="551b3-123">OUTPUTS</span></span>

### <span data-ttu-id="551b3-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="551b3-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="551b3-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="551b3-125">NOTES</span></span>

## <span data-ttu-id="551b3-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="551b3-126">RELATED LINKS</span></span>

[<span data-ttu-id="551b3-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="551b3-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="551b3-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="551b3-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="551b3-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="551b3-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="551b3-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="551b3-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
