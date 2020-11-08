---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052752"
---
# <span data-ttu-id="7597e-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7597e-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="7597e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7597e-102">SYNOPSIS</span></span>
<span data-ttu-id="7597e-103">Dodaje regułę ponownej edycji do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7597e-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="7597e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7597e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7597e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7597e-105">DESCRIPTION</span></span>
<span data-ttu-id="7597e-106">Polecenie cmdlet **Add-AzApplicationGatewayRewriteRuleSet** umożliwia dodanie reguły ponownego zapisu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7597e-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="7597e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7597e-107">EXAMPLES</span></span>

### <span data-ttu-id="7597e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7597e-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="7597e-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7597e-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7597e-110">Drugie polecenie dodaje regułę ponownej edycji do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7597e-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="7597e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7597e-111">PARAMETERS</span></span>

### <span data-ttu-id="7597e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7597e-112">-ApplicationGateway</span></span>
<span data-ttu-id="7597e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7597e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7597e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7597e-114">-DefaultProfile</span></span>
<span data-ttu-id="7597e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7597e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7597e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7597e-116">-Name</span></span>
<span data-ttu-id="7597e-117">Nazwa RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7597e-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="7597e-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="7597e-118">-RewriteRule</span></span>
<span data-ttu-id="7597e-119">Lista reguł ponownej edycji</span><span class="sxs-lookup"><span data-stu-id="7597e-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="7597e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7597e-120">CommonParameters</span></span>
<span data-ttu-id="7597e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7597e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7597e-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7597e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7597e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7597e-123">INPUTS</span></span>

### <span data-ttu-id="7597e-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7597e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7597e-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7597e-125">OUTPUTS</span></span>

### <span data-ttu-id="7597e-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7597e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7597e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7597e-127">NOTES</span></span>

## <span data-ttu-id="7597e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7597e-128">RELATED LINKS</span></span>

[<span data-ttu-id="7597e-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7597e-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7597e-130">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7597e-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7597e-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7597e-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7597e-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7597e-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7597e-133">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7597e-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="7597e-134">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7597e-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="7597e-135">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7597e-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
