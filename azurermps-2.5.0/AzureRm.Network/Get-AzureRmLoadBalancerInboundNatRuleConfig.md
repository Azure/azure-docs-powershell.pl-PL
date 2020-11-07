---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: fbfa70146a5eb70d118e6cd1859f968c576d8a0f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899281"
---
# <span data-ttu-id="55c6b-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55c6b-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="55c6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="55c6b-103">Pobiera konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="55c6b-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55c6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55c6b-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55c6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="55c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="55c6b-106">Polecenie cmdlet **Get-AzureRmLoadBalancerInboundNatRuleConfig** pobiera co najmniej jeden Regulamin przychodzącego tłumaczenia adresów sieciowych (NAT) w usłudze Azure loadion.</span><span class="sxs-lookup"><span data-stu-id="55c6b-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="55c6b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55c6b-107">EXAMPLES</span></span>

### <span data-ttu-id="55c6b-108">Przykład 1: Pobieranie konfiguracji reguły ruchu przychodzącego NAT</span><span class="sxs-lookup"><span data-stu-id="55c6b-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="55c6b-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer i zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="55c6b-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="55c6b-110">Drugie polecenie pobiera skojarzoną regułę NAT o nazwie MyInboundNatRule1 z modułu równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="55c6b-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="55c6b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55c6b-111">PARAMETERS</span></span>

### <span data-ttu-id="55c6b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c6b-112">-DefaultProfile</span></span>
<span data-ttu-id="55c6b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="55c6b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55c6b-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="55c6b-114">-LoadBalancer</span></span>
<span data-ttu-id="55c6b-115">Określa moduł równoważenia obciążenia skojarzony z konfiguracją reguły przychodzącego NAT do pobrania.</span><span class="sxs-lookup"><span data-stu-id="55c6b-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="55c6b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55c6b-116">-Name</span></span>
<span data-ttu-id="55c6b-117">Określa nazwę konfiguracji reguły ruchu przychodzącego NAT do pobrania.</span><span class="sxs-lookup"><span data-stu-id="55c6b-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c6b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c6b-118">CommonParameters</span></span>
<span data-ttu-id="55c6b-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55c6b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c6b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c6b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c6b-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55c6b-121">INPUTS</span></span>

### <span data-ttu-id="55c6b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55c6b-122">PSLoadBalancer</span></span>
<span data-ttu-id="55c6b-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="55c6b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="55c6b-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55c6b-124">OUTPUTS</span></span>

### <span data-ttu-id="55c6b-125">Microsoft. Azure. Commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="55c6b-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="55c6b-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55c6b-126">NOTES</span></span>

## <span data-ttu-id="55c6b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55c6b-127">RELATED LINKS</span></span>

[<span data-ttu-id="55c6b-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="55c6b-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="55c6b-129">Nowe — AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55c6b-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="55c6b-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55c6b-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="55c6b-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55c6b-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


