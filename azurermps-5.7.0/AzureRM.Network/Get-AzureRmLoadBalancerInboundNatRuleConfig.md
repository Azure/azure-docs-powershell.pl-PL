---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6464b1a7794278bf8bf350add937ac49f23431f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718908"
---
# <span data-ttu-id="2c151-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c151-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="2c151-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c151-102">SYNOPSIS</span></span>
<span data-ttu-id="2c151-103">Pobiera konfigurację reguły NAT dla ruchu przychodzącego dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2c151-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c151-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c151-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c151-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c151-105">DESCRIPTION</span></span>
<span data-ttu-id="2c151-106">Polecenie cmdlet **Get-AzureRmLoadBalancerInboundNatRuleConfig** pobiera co najmniej jeden Regulamin przychodzącego tłumaczenia adresów sieciowych (NAT) w usłudze Azure loadion.</span><span class="sxs-lookup"><span data-stu-id="2c151-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="2c151-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c151-107">EXAMPLES</span></span>

### <span data-ttu-id="2c151-108">Przykład 1: Pobieranie konfiguracji reguły ruchu przychodzącego NAT</span><span class="sxs-lookup"><span data-stu-id="2c151-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="2c151-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer i zapisuje ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="2c151-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="2c151-110">Drugie polecenie pobiera skojarzoną regułę NAT o nazwie MyInboundNatRule1 z modułu równoważenia obciążenia w $slb.</span><span class="sxs-lookup"><span data-stu-id="2c151-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="2c151-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c151-111">PARAMETERS</span></span>

### <span data-ttu-id="2c151-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c151-112">-DefaultProfile</span></span>
<span data-ttu-id="2c151-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c151-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c151-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="2c151-114">-LoadBalancer</span></span>
<span data-ttu-id="2c151-115">Określa moduł równoważenia obciążenia skojarzony z konfiguracją reguły przychodzącego NAT do pobrania.</span><span class="sxs-lookup"><span data-stu-id="2c151-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="2c151-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c151-116">-Name</span></span>
<span data-ttu-id="2c151-117">Określa nazwę konfiguracji reguły ruchu przychodzącego NAT do pobrania.</span><span class="sxs-lookup"><span data-stu-id="2c151-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="2c151-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c151-118">CommonParameters</span></span>
<span data-ttu-id="2c151-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c151-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c151-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c151-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c151-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c151-121">INPUTS</span></span>

### <span data-ttu-id="2c151-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2c151-122">PSLoadBalancer</span></span>
<span data-ttu-id="2c151-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="2c151-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="2c151-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c151-124">OUTPUTS</span></span>

### <span data-ttu-id="2c151-125">Microsoft. Azure. Commands. Network. models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="2c151-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="2c151-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c151-126">NOTES</span></span>

## <span data-ttu-id="2c151-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c151-127">RELATED LINKS</span></span>

[<span data-ttu-id="2c151-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2c151-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="2c151-129">Nowe — AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c151-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2c151-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c151-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2c151-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c151-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


