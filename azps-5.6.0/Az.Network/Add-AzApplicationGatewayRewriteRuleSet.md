---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: d657c769a32d7c042a12a56571343885c526eea7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982497"
---
# <span data-ttu-id="35498-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35498-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="35498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35498-102">SYNOPSIS</span></span>
<span data-ttu-id="35498-103">Powoduje dodanie zestawu reguł ponownego w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="35498-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="35498-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="35498-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35498-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="35498-105">DESCRIPTION</span></span>
<span data-ttu-id="35498-106">Polecenie **cmdlet Add-AzApplicationGatewayRewriteRuleSet** powoduje dodanie zestawu reguł ponownego w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="35498-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="35498-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="35498-107">EXAMPLES</span></span>

### <span data-ttu-id="35498-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35498-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="35498-109">Pierwsze polecenie pobiera bramę aplikacji i zapisuje je w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="35498-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="35498-110">Drugie polecenie dodaje zestaw reguł ponownego ustawienia do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="35498-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="35498-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35498-111">PARAMETERS</span></span>

### <span data-ttu-id="35498-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35498-112">-ApplicationGateway</span></span>
<span data-ttu-id="35498-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="35498-113">The applicationGateway</span></span>

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

### <span data-ttu-id="35498-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35498-114">-DefaultProfile</span></span>
<span data-ttu-id="35498-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="35498-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35498-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="35498-116">-Name</span></span>
<span data-ttu-id="35498-117">Nazwa zestawu rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35498-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="35498-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="35498-118">-RewriteRule</span></span>
<span data-ttu-id="35498-119">Lista reguł ponownego agagenia</span><span class="sxs-lookup"><span data-stu-id="35498-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="35498-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35498-120">CommonParameters</span></span>
<span data-ttu-id="35498-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35498-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35498-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35498-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35498-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35498-123">INPUTS</span></span>

### <span data-ttu-id="35498-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35498-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35498-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35498-125">OUTPUTS</span></span>

### <span data-ttu-id="35498-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35498-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35498-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="35498-127">NOTES</span></span>

## <span data-ttu-id="35498-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35498-128">RELATED LINKS</span></span>

[<span data-ttu-id="35498-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35498-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="35498-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35498-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="35498-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35498-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="35498-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35498-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="35498-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="35498-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="35498-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="35498-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="35498-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="35498-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
