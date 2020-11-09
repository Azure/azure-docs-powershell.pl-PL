---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318019"
---
# <span data-ttu-id="229d7-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="229d7-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="229d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="229d7-102">SYNOPSIS</span></span>
<span data-ttu-id="229d7-103">Tworzy regułę rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="229d7-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="229d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="229d7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="229d7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="229d7-105">DESCRIPTION</span></span>
<span data-ttu-id="229d7-106">Polecenie cmdlet **New-AzApplicationGatewayRewriteRuleSet** umożliwia utworzenie reguły ponownego zapisu dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="229d7-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="229d7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="229d7-107">EXAMPLES</span></span>

### <span data-ttu-id="229d7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="229d7-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="229d7-109">To polecenie powoduje utworzenie zestawu reguł ponownej edycji o nazwie ruleset1 i zapisanie wyniku w zmiennej o nazwie $ruleset.</span><span class="sxs-lookup"><span data-stu-id="229d7-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="229d7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="229d7-110">PARAMETERS</span></span>

### <span data-ttu-id="229d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229d7-111">-DefaultProfile</span></span>
<span data-ttu-id="229d7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="229d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="229d7-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="229d7-113">-Name</span></span>
<span data-ttu-id="229d7-114">Nazwa RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="229d7-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="229d7-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="229d7-115">-RewriteRule</span></span>
<span data-ttu-id="229d7-116">Lista reguł ponownej edycji</span><span class="sxs-lookup"><span data-stu-id="229d7-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="229d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229d7-117">CommonParameters</span></span>
<span data-ttu-id="229d7-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229d7-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="229d7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229d7-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="229d7-120">INPUTS</span></span>

### <span data-ttu-id="229d7-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="229d7-121">None</span></span>

## <span data-ttu-id="229d7-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="229d7-122">OUTPUTS</span></span>

### <span data-ttu-id="229d7-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="229d7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="229d7-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="229d7-124">NOTES</span></span>

## <span data-ttu-id="229d7-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="229d7-125">RELATED LINKS</span></span>

[<span data-ttu-id="229d7-126">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="229d7-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="229d7-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="229d7-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="229d7-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="229d7-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="229d7-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="229d7-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="229d7-130">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="229d7-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="229d7-131">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="229d7-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="229d7-132">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="229d7-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
