---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358654"
---
# <span data-ttu-id="4d306-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="4d306-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="4d306-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d306-102">SYNOPSIS</span></span>
<span data-ttu-id="4d306-103">Umożliwia utworzenie warunku reguły dostarczania.</span><span class="sxs-lookup"><span data-stu-id="4d306-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="4d306-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d306-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d306-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d306-105">DESCRIPTION</span></span>
<span data-ttu-id="4d306-106">Polecenie cmdlet **New-AzCdnDeliveryRule** umożliwia utworzenie reguły dostarczania dla tworzenia punktu końcowego usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="4d306-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="4d306-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d306-107">EXAMPLES</span></span>

### <span data-ttu-id="4d306-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4d306-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="4d306-109">Utwórz prosty warunek.</span><span class="sxs-lookup"><span data-stu-id="4d306-109">Create a simple condition.</span></span>

## <span data-ttu-id="4d306-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d306-110">PARAMETERS</span></span>

### <span data-ttu-id="4d306-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d306-111">-DefaultProfile</span></span>
<span data-ttu-id="4d306-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d306-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d306-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="4d306-113">-MatchValue</span></span>
<span data-ttu-id="4d306-114">Lista możliwych wartości dopasowania.</span><span class="sxs-lookup"><span data-stu-id="4d306-114">List of possible match values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d306-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="4d306-115">-MatchVariable</span></span>
<span data-ttu-id="4d306-116">Dopasuj zmienną warunku.</span><span class="sxs-lookup"><span data-stu-id="4d306-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="4d306-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="4d306-117">-NegateCondition</span></span>
<span data-ttu-id="4d306-118">Opisuje, czy wynik tego warunku powinien zostać spowodowany negacją.</span><span class="sxs-lookup"><span data-stu-id="4d306-118">Describes if the result of this condition should be negated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d306-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="4d306-119">-Operator</span></span>
<span data-ttu-id="4d306-120">Opis operatora do dopasowania</span><span class="sxs-lookup"><span data-stu-id="4d306-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="4d306-121">-Selector</span><span class="sxs-lookup"><span data-stu-id="4d306-121">-Selector</span></span>
<span data-ttu-id="4d306-122">Nazwa selektora do dopasowania</span><span class="sxs-lookup"><span data-stu-id="4d306-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="4d306-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="4d306-123">-Transform</span></span>
<span data-ttu-id="4d306-124">Przekształć, aby zastosować przed dopasowaniem.</span><span class="sxs-lookup"><span data-stu-id="4d306-124">Transform to apply before matching.</span></span>
<span data-ttu-id="4d306-125">Możliwe wartości to małe i wielkie litery</span><span class="sxs-lookup"><span data-stu-id="4d306-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="4d306-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d306-126">CommonParameters</span></span>
<span data-ttu-id="4d306-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d306-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d306-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d306-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d306-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d306-129">INPUTS</span></span>

### <span data-ttu-id="4d306-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4d306-130">None</span></span>

## <span data-ttu-id="4d306-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d306-131">OUTPUTS</span></span>

### <span data-ttu-id="4d306-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="4d306-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="4d306-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d306-133">NOTES</span></span>

## <span data-ttu-id="4d306-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d306-134">RELATED LINKS</span></span>
