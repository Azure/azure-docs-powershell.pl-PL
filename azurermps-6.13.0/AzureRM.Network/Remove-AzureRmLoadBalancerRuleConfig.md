---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b51c7300296644ffeda75d1fb9e4cf695ff61def
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527814"
---
# <span data-ttu-id="f542d-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f542d-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f542d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f542d-102">SYNOPSIS</span></span>
<span data-ttu-id="f542d-103">Usuwa konfigurację reguły dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="f542d-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f542d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f542d-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f542d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f542d-105">DESCRIPTION</span></span>
<span data-ttu-id="f542d-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerRuleConfig** usuwa konfigurację reguły dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f542d-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f542d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f542d-107">EXAMPLES</span></span>

### <span data-ttu-id="f542d-108">Przykład 1: Usuwanie konfiguracji reguły z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f542d-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="f542d-109">Pierwsze polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer, a następnie zapisuje ją w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f542d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="f542d-110">Drugie polecenie usuwa konfigurację reguły o nazwie MyLBruleName z modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="f542d-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="f542d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f542d-111">PARAMETERS</span></span>

### <span data-ttu-id="f542d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f542d-112">-DefaultProfile</span></span>
<span data-ttu-id="f542d-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f542d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f542d-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="f542d-114">-LoadBalancer</span></span>
<span data-ttu-id="f542d-115">Określa obiekt **modułu równoważenia obciążenia** , który zawiera konfigurację reguły, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f542d-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f542d-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f542d-116">-Name</span></span>
<span data-ttu-id="f542d-117">Określa nazwę konfiguracji reguły modułu równoważenia obciążenia, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f542d-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f542d-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f542d-118">-Confirm</span></span>
<span data-ttu-id="f542d-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f542d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f542d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f542d-120">-WhatIf</span></span>
<span data-ttu-id="f542d-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f542d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f542d-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f542d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f542d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f542d-123">CommonParameters</span></span>
<span data-ttu-id="f542d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f542d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f542d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f542d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f542d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f542d-126">INPUTS</span></span>

### <span data-ttu-id="f542d-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f542d-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="f542d-128">Parametry: moduł równoważenia obciążenia (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f542d-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="f542d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f542d-129">OUTPUTS</span></span>

### <span data-ttu-id="f542d-130">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f542d-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f542d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f542d-131">NOTES</span></span>

## <span data-ttu-id="f542d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f542d-132">RELATED LINKS</span></span>

[<span data-ttu-id="f542d-133">Dodaj-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f542d-133">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f542d-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f542d-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f542d-135">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f542d-135">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f542d-136">Nowe — AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f542d-136">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f542d-137">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f542d-137">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


