---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 934c69071e90ebb1a38bf4e1fda5e631364ab87b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003466"
---
# <span data-ttu-id="5c37d-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c37d-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="5c37d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c37d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c37d-103">Modyfikuje zestaw reguł dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c37d-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="5c37d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5c37d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c37d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5c37d-105">DESCRIPTION</span></span>
<span data-ttu-id="5c37d-106">Polecenie **cmdlet Set-AzApplicationGatewayRewriteRuleSet** modyfikuje regułę routingu żądania.</span><span class="sxs-lookup"><span data-stu-id="5c37d-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="5c37d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5c37d-107">EXAMPLES</span></span>

### <span data-ttu-id="5c37d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c37d-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="5c37d-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c37d-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5c37d-110">Drugie polecenie modyfikuje zestaw reguł ponownego agwania dla bramy aplikacji w celu używania reguł ponownego określonej w $rule aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c37d-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="5c37d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c37d-111">PARAMETERS</span></span>

### <span data-ttu-id="5c37d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c37d-112">-ApplicationGateway</span></span>
<span data-ttu-id="5c37d-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c37d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="5c37d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c37d-114">-DefaultProfile</span></span>
<span data-ttu-id="5c37d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c37d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c37d-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5c37d-116">-Name</span></span>
<span data-ttu-id="5c37d-117">Nazwa zestawu rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c37d-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="5c37d-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="5c37d-118">-RewriteRule</span></span>
<span data-ttu-id="5c37d-119">Lista reguł ponownego agagenia</span><span class="sxs-lookup"><span data-stu-id="5c37d-119">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c37d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c37d-120">CommonParameters</span></span>
<span data-ttu-id="5c37d-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c37d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c37d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c37d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c37d-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c37d-123">INPUTS</span></span>

### <span data-ttu-id="5c37d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c37d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c37d-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c37d-125">OUTPUTS</span></span>

### <span data-ttu-id="5c37d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c37d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c37d-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5c37d-127">NOTES</span></span>

## <span data-ttu-id="5c37d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c37d-128">RELATED LINKS</span></span>

[<span data-ttu-id="5c37d-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c37d-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5c37d-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c37d-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5c37d-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c37d-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5c37d-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c37d-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5c37d-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5c37d-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="5c37d-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5c37d-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="5c37d-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c37d-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
