---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063948"
---
# <span data-ttu-id="79255-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="79255-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="79255-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79255-102">SYNOPSIS</span></span>
<span data-ttu-id="79255-103">Tworzy regułę ponownej edycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="79255-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="79255-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79255-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79255-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79255-105">DESCRIPTION</span></span>
<span data-ttu-id="79255-106">Polecenie cmdlet **New-AzApplicationGatewayRewriteRule** umożliwia utworzenie reguły ponownego zapisu dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79255-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="79255-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79255-107">EXAMPLES</span></span>

### <span data-ttu-id="79255-108">Przykład 1: Tworzenie reguły ponownego zapisu dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="79255-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="79255-109">To polecenie umożliwia utworzenie reguły zapisu o nazwie RULE1 i zapisanie wyniku w zmiennej o nazwie $rule.</span><span class="sxs-lookup"><span data-stu-id="79255-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="79255-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79255-110">PARAMETERS</span></span>

### <span data-ttu-id="79255-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="79255-111">-ActionSet</span></span>
<span data-ttu-id="79255-112">ActionSet reguły ponownej edycji</span><span class="sxs-lookup"><span data-stu-id="79255-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="79255-113">-Warunek</span><span class="sxs-lookup"><span data-stu-id="79255-113">-Condition</span></span>
<span data-ttu-id="79255-114">Warunek reguły ponownego zapisu do wykonania</span><span class="sxs-lookup"><span data-stu-id="79255-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="79255-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79255-115">-DefaultProfile</span></span>
<span data-ttu-id="79255-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79255-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79255-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79255-117">-Name</span></span>
<span data-ttu-id="79255-118">Nazwa RewriteRule</span><span class="sxs-lookup"><span data-stu-id="79255-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="79255-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="79255-119">-RuleSequence</span></span>
<span data-ttu-id="79255-120">Kolejność reguły tej reguły ponownie zapisu w zestawie reguł ponownej edycji</span><span class="sxs-lookup"><span data-stu-id="79255-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="79255-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79255-121">CommonParameters</span></span>
<span data-ttu-id="79255-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79255-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79255-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79255-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79255-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79255-124">INPUTS</span></span>

### <span data-ttu-id="79255-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="79255-125">None</span></span>

## <span data-ttu-id="79255-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79255-126">OUTPUTS</span></span>

### <span data-ttu-id="79255-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="79255-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="79255-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79255-128">NOTES</span></span>

## <span data-ttu-id="79255-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79255-129">RELATED LINKS</span></span>

[<span data-ttu-id="79255-130">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79255-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79255-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79255-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79255-132">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79255-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79255-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79255-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79255-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="79255-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="79255-135">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="79255-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="79255-136">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="79255-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
