---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221987"
---
# <span data-ttu-id="2859b-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2859b-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="2859b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2859b-102">SYNOPSIS</span></span>
<span data-ttu-id="2859b-103">Umożliwia utworzenie konfiguracji nagłówka reguły ponownie zapisu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2859b-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="2859b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2859b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2859b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2859b-105">DESCRIPTION</span></span>
<span data-ttu-id="2859b-106">Polecenie cmdlet **AzApplicationGatewayRewriteRuleHeaderConfiguration** umożliwia utworzenie akcji reguły ponownej edycji dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2859b-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="2859b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2859b-107">EXAMPLES</span></span>

### <span data-ttu-id="2859b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2859b-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="2859b-109">To polecenie powoduje utworzenie konfiguracji nagłówka reguły do ponownej edycji i zapisanie wyniku w zmiennej o nazwie $hc.</span><span class="sxs-lookup"><span data-stu-id="2859b-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="2859b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2859b-110">PARAMETERS</span></span>

### <span data-ttu-id="2859b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2859b-111">-DefaultProfile</span></span>
<span data-ttu-id="2859b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2859b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2859b-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="2859b-113">-HeaderName</span></span>
<span data-ttu-id="2859b-114">Nazwa nagłówka, który ma zostać ponownie napisany</span><span class="sxs-lookup"><span data-stu-id="2859b-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="2859b-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="2859b-115">-HeaderValue</span></span>
<span data-ttu-id="2859b-116">Wartość nagłówka do zestawu dla danej nazwy nagłówka.</span><span class="sxs-lookup"><span data-stu-id="2859b-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="2859b-117">Nagłówek zostanie usunięty, jeśli zostanie pominięty</span><span class="sxs-lookup"><span data-stu-id="2859b-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="2859b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2859b-118">CommonParameters</span></span>
<span data-ttu-id="2859b-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2859b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2859b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2859b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2859b-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2859b-121">INPUTS</span></span>

### <span data-ttu-id="2859b-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2859b-122">None</span></span>

## <span data-ttu-id="2859b-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2859b-123">OUTPUTS</span></span>

### <span data-ttu-id="2859b-124">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2859b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="2859b-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2859b-125">NOTES</span></span>

## <span data-ttu-id="2859b-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2859b-126">RELATED LINKS</span></span>

[<span data-ttu-id="2859b-127">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2859b-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2859b-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2859b-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2859b-129">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2859b-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2859b-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2859b-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2859b-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2859b-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2859b-132">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2859b-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="2859b-133">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2859b-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
