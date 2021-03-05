---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 935e2df3de68d9ab8444cd1037d5c48951d6a335
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994071"
---
# <span data-ttu-id="b852b-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b852b-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b852b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b852b-102">SYNOPSIS</span></span>
<span data-ttu-id="b852b-103">Pobiera zestaw reguł ponownego ustawienia bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b852b-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="b852b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b852b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b852b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b852b-105">DESCRIPTION</span></span>
<span data-ttu-id="b852b-106">Pobiera zestaw reguł ponownego ustawienia bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b852b-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="b852b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b852b-107">EXAMPLES</span></span>

### <span data-ttu-id="b852b-108">Przykład 1. Uzyskiwanie określonego zestawu reguł ponownego ustawienia</span><span class="sxs-lookup"><span data-stu-id="b852b-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="b852b-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i przechowuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b852b-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b852b-110">Drugie polecenie pobiera zestaw reguł o nazwie Reguła o nazwie "RuleSet01" z bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b852b-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="b852b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b852b-111">PARAMETERS</span></span>

### <span data-ttu-id="b852b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b852b-112">-ApplicationGateway</span></span>
<span data-ttu-id="b852b-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b852b-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b852b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b852b-114">-DefaultProfile</span></span>
<span data-ttu-id="b852b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b852b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b852b-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b852b-116">-Name</span></span>
<span data-ttu-id="b852b-117">Nazwa bramy aplikacji RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b852b-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b852b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b852b-118">CommonParameters</span></span>
<span data-ttu-id="b852b-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b852b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b852b-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b852b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b852b-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b852b-121">INPUTS</span></span>

### <span data-ttu-id="b852b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b852b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b852b-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b852b-123">OUTPUTS</span></span>

### <span data-ttu-id="b852b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b852b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b852b-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b852b-125">NOTES</span></span>

## <span data-ttu-id="b852b-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b852b-126">RELATED LINKS</span></span>

[<span data-ttu-id="b852b-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b852b-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b852b-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b852b-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b852b-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b852b-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b852b-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b852b-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b852b-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b852b-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b852b-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b852b-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b852b-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b852b-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
