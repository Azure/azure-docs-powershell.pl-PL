---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202875"
---
# <span data-ttu-id="0befe-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0befe-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="0befe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0befe-102">SYNOPSIS</span></span>
<span data-ttu-id="0befe-103">Tworzy regułę ponownego tworzenia dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0befe-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="0befe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0befe-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0befe-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0befe-105">DESCRIPTION</span></span>
<span data-ttu-id="0befe-106">**Polecenie cmdlet New-AzApplicationGatewayRewriteRule** tworzy regułę ponownego tworzenia dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0befe-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="0befe-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0befe-107">EXAMPLES</span></span>

### <span data-ttu-id="0befe-108">Przykład 1. Tworzenie reguły ponownego tworzenia dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="0befe-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="0befe-109">To polecenie tworzy regułę o nazwie reguła1 i zapisuje wynik w zmiennej o nazwie $rule.</span><span class="sxs-lookup"><span data-stu-id="0befe-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="0befe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0befe-110">PARAMETERS</span></span>

### <span data-ttu-id="0befe-111">- ActionSet</span><span class="sxs-lookup"><span data-stu-id="0befe-111">-ActionSet</span></span>
<span data-ttu-id="0befe-112">Zestaw akcji reguły ponownego edytowania</span><span class="sxs-lookup"><span data-stu-id="0befe-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="0befe-113">— Warunek</span><span class="sxs-lookup"><span data-stu-id="0befe-113">-Condition</span></span>
<span data-ttu-id="0befe-114">Warunek wykonania reguły ponownego edytu</span><span class="sxs-lookup"><span data-stu-id="0befe-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="0befe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0befe-115">-DefaultProfile</span></span>
<span data-ttu-id="0befe-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0befe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0befe-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0befe-117">-Name</span></span>
<span data-ttu-id="0befe-118">Nazwa rewriteRule</span><span class="sxs-lookup"><span data-stu-id="0befe-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="0befe-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="0befe-119">-RuleSequence</span></span>
<span data-ttu-id="0befe-120">Kolejność reguł tej reguły ponownego agowania w zestawie reguł ponownego edytowania</span><span class="sxs-lookup"><span data-stu-id="0befe-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="0befe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0befe-121">CommonParameters</span></span>
<span data-ttu-id="0befe-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0befe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0befe-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0befe-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0befe-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0befe-124">INPUTS</span></span>

### <span data-ttu-id="0befe-125">Brak</span><span class="sxs-lookup"><span data-stu-id="0befe-125">None</span></span>

## <span data-ttu-id="0befe-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0befe-126">OUTPUTS</span></span>

### <span data-ttu-id="0befe-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0befe-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="0befe-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0befe-128">NOTES</span></span>

## <span data-ttu-id="0befe-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0befe-129">RELATED LINKS</span></span>

[<span data-ttu-id="0befe-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0befe-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0befe-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0befe-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0befe-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0befe-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0befe-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0befe-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0befe-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0befe-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0befe-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0befe-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="0befe-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0befe-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
