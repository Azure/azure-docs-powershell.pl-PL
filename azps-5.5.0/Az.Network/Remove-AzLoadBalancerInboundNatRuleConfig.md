---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 76cf9e2624c812d99702823b303e4e6427845670
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189587"
---
# <span data-ttu-id="a9eb8-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a9eb8-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a9eb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="a9eb8-103">Usuwa konfigurację reguły nat ruchu przychodzącego z urządzenia do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="a9eb8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9eb8-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9eb8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9eb8-105">DESCRIPTION</span></span>
<span data-ttu-id="a9eb8-106">Polecenie **cmdlet Remove-AzLoadBalancerInboundNatRuleConfig** usuwa konfigurację reguły translacji adresów sieciowych ruchu przychodzącego z narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="a9eb8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9eb8-107">EXAMPLES</span></span>

### <span data-ttu-id="a9eb8-108">1. Usuwanie reguły nat ruchu przychodzącego z narzędzia do równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a9eb8-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a9eb8-109">Pierwsze polecenie ładuje już istniejący równoważenie obciążenia o nazwie "mójlb" i przechowuje je w $load równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="a9eb8-110">Drugie polecenie usuwa regułę nat ruchu przychodzącego skojarzoną z tym równoważeniem obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="a9eb8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9eb8-111">PARAMETERS</span></span>

### <span data-ttu-id="a9eb8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9eb8-112">-DefaultProfile</span></span>
<span data-ttu-id="a9eb8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9eb8-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9eb8-114">-LoadBalancer</span></span>
<span data-ttu-id="a9eb8-115">Określa obiekt **LoadBalancer** zawierający konfigurację reguły przychodzącego serwera NAT usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a9eb8-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9eb8-116">-Name</span></span>
<span data-ttu-id="a9eb8-117">Określa nazwę konfiguracji reguły nat ruchu przychodzącego, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a9eb8-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9eb8-118">-Confirm</span></span>
<span data-ttu-id="a9eb8-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9eb8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9eb8-120">-WhatIf</span></span>
<span data-ttu-id="a9eb8-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9eb8-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9eb8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9eb8-123">CommonParameters</span></span>
<span data-ttu-id="a9eb8-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9eb8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9eb8-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9eb8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9eb8-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9eb8-126">INPUTS</span></span>

### <span data-ttu-id="a9eb8-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9eb8-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a9eb8-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9eb8-128">OUTPUTS</span></span>

### <span data-ttu-id="a9eb8-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9eb8-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a9eb8-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9eb8-130">NOTES</span></span>

## <span data-ttu-id="a9eb8-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9eb8-131">RELATED LINKS</span></span>

[<span data-ttu-id="a9eb8-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a9eb8-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a9eb8-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a9eb8-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a9eb8-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a9eb8-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a9eb8-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a9eb8-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


