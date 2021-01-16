---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358225"
---
# <span data-ttu-id="d0de8-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d0de8-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d0de8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0de8-102">SYNOPSIS</span></span>
<span data-ttu-id="d0de8-103">Umożliwia utworzenie akcji reguły ponownej edycji dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d0de8-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="d0de8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0de8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0de8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0de8-105">DESCRIPTION</span></span>
<span data-ttu-id="d0de8-106">Polecenie cmdlet **New-AzApplicationGatewayRewriteRuleActionSet** umożliwia utworzenie akcji reguły ponownego zapisu dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0de8-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="d0de8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0de8-107">EXAMPLES</span></span>

### <span data-ttu-id="d0de8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0de8-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="d0de8-109">To polecenie umożliwia utworzenie ustawionej akcji przepisywania i zapisanie wyniku w zmiennej o nazwie $action.</span><span class="sxs-lookup"><span data-stu-id="d0de8-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="d0de8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0de8-110">PARAMETERS</span></span>

### <span data-ttu-id="d0de8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0de8-111">-DefaultProfile</span></span>
<span data-ttu-id="d0de8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0de8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0de8-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0de8-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="d0de8-114">Lista konfiguracji nagłówków żądań</span><span class="sxs-lookup"><span data-stu-id="d0de8-114">List of request header configurations</span></span>

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

### <span data-ttu-id="d0de8-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0de8-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="d0de8-116">Lista konfiguracji nagłówka odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="d0de8-116">List of response header configurations</span></span>

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

### <span data-ttu-id="d0de8-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0de8-117">-UrlConfiguration</span></span>
<span data-ttu-id="d0de8-118">Konfiguracja adresu URL dla zestawu akcji</span><span class="sxs-lookup"><span data-stu-id="d0de8-118">Url Configuration for action set</span></span>

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

### <span data-ttu-id="d0de8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0de8-119">CommonParameters</span></span>
<span data-ttu-id="d0de8-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0de8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0de8-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0de8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0de8-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0de8-122">INPUTS</span></span>

### <span data-ttu-id="d0de8-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d0de8-123">None</span></span>

## <span data-ttu-id="d0de8-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0de8-124">OUTPUTS</span></span>

### <span data-ttu-id="d0de8-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d0de8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="d0de8-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0de8-126">NOTES</span></span>

## <span data-ttu-id="d0de8-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0de8-127">RELATED LINKS</span></span>

[<span data-ttu-id="d0de8-128">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0de8-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0de8-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0de8-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0de8-130">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0de8-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0de8-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0de8-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0de8-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0de8-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d0de8-133">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d0de8-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d0de8-134">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0de8-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="d0de8-135">Nowe — AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0de8-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)