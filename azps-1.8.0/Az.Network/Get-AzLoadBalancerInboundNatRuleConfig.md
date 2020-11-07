---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: e28ebc04277e3c9031c9c287aa02f7eea32867a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709523"
---
# <span data-ttu-id="a1c0a-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c0a-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a1c0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c0a-103">Pobiera konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a1c0a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1c0a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1c0a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a1c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c0a-106">Polecenie cmdlet **Get-AzLoadBalancerInboundNatRuleConfig** pobiera co najmniej jeden Regulamin przychodzącego tłumaczenia adresów sieciowych (NAT) w usłudze Azure loadion.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="a1c0a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1c0a-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c0a-108">Przykład 1: Pobieranie konfiguracji reguły ruchu przychodzącego NAT</span><span class="sxs-lookup"><span data-stu-id="a1c0a-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="a1c0a-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer i zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="a1c0a-110">Drugie polecenie pobiera skojarzoną regułę NAT o nazwie MyInboundNatRule1 z modułu równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="a1c0a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1c0a-111">PARAMETERS</span></span>

### <span data-ttu-id="a1c0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c0a-112">-DefaultProfile</span></span>
<span data-ttu-id="a1c0a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1c0a-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a1c0a-114">-LoadBalancer</span></span>
<span data-ttu-id="a1c0a-115">Określa moduł równoważenia obciążenia skojarzony z konfiguracją reguły przychodzącego NAT do pobrania.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="a1c0a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1c0a-116">-Name</span></span>
<span data-ttu-id="a1c0a-117">Określa nazwę konfiguracji reguły ruchu przychodzącego NAT do pobrania.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="a1c0a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c0a-118">CommonParameters</span></span>
<span data-ttu-id="a1c0a-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c0a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c0a-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1c0a-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c0a-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1c0a-121">INPUTS</span></span>

### <span data-ttu-id="a1c0a-122">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1c0a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a1c0a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1c0a-123">OUTPUTS</span></span>

### <span data-ttu-id="a1c0a-124">Microsoft. Azure. Commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a1c0a-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="a1c0a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1c0a-125">NOTES</span></span>

## <span data-ttu-id="a1c0a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1c0a-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1c0a-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1c0a-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a1c0a-128">Nowe — AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c0a-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a1c0a-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c0a-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a1c0a-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c0a-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)

