---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: cc9a79b424d6ad81804aaed0d941ca017463abba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547451"
---
# <span data-ttu-id="9145c-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9145c-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="9145c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9145c-102">SYNOPSIS</span></span>
<span data-ttu-id="9145c-103">Usuwa konfigurację reguły ruchu wychodzącego z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9145c-103">Removes an outbound rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9145c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9145c-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9145c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9145c-105">DESCRIPTION</span></span>
<span data-ttu-id="9145c-106">Polecenie cmdlet **Remove-AzureRmLoadBalancerOutboundRuleConfig** usuwa konfigurację reguły wychodzącą z modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9145c-106">The **Remove-AzureRmLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="9145c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9145c-107">EXAMPLES</span></span>

### <span data-ttu-id="9145c-108">Przykład 1: Usuwanie reguły wychodzącej z modułu równoważenia obciążenia platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9145c-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzureRmLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzureRmLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="9145c-109">Pierwsze polecenie uzyskuje moduł równoważenia obciążenia skojarzony z konfiguracją reguły ruchu wychodzącego, którą chcesz usunąć, a następnie zapisze ją w zmiennej $slb.</span><span class="sxs-lookup"><span data-stu-id="9145c-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="9145c-110">Drugie polecenie usuwa konfigurację skojarzonej reguły wychodzącej z modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9145c-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="9145c-111">W trzecim poleceniu jest aktualizowana usługa równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9145c-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="9145c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9145c-112">PARAMETERS</span></span>

### <span data-ttu-id="9145c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9145c-113">-DefaultProfile</span></span>
<span data-ttu-id="9145c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9145c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9145c-115">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="9145c-115">-LoadBalancer</span></span>
<span data-ttu-id="9145c-116">Odwołanie do zasobu modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="9145c-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="9145c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9145c-117">-Name</span></span>
<span data-ttu-id="9145c-118">Nazwa reguły ruchu wychodzącego</span><span class="sxs-lookup"><span data-stu-id="9145c-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9145c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9145c-119">-Confirm</span></span>
<span data-ttu-id="9145c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9145c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9145c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9145c-121">-WhatIf</span></span>
<span data-ttu-id="9145c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9145c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9145c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9145c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9145c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9145c-124">CommonParameters</span></span>
<span data-ttu-id="9145c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9145c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9145c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9145c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9145c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9145c-127">INPUTS</span></span>

### <span data-ttu-id="9145c-128">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9145c-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9145c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9145c-129">OUTPUTS</span></span>

### <span data-ttu-id="9145c-130">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9145c-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9145c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9145c-131">NOTES</span></span>

## <span data-ttu-id="9145c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9145c-132">RELATED LINKS</span></span>
