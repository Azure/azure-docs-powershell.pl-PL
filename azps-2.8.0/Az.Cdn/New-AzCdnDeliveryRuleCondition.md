---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 830b561a3d46e23f083d77dcac627b28f7dbb94e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706548"
---
# <span data-ttu-id="6ded8-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="6ded8-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="6ded8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ded8-102">SYNOPSIS</span></span>
<span data-ttu-id="6ded8-103">Umożliwia utworzenie warunku reguły dostarczania.</span><span class="sxs-lookup"><span data-stu-id="6ded8-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="6ded8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ded8-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> -MatchValue <String[]>
 [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ded8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ded8-105">DESCRIPTION</span></span>
<span data-ttu-id="6ded8-106">Polecenie cmdlet **New-AzCdnDeliveryRule** umożliwia utworzenie reguły dostarczania dla tworzenia punktu końcowego usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="6ded8-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="6ded8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ded8-107">EXAMPLES</span></span>

### <span data-ttu-id="6ded8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ded8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="6ded8-109">Utwórz prosty warunek.</span><span class="sxs-lookup"><span data-stu-id="6ded8-109">Create a simple condition.</span></span>

## <span data-ttu-id="6ded8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ded8-110">PARAMETERS</span></span>

### <span data-ttu-id="6ded8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ded8-111">-DefaultProfile</span></span>
<span data-ttu-id="6ded8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ded8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ded8-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="6ded8-113">-MatchValue</span></span>
<span data-ttu-id="6ded8-114">Lista możliwych wartości dopasowania.</span><span class="sxs-lookup"><span data-stu-id="6ded8-114">List of possible match values.</span></span>

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

### <span data-ttu-id="6ded8-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="6ded8-115">-MatchVariable</span></span>
<span data-ttu-id="6ded8-116">Dopasuj zmienną warunku.</span><span class="sxs-lookup"><span data-stu-id="6ded8-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="6ded8-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="6ded8-117">-NegateCondition</span></span>
<span data-ttu-id="6ded8-118">Opisuje, czy wynik tego warunku powinien zostać spowodowany negacją.</span><span class="sxs-lookup"><span data-stu-id="6ded8-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="6ded8-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="6ded8-119">-Operator</span></span>
<span data-ttu-id="6ded8-120">Opis operatora do dopasowania</span><span class="sxs-lookup"><span data-stu-id="6ded8-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="6ded8-121">-Transform</span><span class="sxs-lookup"><span data-stu-id="6ded8-121">-Transform</span></span>
<span data-ttu-id="6ded8-122">Przekształć, aby zastosować przed dopasowaniem.</span><span class="sxs-lookup"><span data-stu-id="6ded8-122">Transform to apply before matching.</span></span>
<span data-ttu-id="6ded8-123">Możliwe wartości to małe i wielkie litery</span><span class="sxs-lookup"><span data-stu-id="6ded8-123">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="6ded8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ded8-124">CommonParameters</span></span>
<span data-ttu-id="6ded8-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ded8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ded8-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ded8-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ded8-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ded8-127">INPUTS</span></span>

### <span data-ttu-id="6ded8-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6ded8-128">None</span></span>

## <span data-ttu-id="6ded8-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ded8-129">OUTPUTS</span></span>

### <span data-ttu-id="6ded8-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="6ded8-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="6ded8-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ded8-131">NOTES</span></span>

## <span data-ttu-id="6ded8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ded8-132">RELATED LINKS</span></span>
