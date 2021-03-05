---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: e67841073d6c7342e0bb88c52809a9c45d92f82f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970842"
---
# <span data-ttu-id="9b5e9-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="9b5e9-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="9b5e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5e9-103">Tworzenie obiektu MatchCondition do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="9b5e9-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="9b5e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b5e9-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b5e9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b5e9-105">DESCRIPTION</span></span>
<span data-ttu-id="9b5e9-106">Tworzenie obiektu MatchCondition do tworzenia zasad WAF</span><span class="sxs-lookup"><span data-stu-id="9b5e9-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="9b5e9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b5e9-107">EXAMPLES</span></span>

### <span data-ttu-id="9b5e9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b5e9-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="9b5e9-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9b5e9-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="9b5e9-110">Tworzenie obiektu MatchCondition</span><span class="sxs-lookup"><span data-stu-id="9b5e9-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="9b5e9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b5e9-111">PARAMETERS</span></span>

### <span data-ttu-id="9b5e9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5e9-112">-DefaultProfile</span></span>
<span data-ttu-id="9b5e9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b5e9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b5e9-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="9b5e9-114">-MatchValue</span></span>
<span data-ttu-id="9b5e9-115">Dopasuj wartość.</span><span class="sxs-lookup"><span data-stu-id="9b5e9-115">Match value.</span></span>

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

### <span data-ttu-id="9b5e9-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="9b5e9-116">-MatchVariable</span></span>
<span data-ttu-id="9b5e9-117">Dopasuj zmienną.</span><span class="sxs-lookup"><span data-stu-id="9b5e9-117">Match Variable.</span></span>
<span data-ttu-id="9b5e9-118">Możliwe wartości to: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span><span class="sxs-lookup"><span data-stu-id="9b5e9-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="9b5e9-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="9b5e9-119">-NegateCondition</span></span>
<span data-ttu-id="9b5e9-120">W tym artykule opisano, czy jest to warunek negatywowy, czy wartość domyślna nie jest fałszywa.</span><span class="sxs-lookup"><span data-stu-id="9b5e9-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="9b5e9-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="9b5e9-121">-OperatorProperty</span></span>
<span data-ttu-id="9b5e9-122">Opis operatora do dopasowania.</span><span class="sxs-lookup"><span data-stu-id="9b5e9-122">Describes operator to be matched.</span></span>
<span data-ttu-id="9b5e9-123">Możliwe wartości to: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span><span class="sxs-lookup"><span data-stu-id="9b5e9-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="9b5e9-124">— Selektor</span><span class="sxs-lookup"><span data-stu-id="9b5e9-124">-Selector</span></span>
<span data-ttu-id="9b5e9-125">Nazwa selektora w polach RequestHeader lub RequestBody do dopasowania</span><span class="sxs-lookup"><span data-stu-id="9b5e9-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="9b5e9-126">— Przekształcanie</span><span class="sxs-lookup"><span data-stu-id="9b5e9-126">-Transform</span></span>
<span data-ttu-id="9b5e9-127">Przekształcenia do zastosowania.</span><span class="sxs-lookup"><span data-stu-id="9b5e9-127">Transforms to apply.</span></span> <span data-ttu-id="9b5e9-128">Możliwe wartości to: "Małe litery", "Wielkie litery", "Przytnij", "AdresDodaty", "Adres_url", "UsuńNulls".</span><span class="sxs-lookup"><span data-stu-id="9b5e9-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="9b5e9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5e9-129">CommonParameters</span></span>
<span data-ttu-id="9b5e9-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b5e9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5e9-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b5e9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5e9-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b5e9-132">INPUTS</span></span>

### <span data-ttu-id="9b5e9-133">Brak</span><span class="sxs-lookup"><span data-stu-id="9b5e9-133">None</span></span>

## <span data-ttu-id="9b5e9-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b5e9-134">OUTPUTS</span></span>

### <span data-ttu-id="9b5e9-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="9b5e9-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="9b5e9-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b5e9-136">NOTES</span></span>

## <span data-ttu-id="9b5e9-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b5e9-137">RELATED LINKS</span></span>

[<span data-ttu-id="9b5e9-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="9b5e9-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
