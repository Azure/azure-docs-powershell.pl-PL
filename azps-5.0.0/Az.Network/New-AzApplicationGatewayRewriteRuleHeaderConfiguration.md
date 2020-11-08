---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233031"
---
# <span data-ttu-id="c168f-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c168f-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="c168f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c168f-102">SYNOPSIS</span></span>
<span data-ttu-id="c168f-103">Umożliwia utworzenie konfiguracji nagłówka reguły ponownie zapisu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c168f-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="c168f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c168f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c168f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c168f-105">DESCRIPTION</span></span>
<span data-ttu-id="c168f-106">Polecenie cmdlet **AzApplicationGatewayRewriteRuleHeaderConfiguration** umożliwia utworzenie akcji reguły ponownej edycji dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c168f-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="c168f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c168f-107">EXAMPLES</span></span>

### <span data-ttu-id="c168f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c168f-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="c168f-109">To polecenie powoduje utworzenie konfiguracji nagłówka reguły do ponownej edycji i zapisanie wyniku w zmiennej o nazwie $hc.</span><span class="sxs-lookup"><span data-stu-id="c168f-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="c168f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c168f-110">PARAMETERS</span></span>

### <span data-ttu-id="c168f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c168f-111">-DefaultProfile</span></span>
<span data-ttu-id="c168f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c168f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c168f-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="c168f-113">-HeaderName</span></span>
<span data-ttu-id="c168f-114">Nazwa nagłówka, który ma zostać ponownie napisany</span><span class="sxs-lookup"><span data-stu-id="c168f-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="c168f-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="c168f-115">-HeaderValue</span></span>
<span data-ttu-id="c168f-116">Wartość nagłówka do zestawu dla danej nazwy nagłówka.</span><span class="sxs-lookup"><span data-stu-id="c168f-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="c168f-117">Nagłówek zostanie usunięty, jeśli zostanie pominięty</span><span class="sxs-lookup"><span data-stu-id="c168f-117">Header will be deleted if this is omitted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c168f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c168f-118">CommonParameters</span></span>
<span data-ttu-id="c168f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c168f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c168f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c168f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c168f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c168f-121">INPUTS</span></span>

### <span data-ttu-id="c168f-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c168f-122">None</span></span>

## <span data-ttu-id="c168f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c168f-123">OUTPUTS</span></span>

### <span data-ttu-id="c168f-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c168f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="c168f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c168f-125">NOTES</span></span>

## <span data-ttu-id="c168f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c168f-126">RELATED LINKS</span></span>

[<span data-ttu-id="c168f-127">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c168f-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c168f-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c168f-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c168f-129">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c168f-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c168f-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c168f-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c168f-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c168f-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="c168f-132">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c168f-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="c168f-133">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c168f-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
