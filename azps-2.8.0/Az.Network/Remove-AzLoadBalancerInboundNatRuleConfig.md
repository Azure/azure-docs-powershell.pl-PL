---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 2d47a3481772d846a65e3b0bc0d1eb1c62fa5cd5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869711"
---
# <span data-ttu-id="99e07-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99e07-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="99e07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99e07-102">SYNOPSIS</span></span>
<span data-ttu-id="99e07-103">Usuwa konfigurację reguły NAT dla ruchu przychodzącego z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99e07-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="99e07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99e07-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99e07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99e07-105">DESCRIPTION</span></span>
<span data-ttu-id="99e07-106">Polecenie cmdlet **Remove-AzLoadBalancerInboundNatRuleConfig** usuwa konfigurację reguły translacji adresów sieciowych (NAT) ze składnika Azure Load równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99e07-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="99e07-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99e07-107">EXAMPLES</span></span>

### <span data-ttu-id="99e07-108">1: Usuwanie reguły ruchu przychodzącego NAT z modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="99e07-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="99e07-109">Pierwsze polecenie ładuje już istniejący moduł równoważenia obciążenia o nazwie "mylb" i zapisuje go w zmiennej $load modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99e07-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="99e07-110">Drugie polecenie usuwa regułę ruchu przychodzącego NAT skojarzoną z tym modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="99e07-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="99e07-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99e07-111">PARAMETERS</span></span>

### <span data-ttu-id="99e07-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e07-112">-DefaultProfile</span></span>
<span data-ttu-id="99e07-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99e07-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99e07-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="99e07-114">-LoadBalancer</span></span>
<span data-ttu-id="99e07-115">Określa obiekt **modułu równoważenia obciążenia** zawierający konfigurację reguły przychodzącego NAT, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99e07-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99e07-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="99e07-116">-Name</span></span>
<span data-ttu-id="99e07-117">Określa nazwę konfiguracji przychodzącej reguły NAT, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99e07-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="99e07-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99e07-118">-Confirm</span></span>
<span data-ttu-id="99e07-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99e07-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99e07-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99e07-120">-WhatIf</span></span>
<span data-ttu-id="99e07-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99e07-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99e07-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="99e07-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99e07-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e07-123">CommonParameters</span></span>
<span data-ttu-id="99e07-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e07-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e07-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e07-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e07-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99e07-126">INPUTS</span></span>

### <span data-ttu-id="99e07-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99e07-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="99e07-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99e07-128">OUTPUTS</span></span>

### <span data-ttu-id="99e07-129">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="99e07-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="99e07-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99e07-130">NOTES</span></span>

## <span data-ttu-id="99e07-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99e07-131">RELATED LINKS</span></span>

[<span data-ttu-id="99e07-132">Dodaj-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99e07-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="99e07-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99e07-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="99e07-134">Nowe — AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99e07-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="99e07-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="99e07-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


