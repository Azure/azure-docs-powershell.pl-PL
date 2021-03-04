---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 2c5fa5f4c12a44d1efc12e75dfa3901dce061f8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008769"
---
# <span data-ttu-id="2f254-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2f254-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="2f254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f254-102">SYNOPSIS</span></span>
<span data-ttu-id="2f254-103">Tworzy zestaw akcji reguły ponownego tworzenia dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2f254-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="2f254-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2f254-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f254-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2f254-105">DESCRIPTION</span></span>
<span data-ttu-id="2f254-106">**Polecenie cmdlet New-AzApplicationGatewayRewriteRuleActionSet** tworzy akcję ponownego wstawienia reguły dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2f254-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="2f254-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2f254-107">EXAMPLES</span></span>

### <span data-ttu-id="2f254-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f254-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="2f254-109">To polecenie tworzy zestaw akcji reguły ponownego tworzenia i przechowuje wynik w zmiennej o nazwie $action.</span><span class="sxs-lookup"><span data-stu-id="2f254-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="2f254-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f254-110">PARAMETERS</span></span>

### <span data-ttu-id="2f254-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f254-111">-DefaultProfile</span></span>
<span data-ttu-id="2f254-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f254-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f254-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f254-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="2f254-114">Lista konfiguracji nagłówków żądań</span><span class="sxs-lookup"><span data-stu-id="2f254-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f254-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f254-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="2f254-116">Lista konfiguracji nagłówka odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="2f254-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f254-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f254-117">-UrlConfiguration</span></span>
<span data-ttu-id="2f254-118">Konfiguracja adresu URL dla zestawu akcji</span><span class="sxs-lookup"><span data-stu-id="2f254-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f254-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f254-119">CommonParameters</span></span>
<span data-ttu-id="2f254-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f254-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f254-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f254-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f254-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f254-122">INPUTS</span></span>

### <span data-ttu-id="2f254-123">Brak</span><span class="sxs-lookup"><span data-stu-id="2f254-123">None</span></span>

## <span data-ttu-id="2f254-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f254-124">OUTPUTS</span></span>

### <span data-ttu-id="2f254-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2f254-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="2f254-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2f254-126">NOTES</span></span>

## <span data-ttu-id="2f254-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f254-127">RELATED LINKS</span></span>

[<span data-ttu-id="2f254-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f254-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f254-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f254-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f254-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f254-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f254-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f254-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f254-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f254-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2f254-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2f254-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="2f254-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f254-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="2f254-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f254-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)