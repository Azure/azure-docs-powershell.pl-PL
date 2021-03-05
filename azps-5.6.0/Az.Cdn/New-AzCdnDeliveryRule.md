---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: a2143e0363d08a06ac72ee7c5207ef93f5c3a509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001834"
---
# <span data-ttu-id="91359-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="91359-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="91359-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91359-102">SYNOPSIS</span></span>
<span data-ttu-id="91359-103">Tworzy regułę dostarczania.</span><span class="sxs-lookup"><span data-stu-id="91359-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="91359-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91359-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91359-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="91359-105">DESCRIPTION</span></span>
<span data-ttu-id="91359-106">Polecenie **cmdlet New-AzCdnDeliveryRule** tworzy regułę dostarczania dla tworzenia punktu końcowego sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="91359-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="91359-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91359-107">EXAMPLES</span></span>

### <span data-ttu-id="91359-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="91359-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="91359-109">Utwórz prostą regułę.</span><span class="sxs-lookup"><span data-stu-id="91359-109">Create a simple rule.</span></span>

## <span data-ttu-id="91359-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91359-110">PARAMETERS</span></span>

### <span data-ttu-id="91359-111">— Akcja</span><span class="sxs-lookup"><span data-stu-id="91359-111">-Action</span></span>
<span data-ttu-id="91359-112">Lista akcji wykonywanych po wykonaniu wszystkich warunków reguły.</span><span class="sxs-lookup"><span data-stu-id="91359-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="91359-113">— Warunek</span><span class="sxs-lookup"><span data-stu-id="91359-113">-Condition</span></span>
<span data-ttu-id="91359-114">Lista warunków, które muszą być zgodne dla akcji do wykonania.</span><span class="sxs-lookup"><span data-stu-id="91359-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="91359-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91359-115">-DefaultProfile</span></span>
<span data-ttu-id="91359-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91359-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91359-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="91359-117">-Name</span></span>
<span data-ttu-id="91359-118">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="91359-118">Name of the rule</span></span>

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

### <span data-ttu-id="91359-119">— zamówienie</span><span class="sxs-lookup"><span data-stu-id="91359-119">-Order</span></span>
<span data-ttu-id="91359-120">Kolejność reguły</span><span class="sxs-lookup"><span data-stu-id="91359-120">Order of the rule</span></span>

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

### <span data-ttu-id="91359-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91359-121">CommonParameters</span></span>
<span data-ttu-id="91359-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91359-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91359-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91359-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91359-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91359-124">INPUTS</span></span>

### <span data-ttu-id="91359-125">Brak</span><span class="sxs-lookup"><span data-stu-id="91359-125">None</span></span>

## <span data-ttu-id="91359-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91359-126">OUTPUTS</span></span>

### <span data-ttu-id="91359-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="91359-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="91359-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91359-128">NOTES</span></span>

## <span data-ttu-id="91359-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91359-129">RELATED LINKS</span></span>
