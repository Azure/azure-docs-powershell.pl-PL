---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 8bd540c30551451bd729126c35c4d778c700591f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001121"
---
# <span data-ttu-id="6ea93-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ea93-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="6ea93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ea93-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea93-103">Tworzy regułę routingu żądania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6ea93-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="6ea93-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6ea93-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ea93-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6ea93-105">DESCRIPTION</span></span>
<span data-ttu-id="6ea93-106">**Polecenie cmdlet New-AzApplicationGatewayRewriteRuleSet** tworzy zestaw reguł ponownego tworzenia dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ea93-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="6ea93-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6ea93-107">EXAMPLES</span></span>

### <span data-ttu-id="6ea93-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ea93-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="6ea93-109">To polecenie tworzy zestaw reguł o nazwie reguły ponownej o nazwie ruleset1 i przechowuje wynik w zmiennej o nazwie $ruleset.</span><span class="sxs-lookup"><span data-stu-id="6ea93-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="6ea93-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ea93-110">PARAMETERS</span></span>

### <span data-ttu-id="6ea93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea93-111">-DefaultProfile</span></span>
<span data-ttu-id="6ea93-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ea93-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ea93-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6ea93-113">-Name</span></span>
<span data-ttu-id="6ea93-114">Nazwa zestawu rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ea93-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="6ea93-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="6ea93-115">-RewriteRule</span></span>
<span data-ttu-id="6ea93-116">Lista reguł ponownego agagenia</span><span class="sxs-lookup"><span data-stu-id="6ea93-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="6ea93-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea93-117">CommonParameters</span></span>
<span data-ttu-id="6ea93-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ea93-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea93-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ea93-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea93-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ea93-120">INPUTS</span></span>

### <span data-ttu-id="6ea93-121">Brak</span><span class="sxs-lookup"><span data-stu-id="6ea93-121">None</span></span>

## <span data-ttu-id="6ea93-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ea93-122">OUTPUTS</span></span>

### <span data-ttu-id="6ea93-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ea93-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="6ea93-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6ea93-124">NOTES</span></span>

## <span data-ttu-id="6ea93-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ea93-125">RELATED LINKS</span></span>

[<span data-ttu-id="6ea93-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ea93-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6ea93-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ea93-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6ea93-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ea93-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6ea93-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6ea93-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6ea93-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6ea93-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="6ea93-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6ea93-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="6ea93-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ea93-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
