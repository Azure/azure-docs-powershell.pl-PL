---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358197"
---
# <span data-ttu-id="3144d-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="3144d-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="3144d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3144d-102">SYNOPSIS</span></span>
<span data-ttu-id="3144d-103">Dodaje warunek do RewriteRule dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3144d-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="3144d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3144d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3144d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3144d-105">DESCRIPTION</span></span>
<span data-ttu-id="3144d-106">Polecenie cmdlet **AzApplicationGatewayRewriteRuleCondition** tworzy warunek reguły ponownej edycji dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3144d-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="3144d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3144d-107">EXAMPLES</span></span>

### <span data-ttu-id="3144d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3144d-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="3144d-109">To polecenie powoduje utworzenie warunku w regule ponownej edycji i zapisanie wyniku w zmiennej o nazwie $condition.</span><span class="sxs-lookup"><span data-stu-id="3144d-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="3144d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3144d-110">PARAMETERS</span></span>

### <span data-ttu-id="3144d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3144d-111">-DefaultProfile</span></span>
<span data-ttu-id="3144d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3144d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3144d-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="3144d-113">-IgnoreCase</span></span>
<span data-ttu-id="3144d-114">Ustaw tę flagę na ignorowanie wielkości liter we wzorcu</span><span class="sxs-lookup"><span data-stu-id="3144d-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3144d-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="3144d-115">-Negate</span></span>
<span data-ttu-id="3144d-116">Ustaw tę flagę, aby Negate weryfikację warunku</span><span class="sxs-lookup"><span data-stu-id="3144d-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3144d-117">-Wzorzec</span><span class="sxs-lookup"><span data-stu-id="3144d-117">-Pattern</span></span>
<span data-ttu-id="3144d-118">Deseń do wyszukania w nagłówku zmiennej</span><span class="sxs-lookup"><span data-stu-id="3144d-118">Pattern to look for in the Variable Header</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3144d-119">-Zmienna</span><span class="sxs-lookup"><span data-stu-id="3144d-119">-Variable</span></span>
<span data-ttu-id="3144d-120">Nazwa nagłówka, dla którego ma zostać ustawiony warunek</span><span class="sxs-lookup"><span data-stu-id="3144d-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3144d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3144d-121">CommonParameters</span></span>
<span data-ttu-id="3144d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3144d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3144d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3144d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3144d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3144d-124">INPUTS</span></span>

### <span data-ttu-id="3144d-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3144d-125">None</span></span>

## <span data-ttu-id="3144d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3144d-126">OUTPUTS</span></span>

### <span data-ttu-id="3144d-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="3144d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="3144d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3144d-128">NOTES</span></span>

## <span data-ttu-id="3144d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3144d-129">RELATED LINKS</span></span>
[<span data-ttu-id="3144d-130">Dodaj-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3144d-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3144d-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3144d-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3144d-132">Nowe — AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3144d-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3144d-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3144d-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3144d-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3144d-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3144d-135">Nowe — AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3144d-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="3144d-136">Nowe — AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3144d-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
