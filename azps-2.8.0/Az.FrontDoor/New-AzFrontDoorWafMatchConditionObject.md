---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: f192eb4bf88201f30f8648cba6468fb406401f43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705374"
---
# <span data-ttu-id="fbf29-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="fbf29-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="fbf29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbf29-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf29-103">Tworzenie obiektu MatchCondition do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="fbf29-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="fbf29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbf29-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbf29-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbf29-105">DESCRIPTION</span></span>
<span data-ttu-id="fbf29-106">Tworzenie obiektu MatchCondition do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="fbf29-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="fbf29-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbf29-107">EXAMPLES</span></span>

### <span data-ttu-id="fbf29-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fbf29-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="fbf29-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fbf29-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="fbf29-110">Tworzenie obiektu MatchCondition</span><span class="sxs-lookup"><span data-stu-id="fbf29-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="fbf29-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbf29-111">PARAMETERS</span></span>

### <span data-ttu-id="fbf29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf29-112">-DefaultProfile</span></span>
<span data-ttu-id="fbf29-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbf29-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbf29-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="fbf29-114">-MatchValue</span></span>
<span data-ttu-id="fbf29-115">Wartość dopasowania.</span><span class="sxs-lookup"><span data-stu-id="fbf29-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf29-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="fbf29-116">-MatchVariable</span></span>
<span data-ttu-id="fbf29-117">Zmienna dopasowania.</span><span class="sxs-lookup"><span data-stu-id="fbf29-117">Match Variable.</span></span>
<span data-ttu-id="fbf29-118">Możliwe wartości to: "RemoteAddr", "RequestMethod", "QueryString", "PostArgs", "RequestUri", "RequestHeader", "RequestBody".</span><span class="sxs-lookup"><span data-stu-id="fbf29-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="fbf29-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="fbf29-119">-NegateCondition</span></span>
<span data-ttu-id="fbf29-120">W tym artykule opisano, czy jest to warunek Negate, czy nie jest wartością domyślną FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="fbf29-120">Describes if this is negate condition or not Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf29-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="fbf29-121">-OperatorProperty</span></span>
<span data-ttu-id="fbf29-122">Opis operatora do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="fbf29-122">Describes operator to be matched.</span></span>
<span data-ttu-id="fbf29-123">Możliwe są następujące wartości: "any", "IPMatch", "nomatch", "równa się", "Contains", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "BeginsWith", "EndsWith", "wyrażenie regularne"</span><span class="sxs-lookup"><span data-stu-id="fbf29-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="fbf29-124">-Selector</span><span class="sxs-lookup"><span data-stu-id="fbf29-124">-Selector</span></span>
<span data-ttu-id="fbf29-125">Nazwa selektora w programie RequestHeader lub RequestBody do dopasowania</span><span class="sxs-lookup"><span data-stu-id="fbf29-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="fbf29-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="fbf29-126">-Transform</span></span>
<span data-ttu-id="fbf29-127">Przekształceń, które mają zostać zastosowane.</span><span class="sxs-lookup"><span data-stu-id="fbf29-127">Transforms to apply.</span></span> <span data-ttu-id="fbf29-128">Możliwe wartości to: "małe", "wielkie", "Trim", "UrlDecode", "UrlEncode", "RemoveNulls".</span><span class="sxs-lookup"><span data-stu-id="fbf29-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf29-129">CommonParameters</span></span>
<span data-ttu-id="fbf29-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf29-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbf29-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf29-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbf29-132">INPUTS</span></span>

### <span data-ttu-id="fbf29-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fbf29-133">None</span></span>

## <span data-ttu-id="fbf29-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbf29-134">OUTPUTS</span></span>

### <span data-ttu-id="fbf29-135">Microsoft. Azure. Commands. FrontDoor. models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="fbf29-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="fbf29-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbf29-136">NOTES</span></span>

## <span data-ttu-id="fbf29-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbf29-137">RELATED LINKS</span></span>

[<span data-ttu-id="fbf29-138">Nowe — AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="fbf29-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)