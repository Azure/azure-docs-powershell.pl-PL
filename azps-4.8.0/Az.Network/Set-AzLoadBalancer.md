---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220486"
---
# <span data-ttu-id="e077c-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e077c-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="e077c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e077c-102">SYNOPSIS</span></span>
<span data-ttu-id="e077c-103">Umożliwia zaktualizowanie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e077c-103">Updates a load balancer.</span></span>

## <span data-ttu-id="e077c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e077c-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e077c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e077c-105">DESCRIPTION</span></span>
<span data-ttu-id="e077c-106">Polecenie cmdlet **Set-AzLoadBalancer** umożliwia zaktualizowanie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e077c-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="e077c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e077c-107">EXAMPLES</span></span>

### <span data-ttu-id="e077c-108">Przykład 1: modyfikowanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e077c-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="e077c-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie NRPLB, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="e077c-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="e077c-110">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzLoadBalancerInboundNatRuleConfig, które dodaje przychodzącą regułę NAT o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="e077c-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="e077c-111">Trzecia komenda przekazuje modułowi równoważenia obciążenia polecenie **Set-AzLoadBalancer** , co powoduje zaktualizowanie konfiguracji modułu równoważenia obciążenia i zapisanie go.</span><span class="sxs-lookup"><span data-stu-id="e077c-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="e077c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e077c-112">PARAMETERS</span></span>

### <span data-ttu-id="e077c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e077c-113">-AsJob</span></span>
<span data-ttu-id="e077c-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e077c-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e077c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e077c-115">-DefaultProfile</span></span>
<span data-ttu-id="e077c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e077c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e077c-117">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="e077c-117">-LoadBalancer</span></span>
<span data-ttu-id="e077c-118">Określa obiekt modułu równoważenia obciążenia reprezentujący stan, do którego należy ustawić moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="e077c-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e077c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e077c-119">-Confirm</span></span>
<span data-ttu-id="e077c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e077c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e077c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e077c-121">-WhatIf</span></span>
<span data-ttu-id="e077c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e077c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e077c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e077c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e077c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e077c-124">CommonParameters</span></span>
<span data-ttu-id="e077c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e077c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e077c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e077c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e077c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e077c-127">INPUTS</span></span>

### <span data-ttu-id="e077c-128">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e077c-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e077c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e077c-129">OUTPUTS</span></span>

### <span data-ttu-id="e077c-130">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e077c-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e077c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e077c-131">NOTES</span></span>

## <span data-ttu-id="e077c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e077c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e077c-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e077c-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e077c-134">Nowe — AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e077c-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="e077c-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e077c-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


