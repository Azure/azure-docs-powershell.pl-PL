---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 01e132dab83931a48254bb8483cc794d7c619a6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871223"
---
# <span data-ttu-id="a6e38-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e38-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a6e38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6e38-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e38-103">Usuwa konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a6e38-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a6e38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6e38-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6e38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a6e38-105">DESCRIPTION</span></span>
<span data-ttu-id="a6e38-106">Polecenie cmdlet **Remove-AzLoadBalancerRuleConfig** usuwa konfigurację reguły dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e38-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a6e38-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6e38-107">EXAMPLES</span></span>

### <span data-ttu-id="a6e38-108">Przykład 1: Usuwanie konfiguracji reguły z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a6e38-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a6e38-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a6e38-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a6e38-110">Drugie polecenie usuwa konfigurację reguły o nazwie MyLBruleName z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a6e38-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a6e38-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6e38-111">PARAMETERS</span></span>

### <span data-ttu-id="a6e38-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e38-112">-DefaultProfile</span></span>
<span data-ttu-id="a6e38-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e38-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6e38-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a6e38-114">-LoadBalancer</span></span>
<span data-ttu-id="a6e38-115">Określa obiekt **modułu równoważenia obciążenia** , który zawiera konfigurację reguły, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6e38-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6e38-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6e38-116">-Name</span></span>
<span data-ttu-id="a6e38-117">Określa nazwę konfiguracji reguły modułu równoważenia obciążenia, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6e38-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a6e38-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6e38-118">-Confirm</span></span>
<span data-ttu-id="a6e38-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6e38-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6e38-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6e38-120">-WhatIf</span></span>
<span data-ttu-id="a6e38-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6e38-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6e38-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a6e38-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6e38-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e38-123">CommonParameters</span></span>
<span data-ttu-id="a6e38-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6e38-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e38-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6e38-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e38-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6e38-126">INPUTS</span></span>

### <span data-ttu-id="a6e38-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6e38-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a6e38-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6e38-128">OUTPUTS</span></span>

### <span data-ttu-id="a6e38-129">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6e38-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a6e38-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6e38-130">NOTES</span></span>

## <span data-ttu-id="a6e38-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6e38-131">RELATED LINKS</span></span>

[<span data-ttu-id="a6e38-132">Dodaj-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e38-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a6e38-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a6e38-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a6e38-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e38-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a6e38-135">Nowe — AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e38-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a6e38-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a6e38-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


