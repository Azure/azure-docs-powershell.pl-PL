---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 463b9cf07bbb04273e1653f4d84805de3802b616
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542511"
---
# <span data-ttu-id="fa9ca-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa9ca-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="fa9ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9ca-103">Ustawia stan celu dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="fa9ca-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa9ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa9ca-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa9ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa9ca-105">DESCRIPTION</span></span>
<span data-ttu-id="fa9ca-106">Polecenie cmdlet **Set-AzureRmLoadBalancer** ustawia stan celu dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fa9ca-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="fa9ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa9ca-107">EXAMPLES</span></span>

### <span data-ttu-id="fa9ca-108">Przykład 1: modyfikowanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="fa9ca-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="fa9ca-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie NRPLB, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="fa9ca-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="fa9ca-110">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzureRmLoadBalancerInboundNatRuleConfig, które dodaje przychodzącą regułę NAT o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="fa9ca-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="fa9ca-111">Trzecia komenda przekazuje modułowi równoważenia obciążenia polecenie **Set-AzureRmLoadBalancer** , co powoduje zaktualizowanie konfiguracji modułu równoważenia obciążenia i zapisanie go.</span><span class="sxs-lookup"><span data-stu-id="fa9ca-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="fa9ca-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa9ca-112">PARAMETERS</span></span>

### <span data-ttu-id="fa9ca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa9ca-113">-AsJob</span></span>
<span data-ttu-id="fa9ca-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fa9ca-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa9ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9ca-115">-DefaultProfile</span></span>
<span data-ttu-id="fa9ca-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa9ca-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa9ca-117">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="fa9ca-117">-LoadBalancer</span></span>
<span data-ttu-id="fa9ca-118">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="fa9ca-118">Specifies a load balancer.</span></span>
<span data-ttu-id="fa9ca-119">To polecenie cmdlet ustawia stan celu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="fa9ca-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa9ca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9ca-120">CommonParameters</span></span>
<span data-ttu-id="fa9ca-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa9ca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9ca-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa9ca-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9ca-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa9ca-123">INPUTS</span></span>

### <span data-ttu-id="fa9ca-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa9ca-124">PSLoadBalancer</span></span>
<span data-ttu-id="fa9ca-125">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="fa9ca-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="fa9ca-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa9ca-126">OUTPUTS</span></span>

### <span data-ttu-id="fa9ca-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa9ca-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fa9ca-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa9ca-128">NOTES</span></span>

## <span data-ttu-id="fa9ca-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa9ca-129">RELATED LINKS</span></span>

[<span data-ttu-id="fa9ca-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa9ca-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="fa9ca-131">Nowe — AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa9ca-131">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="fa9ca-132">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fa9ca-132">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


