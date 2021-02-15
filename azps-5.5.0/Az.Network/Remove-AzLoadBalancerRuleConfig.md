---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186947"
---
# <span data-ttu-id="7e951-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e951-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="7e951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e951-102">SYNOPSIS</span></span>
<span data-ttu-id="7e951-103">Usuwa konfigurację reguły dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7e951-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="7e951-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7e951-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e951-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7e951-105">DESCRIPTION</span></span>
<span data-ttu-id="7e951-106">Polecenie **cmdlet Remove-AzLoadBalancerRuleConfig** usuwa konfigurację reguły dla narzędzia do równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7e951-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="7e951-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7e951-107">EXAMPLES</span></span>

### <span data-ttu-id="7e951-108">Przykład 1. Usuwanie konfiguracji reguły z urządzenia do równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7e951-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="7e951-109">Pierwsze polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer, a następnie przechowuje je w $loadbalancer ładowania.</span><span class="sxs-lookup"><span data-stu-id="7e951-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="7e951-110">Drugie polecenie usuwa konfigurację reguł o nazwie MyLBruleName z równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="7e951-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="7e951-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e951-111">PARAMETERS</span></span>

### <span data-ttu-id="7e951-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e951-112">-DefaultProfile</span></span>
<span data-ttu-id="7e951-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e951-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e951-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7e951-114">-LoadBalancer</span></span>
<span data-ttu-id="7e951-115">Określa obiekt **LoadBalancer** zawierający konfigurację reguły usuwaną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e951-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7e951-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7e951-116">-Name</span></span>
<span data-ttu-id="7e951-117">Określa nazwę konfiguracji reguły równoważenia obciążenia, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e951-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7e951-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e951-118">-Confirm</span></span>
<span data-ttu-id="7e951-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7e951-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e951-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e951-120">-WhatIf</span></span>
<span data-ttu-id="7e951-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e951-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e951-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7e951-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e951-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e951-123">CommonParameters</span></span>
<span data-ttu-id="7e951-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e951-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e951-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e951-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e951-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e951-126">INPUTS</span></span>

### <span data-ttu-id="7e951-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7e951-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7e951-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e951-128">OUTPUTS</span></span>

### <span data-ttu-id="7e951-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7e951-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7e951-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7e951-130">NOTES</span></span>

## <span data-ttu-id="7e951-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e951-131">RELATED LINKS</span></span>

[<span data-ttu-id="7e951-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e951-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7e951-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7e951-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7e951-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e951-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7e951-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e951-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="7e951-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7e951-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


