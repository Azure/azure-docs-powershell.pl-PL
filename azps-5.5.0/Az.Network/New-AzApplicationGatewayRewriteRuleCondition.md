---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202872"
---
# <span data-ttu-id="ff5b7-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="ff5b7-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="ff5b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5b7-103">Dodaje warunek doulecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="ff5b7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff5b7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff5b7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff5b7-105">DESCRIPTION</span></span>
<span data-ttu-id="ff5b7-106">**Polecenie cmdlet AzApplicationGatewayRewriteRuleCondition** tworzy warunek reguły ponownego w przypadku bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="ff5b7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff5b7-107">EXAMPLES</span></span>

### <span data-ttu-id="ff5b7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ff5b7-108">Example 1</span></span>
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
<span data-ttu-id="ff5b7-109">To polecenie tworzy warunek w regułę ponownego agwania i zapisuje wynik w zmiennej o nazwie $condition.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="ff5b7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff5b7-110">PARAMETERS</span></span>

### <span data-ttu-id="ff5b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5b7-111">-DefaultProfile</span></span>
<span data-ttu-id="ff5b7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff5b7-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="ff5b7-113">-IgnoreCase</span></span>
<span data-ttu-id="ff5b7-114">Ustaw tę flagę tak, aby zignorować literę we wzorcu</span><span class="sxs-lookup"><span data-stu-id="ff5b7-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="ff5b7-115">- Negate</span><span class="sxs-lookup"><span data-stu-id="ff5b7-115">-Negate</span></span>
<span data-ttu-id="ff5b7-116">Ustawienie tej flagi w celu negacji sprawdzania poprawności warunku</span><span class="sxs-lookup"><span data-stu-id="ff5b7-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="ff5b7-117">— Deseń</span><span class="sxs-lookup"><span data-stu-id="ff5b7-117">-Pattern</span></span>
<span data-ttu-id="ff5b7-118">Wzorzec wyszukiwania w nagłówku zmiennych</span><span class="sxs-lookup"><span data-stu-id="ff5b7-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="ff5b7-119">—Zmienna</span><span class="sxs-lookup"><span data-stu-id="ff5b7-119">-Variable</span></span>
<span data-ttu-id="ff5b7-120">Nazwa nagłówka, który ma być ustawiony jako warunek</span><span class="sxs-lookup"><span data-stu-id="ff5b7-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="ff5b7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5b7-121">CommonParameters</span></span>
<span data-ttu-id="ff5b7-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff5b7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ff5b7-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5b7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5b7-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff5b7-124">INPUTS</span></span>

### <span data-ttu-id="ff5b7-125">Brak</span><span class="sxs-lookup"><span data-stu-id="ff5b7-125">None</span></span>

## <span data-ttu-id="ff5b7-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff5b7-126">OUTPUTS</span></span>

### <span data-ttu-id="ff5b7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="ff5b7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="ff5b7-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff5b7-128">NOTES</span></span>

## <span data-ttu-id="ff5b7-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff5b7-129">RELATED LINKS</span></span>
[<span data-ttu-id="ff5b7-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5b7-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff5b7-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5b7-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff5b7-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5b7-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff5b7-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5b7-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff5b7-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff5b7-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ff5b7-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ff5b7-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="ff5b7-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ff5b7-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
