---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241122"
---
# <span data-ttu-id="9e3ec-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e3ec-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="9e3ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3ec-103">Powoduje dodanie zestawu reguł ponownego w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="9e3ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e3ec-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e3ec-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e3ec-105">DESCRIPTION</span></span>
<span data-ttu-id="9e3ec-106">Polecenie **cmdlet Add-AzApplicationGatewayRewriteRuleSet** powoduje dodanie zestawu reguł ponownego w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="9e3ec-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e3ec-107">EXAMPLES</span></span>

### <span data-ttu-id="9e3ec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e3ec-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="9e3ec-109">Pierwsze polecenie pobiera bramę aplikacji i zapisuje ją w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9e3ec-110">Drugie polecenie dodaje zestaw reguł ponownego ustawienia do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="9e3ec-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e3ec-111">PARAMETERS</span></span>

### <span data-ttu-id="9e3ec-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e3ec-112">-ApplicationGateway</span></span>
<span data-ttu-id="9e3ec-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e3ec-113">The applicationGateway</span></span>

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

### <span data-ttu-id="9e3ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3ec-114">-DefaultProfile</span></span>
<span data-ttu-id="9e3ec-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3ec-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9e3ec-116">-Name</span></span>
<span data-ttu-id="9e3ec-117">Nazwa zestawu rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e3ec-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="9e3ec-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="9e3ec-118">-RewriteRule</span></span>
<span data-ttu-id="9e3ec-119">Lista reguł ponownego edyt-</span><span class="sxs-lookup"><span data-stu-id="9e3ec-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="9e3ec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3ec-120">CommonParameters</span></span>
<span data-ttu-id="9e3ec-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3ec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3ec-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3ec-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3ec-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e3ec-123">INPUTS</span></span>

### <span data-ttu-id="9e3ec-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e3ec-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e3ec-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e3ec-125">OUTPUTS</span></span>

### <span data-ttu-id="9e3ec-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e3ec-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e3ec-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e3ec-127">NOTES</span></span>

## <span data-ttu-id="9e3ec-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e3ec-128">RELATED LINKS</span></span>

[<span data-ttu-id="9e3ec-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e3ec-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9e3ec-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e3ec-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9e3ec-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e3ec-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9e3ec-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e3ec-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9e3ec-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9e3ec-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="9e3ec-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9e3ec-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="9e3ec-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e3ec-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
