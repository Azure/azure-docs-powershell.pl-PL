---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 17af7cc61ec3d254133dd0563e8ea09fc0e3043f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892797"
---
# <span data-ttu-id="fbfea-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbfea-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="fbfea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbfea-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfea-103">Ustawia stan celu dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="fbfea-103">Sets the goal state for a load balancer.</span></span>

## <span data-ttu-id="fbfea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbfea-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbfea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbfea-105">DESCRIPTION</span></span>
<span data-ttu-id="fbfea-106">Polecenie cmdlet **Set-AzLoadBalancer** ustawia stan celu dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfea-106">The **Set-AzLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="fbfea-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbfea-107">EXAMPLES</span></span>

### <span data-ttu-id="fbfea-108">Przykład 1: modyfikowanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="fbfea-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="fbfea-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie NRPLB, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="fbfea-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="fbfea-110">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzLoadBalancerInboundNatRuleConfig, które dodaje przychodzącą regułę NAT o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="fbfea-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="fbfea-111">Trzecia komenda przekazuje modułowi równoważenia obciążenia polecenie **Set-AzLoadBalancer** , co powoduje zaktualizowanie konfiguracji modułu równoważenia obciążenia i zapisanie go.</span><span class="sxs-lookup"><span data-stu-id="fbfea-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="fbfea-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbfea-112">PARAMETERS</span></span>

### <span data-ttu-id="fbfea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbfea-113">-AsJob</span></span>
<span data-ttu-id="fbfea-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fbfea-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbfea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfea-115">-DefaultProfile</span></span>
<span data-ttu-id="fbfea-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbfea-117">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="fbfea-117">-LoadBalancer</span></span>
<span data-ttu-id="fbfea-118">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="fbfea-118">Specifies a load balancer.</span></span>
<span data-ttu-id="fbfea-119">To polecenie cmdlet ustawia stan celu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="fbfea-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbfea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfea-120">CommonParameters</span></span>
<span data-ttu-id="fbfea-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbfea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfea-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbfea-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfea-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbfea-123">INPUTS</span></span>

### <span data-ttu-id="fbfea-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbfea-124">PSLoadBalancer</span></span>
<span data-ttu-id="fbfea-125">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="fbfea-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="fbfea-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbfea-126">OUTPUTS</span></span>

### <span data-ttu-id="fbfea-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbfea-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fbfea-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbfea-128">NOTES</span></span>

## <span data-ttu-id="fbfea-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbfea-129">RELATED LINKS</span></span>

[<span data-ttu-id="fbfea-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbfea-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="fbfea-131">Nowe — AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbfea-131">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="fbfea-132">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbfea-132">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


