---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6b866dc04975c2cde17509182e21936a2d6c9363
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890770"
---
# <span data-ttu-id="7432f-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7432f-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="7432f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7432f-102">SYNOPSIS</span></span>
<span data-ttu-id="7432f-103">Pobiera konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7432f-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="7432f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7432f-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7432f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7432f-105">DESCRIPTION</span></span>
<span data-ttu-id="7432f-106">Polecenie cmdlet **Get-AzLoadBalancerInboundNatRuleConfig** pobiera co najmniej jeden Regulamin przychodzącego tłumaczenia adresów sieciowych (NAT) w usłudze Azure loadion.</span><span class="sxs-lookup"><span data-stu-id="7432f-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="7432f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7432f-107">EXAMPLES</span></span>

### <span data-ttu-id="7432f-108">Przykład 1: Pobieranie konfiguracji reguły ruchu przychodzącego NAT</span><span class="sxs-lookup"><span data-stu-id="7432f-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="7432f-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer i zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="7432f-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="7432f-110">Drugie polecenie pobiera skojarzoną regułę NAT o nazwie MyInboundNatRule1 z modułu równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="7432f-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="7432f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7432f-111">PARAMETERS</span></span>

### <span data-ttu-id="7432f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7432f-112">-DefaultProfile</span></span>
<span data-ttu-id="7432f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7432f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7432f-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7432f-114">-LoadBalancer</span></span>
<span data-ttu-id="7432f-115">Określa moduł równoważenia obciążenia skojarzony z konfiguracją reguły przychodzącego NAT do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7432f-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="7432f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7432f-116">-Name</span></span>
<span data-ttu-id="7432f-117">Określa nazwę konfiguracji reguły ruchu przychodzącego NAT do pobrania.</span><span class="sxs-lookup"><span data-stu-id="7432f-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="7432f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7432f-118">CommonParameters</span></span>
<span data-ttu-id="7432f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7432f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7432f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7432f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7432f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7432f-121">INPUTS</span></span>

### <span data-ttu-id="7432f-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7432f-122">PSLoadBalancer</span></span>
<span data-ttu-id="7432f-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="7432f-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7432f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7432f-124">OUTPUTS</span></span>

### <span data-ttu-id="7432f-125">Microsoft. Azure. Commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="7432f-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="7432f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7432f-126">NOTES</span></span>

## <span data-ttu-id="7432f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7432f-127">RELATED LINKS</span></span>

[<span data-ttu-id="7432f-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7432f-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7432f-129">Nowe — AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7432f-129">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7432f-130">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7432f-130">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7432f-131">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7432f-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


