---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717399"
---
# <span data-ttu-id="c471f-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="c471f-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="c471f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c471f-102">SYNOPSIS</span></span>
<span data-ttu-id="c471f-103">Tworzenie obiektu MatchCondition do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="c471f-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c471f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c471f-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c471f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c471f-105">DESCRIPTION</span></span>
<span data-ttu-id="c471f-106">Tworzenie obiektu MatchCondition do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="c471f-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="c471f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c471f-107">EXAMPLES</span></span>

### <span data-ttu-id="c471f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c471f-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="c471f-109">Tworzenie obiektu MatchCondition</span><span class="sxs-lookup"><span data-stu-id="c471f-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="c471f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c471f-110">PARAMETERS</span></span>

### <span data-ttu-id="c471f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c471f-111">-DefaultProfile</span></span>
<span data-ttu-id="c471f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c471f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c471f-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="c471f-113">-MatchValue</span></span>
<span data-ttu-id="c471f-114">Wartość dopasowania.</span><span class="sxs-lookup"><span data-stu-id="c471f-114">Match value.</span></span>

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

### <span data-ttu-id="c471f-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="c471f-115">-MatchVariable</span></span>
<span data-ttu-id="c471f-116">Zmienna dopasowania.</span><span class="sxs-lookup"><span data-stu-id="c471f-116">Match Variable.</span></span>
<span data-ttu-id="c471f-117">Możliwe wartości to: "RemoteAddr", "RequestMethod", "QueryString", "PostArgs", "RequestUri", "RequestHeader", "RequestBody".</span><span class="sxs-lookup"><span data-stu-id="c471f-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="c471f-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="c471f-118">-NegateCondition</span></span>
<span data-ttu-id="c471f-119">W tym artykule opisano, czy jest to warunek Negate, czy nie jest wartością domyślną FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="c471f-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="c471f-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="c471f-120">-OperatorProperty</span></span>
<span data-ttu-id="c471f-121">Opis operatora do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="c471f-121">Describes operator to be matched.</span></span>
<span data-ttu-id="c471f-122">Możliwe są następujące wartości: "any", "IPMatch", "nomatch", "EQUAL", "Contains", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "BeginsWith".</span><span class="sxs-lookup"><span data-stu-id="c471f-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

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

### <span data-ttu-id="c471f-123">-Selector</span><span class="sxs-lookup"><span data-stu-id="c471f-123">-Selector</span></span>
<span data-ttu-id="c471f-124">Nazwa selektora w programie RequestHeader lub RequestBody do dopasowania</span><span class="sxs-lookup"><span data-stu-id="c471f-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="c471f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c471f-125">CommonParameters</span></span>
<span data-ttu-id="c471f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c471f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c471f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c471f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c471f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c471f-128">INPUTS</span></span>

### <span data-ttu-id="c471f-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c471f-129">None</span></span>

## <span data-ttu-id="c471f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c471f-130">OUTPUTS</span></span>

### <span data-ttu-id="c471f-131">Microsoft. Azure. Commands. FrontDoor. models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="c471f-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="c471f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c471f-132">NOTES</span></span>

## <span data-ttu-id="c471f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c471f-133">RELATED LINKS</span></span>

[<span data-ttu-id="c471f-134">Nowe — AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="c471f-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
