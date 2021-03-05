---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: b608a8fe62f7316116409d4174ea01603b928ae2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963937"
---
# <span data-ttu-id="456c9-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="456c9-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="456c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="456c9-102">SYNOPSIS</span></span>
<span data-ttu-id="456c9-103">Aktualizuje równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="456c9-103">Updates a load balancer.</span></span>

## <span data-ttu-id="456c9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="456c9-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="456c9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="456c9-105">DESCRIPTION</span></span>
<span data-ttu-id="456c9-106">Polecenie **cmdlet Set-AzLoadBalancer** aktualizuje równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="456c9-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="456c9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="456c9-107">EXAMPLES</span></span>

### <span data-ttu-id="456c9-108">Przykład 1. Modyfikowanie równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="456c9-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="456c9-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie NRPLB, a następnie zapisuje je w $slb danych.</span><span class="sxs-lookup"><span data-stu-id="456c9-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="456c9-110">Drugie polecenie używa operatora potoku do przekazania równoważenia obciążenia w programie $slb do dodatku AzLoadBalancerInboundNatRuleConfig, który dodaje regułę nat ruchu przychodzącego o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="456c9-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="456c9-111">Trzecie polecenie przekazuje równoważenie obciążenia do polecenia **Set-AzLoadBalancer,** które aktualizuje konfigurację równoważenia obciążenia i zapisuje je.</span><span class="sxs-lookup"><span data-stu-id="456c9-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="456c9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="456c9-112">PARAMETERS</span></span>

### <span data-ttu-id="456c9-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="456c9-113">-AsJob</span></span>
<span data-ttu-id="456c9-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="456c9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="456c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456c9-115">-DefaultProfile</span></span>
<span data-ttu-id="456c9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="456c9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="456c9-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="456c9-117">-LoadBalancer</span></span>
<span data-ttu-id="456c9-118">Określa obiekt równoważenia obciążenia reprezentujący stan, dla którego należy ustawić równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="456c9-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="456c9-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="456c9-119">-Confirm</span></span>
<span data-ttu-id="456c9-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="456c9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456c9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456c9-121">-WhatIf</span></span>
<span data-ttu-id="456c9-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="456c9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="456c9-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="456c9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456c9-124">CommonParameters</span></span>
<span data-ttu-id="456c9-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456c9-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="456c9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456c9-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="456c9-127">INPUTS</span></span>

### <span data-ttu-id="456c9-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="456c9-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="456c9-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="456c9-129">OUTPUTS</span></span>

### <span data-ttu-id="456c9-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="456c9-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="456c9-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="456c9-131">NOTES</span></span>

## <span data-ttu-id="456c9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="456c9-132">RELATED LINKS</span></span>

[<span data-ttu-id="456c9-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="456c9-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="456c9-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="456c9-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="456c9-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="456c9-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


