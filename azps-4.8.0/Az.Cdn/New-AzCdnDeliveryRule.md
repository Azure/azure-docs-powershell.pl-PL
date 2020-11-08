---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062358"
---
# <span data-ttu-id="6c0c6-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="6c0c6-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="6c0c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0c6-103">Umożliwia utworzenie reguły dostarczania.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="6c0c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c0c6-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c0c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6c0c6-105">DESCRIPTION</span></span>
<span data-ttu-id="6c0c6-106">Polecenie cmdlet **New-AzCdnDeliveryRule** umożliwia utworzenie reguły dostarczania dla tworzenia punktu końcowego usługi CDN.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="6c0c6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c0c6-107">EXAMPLES</span></span>

### <span data-ttu-id="6c0c6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c0c6-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="6c0c6-109">Tworzenie prostej reguły.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-109">Create a simple rule.</span></span>

## <span data-ttu-id="6c0c6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c0c6-110">PARAMETERS</span></span>

### <span data-ttu-id="6c0c6-111">-Action</span><span class="sxs-lookup"><span data-stu-id="6c0c6-111">-Action</span></span>
<span data-ttu-id="6c0c6-112">Lista akcji wykonywanych po spełnieniu wszystkich warunków reguły.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0c6-113">-Warunek</span><span class="sxs-lookup"><span data-stu-id="6c0c6-113">-Condition</span></span>
<span data-ttu-id="6c0c6-114">Lista warunków, które muszą zostać dopasowane w celu wykonania akcji.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0c6-115">-DefaultProfile</span></span>
<span data-ttu-id="6c0c6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c0c6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c0c6-117">-Name</span></span>
<span data-ttu-id="6c0c6-118">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="6c0c6-118">Name of the rule</span></span>

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

### <span data-ttu-id="6c0c6-119">-Order (kolejność)</span><span class="sxs-lookup"><span data-stu-id="6c0c6-119">-Order</span></span>
<span data-ttu-id="6c0c6-120">Kolejność reguły</span><span class="sxs-lookup"><span data-stu-id="6c0c6-120">Order of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0c6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0c6-121">CommonParameters</span></span>
<span data-ttu-id="6c0c6-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c0c6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0c6-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c0c6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0c6-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c0c6-124">INPUTS</span></span>

### <span data-ttu-id="6c0c6-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6c0c6-125">None</span></span>

## <span data-ttu-id="6c0c6-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c0c6-126">OUTPUTS</span></span>

### <span data-ttu-id="6c0c6-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="6c0c6-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="6c0c6-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c0c6-128">NOTES</span></span>

## <span data-ttu-id="6c0c6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c0c6-129">RELATED LINKS</span></span>
