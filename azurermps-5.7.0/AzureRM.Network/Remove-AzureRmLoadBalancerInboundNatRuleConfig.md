---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6dcd7c51a43387139de85a3a9f0c17c0b19cfe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546687"
---
# <span data-ttu-id="8c959-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c959-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="8c959-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c959-102">SYNOPSIS</span></span>
<span data-ttu-id="8c959-103">Usuwa konfigurację reguły NAT dla ruchu przychodzącego z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8c959-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c959-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c959-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c959-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8c959-105">DESCRIPTION</span></span>
<span data-ttu-id="8c959-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerInboundNatRuleConfig** usuwa konfigurację reguły translacji adresów sieciowych (NAT) ze składnika Azure Load równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8c959-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="8c959-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c959-107">EXAMPLES</span></span>

### <span data-ttu-id="8c959-108">1: Usuwanie reguły ruchu przychodzącego NAT z modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8c959-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="8c959-109">Pierwsze polecenie ładuje już istniejący moduł równoważenia obciążenia o nazwie "mylb" i zapisuje go w zmiennej $load modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8c959-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="8c959-110">Drugie polecenie usuwa regułę ruchu przychodzącego NAT skojarzoną z tym modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8c959-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="8c959-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c959-111">PARAMETERS</span></span>

### <span data-ttu-id="8c959-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c959-112">-DefaultProfile</span></span>
<span data-ttu-id="8c959-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c959-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c959-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="8c959-114">-LoadBalancer</span></span>
<span data-ttu-id="8c959-115">Określa obiekt **modułu równoważenia obciążenia** zawierający konfigurację reguły przychodzącego NAT, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c959-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8c959-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c959-116">-Name</span></span>
<span data-ttu-id="8c959-117">Określa nazwę konfiguracji przychodzącej reguły NAT, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c959-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8c959-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c959-118">CommonParameters</span></span>
<span data-ttu-id="8c959-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c959-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c959-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c959-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c959-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c959-121">INPUTS</span></span>

### <span data-ttu-id="8c959-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8c959-122">PSLoadBalancer</span></span>
<span data-ttu-id="8c959-123">Parametr "równoważenia obciążenia" akceptuje wartość typu "PSLoadBalancer" z procesu</span><span class="sxs-lookup"><span data-stu-id="8c959-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8c959-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c959-124">OUTPUTS</span></span>

### <span data-ttu-id="8c959-125">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8c959-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8c959-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c959-126">NOTES</span></span>

## <span data-ttu-id="8c959-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c959-127">RELATED LINKS</span></span>

[<span data-ttu-id="8c959-128">Dodaj-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c959-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8c959-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c959-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8c959-130">Nowe — AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c959-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8c959-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8c959-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


