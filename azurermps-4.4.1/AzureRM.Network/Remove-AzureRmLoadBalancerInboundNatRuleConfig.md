---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ee831cf3f2b6441bde55dc458d6b9af33f4b42e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525506"
---
# <span data-ttu-id="f73c4-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f73c4-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f73c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f73c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f73c4-103">Usuwa konfigurację reguły NAT dla ruchu przychodzącego z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f73c4-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f73c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f73c4-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f73c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f73c4-105">DESCRIPTION</span></span>
<span data-ttu-id="f73c4-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerInboundNatRuleConfig** usuwa konfigurację reguły translacji adresów sieciowych (NAT) ze składnika Azure Load równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f73c4-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="f73c4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f73c4-107">EXAMPLES</span></span>

### <span data-ttu-id="f73c4-108">1: Usuwanie reguły ruchu przychodzącego NAT z modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f73c4-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f73c4-109">Pierwsze polecenie ładuje już istniejący moduł równoważenia obciążenia o nazwie "mylb" i zapisuje go w zmiennej $load modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f73c4-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="f73c4-110">Drugie polecenie usuwa regułę ruchu przychodzącego NAT skojarzoną z tym modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f73c4-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="f73c4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f73c4-111">PARAMETERS</span></span>

### <span data-ttu-id="f73c4-112">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f73c4-112">-LoadBalancer</span></span>
<span data-ttu-id="f73c4-113">Określa obiekt **modułu równoważenia obciążenia** zawierający konfigurację reguły przychodzącego NAT, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f73c4-113">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f73c4-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f73c4-114">-Name</span></span>
<span data-ttu-id="f73c4-115">Określa nazwę konfiguracji przychodzącej reguły NAT, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f73c4-115">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f73c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73c4-116">-DefaultProfile</span></span>
<span data-ttu-id="f73c4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f73c4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f73c4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73c4-118">CommonParameters</span></span>
<span data-ttu-id="f73c4-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f73c4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73c4-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f73c4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73c4-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f73c4-121">INPUTS</span></span>

### <span data-ttu-id="f73c4-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f73c4-122">PSLoadBalancer</span></span>
<span data-ttu-id="f73c4-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="f73c4-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f73c4-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f73c4-124">OUTPUTS</span></span>

### <span data-ttu-id="f73c4-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f73c4-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f73c4-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f73c4-126">NOTES</span></span>

## <span data-ttu-id="f73c4-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f73c4-127">RELATED LINKS</span></span>

[<span data-ttu-id="f73c4-128">Dodaj-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f73c4-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f73c4-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f73c4-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f73c4-130">Nowe — AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f73c4-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f73c4-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f73c4-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


