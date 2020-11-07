---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868368"
---
# <span data-ttu-id="ee4fb-101">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ee4fb-101">New-AzFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="ee4fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4fb-103">Tworzenie obiektu MatchCondition do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="ee4fb-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="ee4fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee4fb-104">SYNTAX</span></span>

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee4fb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee4fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ee4fb-106">Tworzenie obiektu MatchCondition do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="ee4fb-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="ee4fb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee4fb-107">EXAMPLES</span></span>

### <span data-ttu-id="ee4fb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee4fb-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

<span data-ttu-id="ee4fb-109">Tworzenie obiektu MatchCondition</span><span class="sxs-lookup"><span data-stu-id="ee4fb-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="ee4fb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee4fb-110">PARAMETERS</span></span>

### <span data-ttu-id="ee4fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4fb-111">-DefaultProfile</span></span>
<span data-ttu-id="ee4fb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee4fb-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="ee4fb-113">-MatchValue</span></span>
<span data-ttu-id="ee4fb-114">Wartość dopasowania.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-114">Match value.</span></span>

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

### <span data-ttu-id="ee4fb-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="ee4fb-115">-MatchVariable</span></span>
<span data-ttu-id="ee4fb-116">Zmienna dopasowania.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-116">Match Variable.</span></span>
<span data-ttu-id="ee4fb-117">Możliwe wartości to: "RemoteAddr", "RequestMethod", "QueryString", "PostArgs", "RequestUri", "RequestHeader", "RequestBody".</span><span class="sxs-lookup"><span data-stu-id="ee4fb-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4fb-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="ee4fb-118">-NegateCondition</span></span>
<span data-ttu-id="ee4fb-119">W tym artykule opisano, czy jest to warunek Negate, czy nie jest wartością domyślną FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="ee4fb-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="ee4fb-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="ee4fb-120">-OperatorProperty</span></span>
<span data-ttu-id="ee4fb-121">Opis operatora do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-121">Describes operator to be matched.</span></span>
<span data-ttu-id="ee4fb-122">Możliwe są następujące wartości: "any", "IPMatch", "nomatch", "EQUAL", "Contains", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "BeginsWith".</span><span class="sxs-lookup"><span data-stu-id="ee4fb-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee4fb-123">-Selector</span><span class="sxs-lookup"><span data-stu-id="ee4fb-123">-Selector</span></span>
<span data-ttu-id="ee4fb-124">Nazwa selektora w programie RequestHeader lub RequestBody do dopasowania</span><span class="sxs-lookup"><span data-stu-id="ee4fb-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="ee4fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4fb-125">CommonParameters</span></span>
<span data-ttu-id="ee4fb-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee4fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4fb-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee4fb-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4fb-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee4fb-128">INPUTS</span></span>

### <span data-ttu-id="ee4fb-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ee4fb-129">None</span></span>

## <span data-ttu-id="ee4fb-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee4fb-130">OUTPUTS</span></span>

### <span data-ttu-id="ee4fb-131">Microsoft. Azure. Commands. FrontDoor. models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="ee4fb-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="ee4fb-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee4fb-132">NOTES</span></span>

## <span data-ttu-id="ee4fb-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee4fb-133">RELATED LINKS</span></span>

[<span data-ttu-id="ee4fb-134">Nowe — AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="ee4fb-134">New-AzFrontDoorCustomRuleObject</span></span>](./New-AzFrontDoorCustomRuleObject.md)
