---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 84be6aa60ede19e88b98ca9517fa3cbce3872c8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870508"
---
# <span data-ttu-id="26e55-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="26e55-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="26e55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26e55-102">SYNOPSIS</span></span>
<span data-ttu-id="26e55-103">Umożliwia utworzenie akcji reguły ponownej edycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="26e55-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="26e55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26e55-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26e55-105">Opis</span><span class="sxs-lookup"><span data-stu-id="26e55-105">DESCRIPTION</span></span>
<span data-ttu-id="26e55-106">Polecenie cmdlet **New-AzApplicationGatewayRewriteRuleActionSet** umożliwia utworzenie akcji reguły ponownego zapisu dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="26e55-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="26e55-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26e55-107">EXAMPLES</span></span>

### <span data-ttu-id="26e55-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26e55-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="26e55-109">To polecenie umożliwia utworzenie ustawionej akcji przepisywania i zapisanie wyniku w zmiennej o nazwie $action.</span><span class="sxs-lookup"><span data-stu-id="26e55-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="26e55-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26e55-110">PARAMETERS</span></span>

### <span data-ttu-id="26e55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e55-111">-DefaultProfile</span></span>
<span data-ttu-id="26e55-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26e55-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e55-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="26e55-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="26e55-114">Lista konfiguracji nagłówków żądań</span><span class="sxs-lookup"><span data-stu-id="26e55-114">List of request header configurations</span></span>

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

### <span data-ttu-id="26e55-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="26e55-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="26e55-116">Lista konfiguracji nagłówka odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="26e55-116">List of response header configurations</span></span>

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

### <span data-ttu-id="26e55-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e55-117">CommonParameters</span></span>
<span data-ttu-id="26e55-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e55-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e55-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e55-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e55-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26e55-120">INPUTS</span></span>

### <span data-ttu-id="26e55-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="26e55-121">None</span></span>

## <span data-ttu-id="26e55-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26e55-122">OUTPUTS</span></span>

### <span data-ttu-id="26e55-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="26e55-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="26e55-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26e55-124">NOTES</span></span>

## <span data-ttu-id="26e55-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26e55-125">RELATED LINKS</span></span>

[<span data-ttu-id="26e55-126">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26e55-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="26e55-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26e55-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="26e55-128">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26e55-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="26e55-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26e55-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="26e55-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26e55-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="26e55-131">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="26e55-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="26e55-132">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="26e55-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
