---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225191"
---
# <span data-ttu-id="d82c4-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d82c4-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="d82c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d82c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d82c4-103">Pobiera konfigurację reguły ruchu wychodzącego w usłudze równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d82c4-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="d82c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d82c4-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d82c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d82c4-105">DESCRIPTION</span></span>
<span data-ttu-id="d82c4-106">Polecenie cmdlet **Get-AzLoadBalancerOutboundRuleConfig** Pobiera konfigurację reguły ruchu wychodzącego lub listę konfiguracji reguł ruchu wychodzącego w ramach modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d82c4-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="d82c4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d82c4-107">EXAMPLES</span></span>

### <span data-ttu-id="d82c4-108">Przykład 1: Pobieranie konfiguracji reguły ruchu wychodzącego w usłudze równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="d82c4-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="d82c4-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="d82c4-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="d82c4-110">Drugie polecenie pobiera konfigurację reguły ruchu wychodzącego o nazwie Moja reguła skojarzona z tym modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d82c4-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="d82c4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d82c4-111">PARAMETERS</span></span>

### <span data-ttu-id="d82c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d82c4-112">-DefaultProfile</span></span>
<span data-ttu-id="d82c4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d82c4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d82c4-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="d82c4-114">-LoadBalancer</span></span>
<span data-ttu-id="d82c4-115">Odwołanie do zasobu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d82c4-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="d82c4-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d82c4-116">-Name</span></span>
<span data-ttu-id="d82c4-117">Nazwa reguły ruchu wychodzącego.</span><span class="sxs-lookup"><span data-stu-id="d82c4-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="d82c4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d82c4-118">CommonParameters</span></span>
<span data-ttu-id="d82c4-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d82c4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d82c4-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d82c4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d82c4-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d82c4-121">INPUTS</span></span>

### <span data-ttu-id="d82c4-122">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d82c4-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d82c4-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d82c4-123">OUTPUTS</span></span>

### <span data-ttu-id="d82c4-124">Microsoft. Azure. Commands. Network. models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="d82c4-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="d82c4-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d82c4-125">NOTES</span></span>

## <span data-ttu-id="d82c4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d82c4-126">RELATED LINKS</span></span>

[<span data-ttu-id="d82c4-127">Dodaj-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d82c4-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d82c4-128">Nowe — AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d82c4-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d82c4-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d82c4-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d82c4-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d82c4-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
