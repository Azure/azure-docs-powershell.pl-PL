---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 244e71148557ef46ea3305f7dc2826eb06e3b50d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962897"
---
# <span data-ttu-id="2a82c-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2a82c-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="2a82c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a82c-102">SYNOPSIS</span></span>
<span data-ttu-id="2a82c-103">Tworzy obiekt wyboru wymiaru lokalnego, który może służyć do konstruowania metrycznych kryteriów alertów.</span><span class="sxs-lookup"><span data-stu-id="2a82c-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="2a82c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2a82c-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a82c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2a82c-105">DESCRIPTION</span></span>
<span data-ttu-id="2a82c-106">Polecenie cmdlet **New-AzMetricAlertRuleV2DimensionSelection** tworzy obiekt wyboru wymiaru lokalnego, ułatwiający tworzenie kryteriów alertów metrycznych przy użyciu polecenia cmdlet [New-AzMetricAlertRuleV2Criteria.](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria)</span><span class="sxs-lookup"><span data-stu-id="2a82c-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="2a82c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2a82c-107">EXAMPLES</span></span>

### <span data-ttu-id="2a82c-108">Przykład 1. Tworzenie obiektu zaznaczania wymiarów</span><span class="sxs-lookup"><span data-stu-id="2a82c-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="2a82c-109">To polecenie tworzy obiekt zaznaczania wymiarów, który określa, że wartości muszą być wybrane {1,3,4} dla wymiarowania "DPOWIEDZIALNOŚCI".</span><span class="sxs-lookup"><span data-stu-id="2a82c-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="2a82c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a82c-110">PARAMETERS</span></span>

### <span data-ttu-id="2a82c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a82c-111">-DefaultProfile</span></span>
<span data-ttu-id="2a82c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a82c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a82c-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="2a82c-113">-DimensionName</span></span>
<span data-ttu-id="2a82c-114">Nazwa wymiaru</span><span class="sxs-lookup"><span data-stu-id="2a82c-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a82c-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="2a82c-115">-ValuesToExclude</span></span>
<span data-ttu-id="2a82c-116">WykluczanieWartości</span><span class="sxs-lookup"><span data-stu-id="2a82c-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a82c-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="2a82c-117">-ValuesToInclude</span></span>
<span data-ttu-id="2a82c-118">Wartości IncludeValues</span><span class="sxs-lookup"><span data-stu-id="2a82c-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a82c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a82c-119">CommonParameters</span></span>
<span data-ttu-id="2a82c-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a82c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a82c-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a82c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a82c-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a82c-122">INPUTS</span></span>

### <span data-ttu-id="2a82c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="2a82c-123">System.String</span></span>

### <span data-ttu-id="2a82c-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2a82c-124">System.String[]</span></span>

## <span data-ttu-id="2a82c-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a82c-125">OUTPUTS</span></span>

### <span data-ttu-id="2a82c-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="2a82c-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="2a82c-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2a82c-127">NOTES</span></span>

## <span data-ttu-id="2a82c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a82c-128">RELATED LINKS</span></span>
