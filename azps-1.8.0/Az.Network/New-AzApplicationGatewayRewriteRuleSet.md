---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 1ed5c90d4c53769d53cd645b2e5bced7bdec4ce8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709349"
---
# <span data-ttu-id="70af5-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70af5-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="70af5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70af5-102">SYNOPSIS</span></span>
<span data-ttu-id="70af5-103">Tworzy regułę rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="70af5-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="70af5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70af5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70af5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="70af5-105">DESCRIPTION</span></span>
<span data-ttu-id="70af5-106">Polecenie cmdlet **New-AzApplicationGatewayRewriteRuleSet** umożliwia utworzenie reguły ponownego zapisu dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="70af5-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="70af5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70af5-107">EXAMPLES</span></span>

### <span data-ttu-id="70af5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70af5-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="70af5-109">To polecenie powoduje utworzenie zestawu reguł ponownej edycji o nazwie ruleset1 i zapisanie wyniku w zmiennej o nazwie $ruleset.</span><span class="sxs-lookup"><span data-stu-id="70af5-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="70af5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70af5-110">PARAMETERS</span></span>

### <span data-ttu-id="70af5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70af5-111">-DefaultProfile</span></span>
<span data-ttu-id="70af5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70af5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70af5-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70af5-113">-Name</span></span>
<span data-ttu-id="70af5-114">Nazwa RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70af5-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="70af5-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="70af5-115">-RewriteRule</span></span>
<span data-ttu-id="70af5-116">Lista reguł ponownej edycji</span><span class="sxs-lookup"><span data-stu-id="70af5-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="70af5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70af5-117">CommonParameters</span></span>
<span data-ttu-id="70af5-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70af5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70af5-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70af5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70af5-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70af5-120">INPUTS</span></span>

### <span data-ttu-id="70af5-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="70af5-121">None</span></span>

## <span data-ttu-id="70af5-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70af5-122">OUTPUTS</span></span>

### <span data-ttu-id="70af5-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70af5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="70af5-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70af5-124">NOTES</span></span>

## <span data-ttu-id="70af5-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70af5-125">RELATED LINKS</span></span>

[<span data-ttu-id="70af5-126">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70af5-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="70af5-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70af5-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="70af5-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70af5-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="70af5-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="70af5-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="70af5-130">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="70af5-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="70af5-131">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="70af5-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="70af5-132">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="70af5-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
