---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 5090d97157e608b2c3f6ef52d6eafa932ae4be50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548628"
---
# <span data-ttu-id="2df7c-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2df7c-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="2df7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2df7c-102">SYNOPSIS</span></span>
<span data-ttu-id="2df7c-103">Ustawia stan celu dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2df7c-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2df7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2df7c-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2df7c-105">DESCRIPTION</span></span>
<span data-ttu-id="2df7c-106">Polecenie cmdlet **Set-AzureRmLoadBalancer** ustawia stan celu dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2df7c-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="2df7c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2df7c-107">EXAMPLES</span></span>

### <span data-ttu-id="2df7c-108">Przykład 1: modyfikowanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="2df7c-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="2df7c-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie NRPLB, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="2df7c-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="2df7c-110">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzureRmLoadBalancerInboundNatRuleConfig, które dodaje przychodzącą regułę NAT o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="2df7c-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="2df7c-111">Trzecia komenda przekazuje modułowi równoważenia obciążenia polecenie **Set-AzureRmLoadBalancer** , co powoduje zaktualizowanie konfiguracji modułu równoważenia obciążenia i zapisanie go.</span><span class="sxs-lookup"><span data-stu-id="2df7c-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="2df7c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2df7c-112">PARAMETERS</span></span>

### <span data-ttu-id="2df7c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2df7c-113">-AsJob</span></span>
<span data-ttu-id="2df7c-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2df7c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2df7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df7c-115">-DefaultProfile</span></span>
<span data-ttu-id="2df7c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2df7c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df7c-117">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="2df7c-117">-LoadBalancer</span></span>
<span data-ttu-id="2df7c-118">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2df7c-118">Specifies a load balancer.</span></span>
<span data-ttu-id="2df7c-119">To polecenie cmdlet ustawia stan celu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2df7c-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2df7c-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2df7c-120">-Confirm</span></span>
<span data-ttu-id="2df7c-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2df7c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df7c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df7c-122">-WhatIf</span></span>
<span data-ttu-id="2df7c-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2df7c-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2df7c-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2df7c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df7c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df7c-125">CommonParameters</span></span>
<span data-ttu-id="2df7c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df7c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df7c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df7c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df7c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2df7c-128">INPUTS</span></span>

### <span data-ttu-id="2df7c-129">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2df7c-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="2df7c-130">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2df7c-130">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="2df7c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2df7c-131">OUTPUTS</span></span>

### <span data-ttu-id="2df7c-132">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2df7c-132">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2df7c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2df7c-133">NOTES</span></span>

## <span data-ttu-id="2df7c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2df7c-134">RELATED LINKS</span></span>

[<span data-ttu-id="2df7c-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2df7c-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="2df7c-136">Nowe — AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2df7c-136">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="2df7c-137">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2df7c-137">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


