---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: a69f5a3a1da8ec2ac8937793051f0361bf5e0681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011898"
---
# <span data-ttu-id="e996a-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e996a-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="e996a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e996a-102">SYNOPSIS</span></span>
<span data-ttu-id="e996a-103">Tworzy regułę ponownego tworzenia dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e996a-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="e996a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e996a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e996a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e996a-105">DESCRIPTION</span></span>
<span data-ttu-id="e996a-106">**Polecenie cmdlet New-AzApplicationGatewayRewriteRule** tworzy regułę ponownego tworzenia dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e996a-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="e996a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e996a-107">EXAMPLES</span></span>

### <span data-ttu-id="e996a-108">Przykład 1. Tworzenie reguły ponownego tworzenia dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e996a-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="e996a-109">To polecenie tworzy regułę o nazwie reguła1 i zapisuje wynik w zmiennej o nazwie $rule.</span><span class="sxs-lookup"><span data-stu-id="e996a-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="e996a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e996a-110">PARAMETERS</span></span>

### <span data-ttu-id="e996a-111">- ActionSet</span><span class="sxs-lookup"><span data-stu-id="e996a-111">-ActionSet</span></span>
<span data-ttu-id="e996a-112">Zestaw akcji reguły ponownego edytowania</span><span class="sxs-lookup"><span data-stu-id="e996a-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e996a-113">— Warunek</span><span class="sxs-lookup"><span data-stu-id="e996a-113">-Condition</span></span>
<span data-ttu-id="e996a-114">Warunek wykonania reguły ponownego edytu</span><span class="sxs-lookup"><span data-stu-id="e996a-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e996a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e996a-115">-DefaultProfile</span></span>
<span data-ttu-id="e996a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e996a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e996a-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e996a-117">-Name</span></span>
<span data-ttu-id="e996a-118">Nazwa rewriteRule</span><span class="sxs-lookup"><span data-stu-id="e996a-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="e996a-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="e996a-119">-RuleSequence</span></span>
<span data-ttu-id="e996a-120">Kolejność reguł tej reguły ponownego agowania w zestawie reguł ponownego edytowania</span><span class="sxs-lookup"><span data-stu-id="e996a-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e996a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e996a-121">CommonParameters</span></span>
<span data-ttu-id="e996a-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e996a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e996a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e996a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e996a-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e996a-124">INPUTS</span></span>

### <span data-ttu-id="e996a-125">Brak</span><span class="sxs-lookup"><span data-stu-id="e996a-125">None</span></span>

## <span data-ttu-id="e996a-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e996a-126">OUTPUTS</span></span>

### <span data-ttu-id="e996a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e996a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="e996a-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e996a-128">NOTES</span></span>

## <span data-ttu-id="e996a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e996a-129">RELATED LINKS</span></span>

[<span data-ttu-id="e996a-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e996a-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e996a-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e996a-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e996a-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e996a-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e996a-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e996a-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e996a-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e996a-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e996a-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e996a-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="e996a-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e996a-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
