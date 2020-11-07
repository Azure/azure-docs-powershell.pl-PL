---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f13591a92b52e00ed94e93fec480d810037f061d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709354"
---
# <span data-ttu-id="4a77e-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4a77e-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="4a77e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a77e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a77e-103">Umożliwia utworzenie reguły actionset dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4a77e-103">Creates a rewrite rule actionset for an application gateway.</span></span>

## <span data-ttu-id="4a77e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a77e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a77e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4a77e-105">DESCRIPTION</span></span>
<span data-ttu-id="4a77e-106">Polecenie cmdlet **New-AzApplicationGatewayRewriteRuleActionSet** tworzy regułę ponownego zapisu actionset dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4a77e-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule actionset for an Azure application gateway.</span></span>

## <span data-ttu-id="4a77e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a77e-107">EXAMPLES</span></span>

### <span data-ttu-id="4a77e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4a77e-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="4a77e-109">To polecenie powoduje utworzenie reguły actionset i zapisanie wyniku w zmiennej o nazwie $action.</span><span class="sxs-lookup"><span data-stu-id="4a77e-109">This command creates a rewrite rule actionset and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="4a77e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a77e-110">PARAMETERS</span></span>

### <span data-ttu-id="4a77e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a77e-111">-DefaultProfile</span></span>
<span data-ttu-id="4a77e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a77e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a77e-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a77e-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="4a77e-114">Lista konfiguracji nagłówków żądań</span><span class="sxs-lookup"><span data-stu-id="4a77e-114">List of request header configurations</span></span>

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

### <span data-ttu-id="4a77e-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a77e-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="4a77e-116">Lista konfiguracji nagłówka odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="4a77e-116">List of response header configurations</span></span>

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

### <span data-ttu-id="4a77e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a77e-117">CommonParameters</span></span>
<span data-ttu-id="4a77e-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a77e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a77e-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a77e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a77e-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a77e-120">INPUTS</span></span>

### <span data-ttu-id="4a77e-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4a77e-121">None</span></span>

## <span data-ttu-id="4a77e-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a77e-122">OUTPUTS</span></span>

### <span data-ttu-id="4a77e-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4a77e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="4a77e-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a77e-124">NOTES</span></span>

## <span data-ttu-id="4a77e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a77e-125">RELATED LINKS</span></span>

[<span data-ttu-id="4a77e-126">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a77e-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4a77e-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a77e-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4a77e-128">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a77e-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4a77e-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a77e-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4a77e-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4a77e-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="4a77e-131">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4a77e-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="4a77e-132">Nowe — AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a77e-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
