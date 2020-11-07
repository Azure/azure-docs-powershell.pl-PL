---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: be09bb6592ebf950c2fb3de6b4a512235fd0feab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717819"
---
# <span data-ttu-id="01558-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="01558-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="01558-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01558-102">SYNOPSIS</span></span>
<span data-ttu-id="01558-103">Ustawia stan celu dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="01558-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01558-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01558-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01558-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01558-105">DESCRIPTION</span></span>
<span data-ttu-id="01558-106">Polecenie cmdlet **Set-AzureRmLoadBalancer** ustawia stan celu dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01558-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="01558-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01558-107">EXAMPLES</span></span>

### <span data-ttu-id="01558-108">Przykład 1: modyfikowanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="01558-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="01558-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie NRPLB, a następnie zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="01558-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="01558-110">Drugie polecenie używa operatora potoku w celu przekazania modułu równoważenia obciążenia w $slb do polecenia Add-AzureRmLoadBalancerInboundNatRuleConfig, które dodaje przychodzącą regułę NAT o nazwie NewRule.</span><span class="sxs-lookup"><span data-stu-id="01558-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="01558-111">Trzecia komenda przekazuje modułowi równoważenia obciążenia polecenie **Set-AzureRmLoadBalancer** , co powoduje zaktualizowanie konfiguracji modułu równoważenia obciążenia i zapisanie go.</span><span class="sxs-lookup"><span data-stu-id="01558-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="01558-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01558-112">PARAMETERS</span></span>

### <span data-ttu-id="01558-113">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="01558-113">-LoadBalancer</span></span>
<span data-ttu-id="01558-114">Umożliwia określenie modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="01558-114">Specifies a load balancer.</span></span>
<span data-ttu-id="01558-115">To polecenie cmdlet ustawia stan celu dla modułu równoważenia obciążenia, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="01558-115">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="01558-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01558-116">-DefaultProfile</span></span>
<span data-ttu-id="01558-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01558-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01558-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01558-118">CommonParameters</span></span>
<span data-ttu-id="01558-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01558-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01558-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01558-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01558-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01558-121">INPUTS</span></span>

### <span data-ttu-id="01558-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="01558-122">PSLoadBalancer</span></span>
<span data-ttu-id="01558-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="01558-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="01558-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01558-124">OUTPUTS</span></span>

### <span data-ttu-id="01558-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="01558-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="01558-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01558-126">NOTES</span></span>

## <span data-ttu-id="01558-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01558-127">RELATED LINKS</span></span>

[<span data-ttu-id="01558-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="01558-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="01558-129">Nowe — AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="01558-129">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="01558-130">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="01558-130">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


