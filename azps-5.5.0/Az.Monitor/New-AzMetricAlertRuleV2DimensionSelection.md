---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 500a0bed47fad0174e3e7efb3ee27e2bb98a9894
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190122"
---
# <span data-ttu-id="3097b-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="3097b-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="3097b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3097b-102">SYNOPSIS</span></span>
<span data-ttu-id="3097b-103">Tworzy obiekt wyboru wymiaru lokalnego, który może służyć do konstruowania metrycznych kryteriów alertów.</span><span class="sxs-lookup"><span data-stu-id="3097b-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="3097b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3097b-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3097b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3097b-105">DESCRIPTION</span></span>
<span data-ttu-id="3097b-106">Polecenie cmdlet **New-AzMetricAlertRuleV2DimensionSelection** tworzy obiekt wyboru wymiaru lokalnego, ułatwiający tworzenie kryteriów alertów metrycznych przy użyciu polecenia cmdlet [New-AzMetricAlertRuleV2Criteria.](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria)</span><span class="sxs-lookup"><span data-stu-id="3097b-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="3097b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3097b-107">EXAMPLES</span></span>

### <span data-ttu-id="3097b-108">Przykład 1. Tworzenie obiektu zaznaczania wymiarów</span><span class="sxs-lookup"><span data-stu-id="3097b-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="3097b-109">To polecenie tworzy obiekt zaznaczania wymiarów, który określa, że wartości muszą być wybrane dla {1,3,4} wymiarowania "DPOWIEDZIALNOŚCI".</span><span class="sxs-lookup"><span data-stu-id="3097b-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="3097b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3097b-110">PARAMETERS</span></span>

### <span data-ttu-id="3097b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3097b-111">-DefaultProfile</span></span>
<span data-ttu-id="3097b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3097b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3097b-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="3097b-113">-DimensionName</span></span>
<span data-ttu-id="3097b-114">Nazwa wymiaru</span><span class="sxs-lookup"><span data-stu-id="3097b-114">The Dimension name</span></span>

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

### <span data-ttu-id="3097b-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="3097b-115">-ValuesToExclude</span></span>
<span data-ttu-id="3097b-116">WykluczanieWartości</span><span class="sxs-lookup"><span data-stu-id="3097b-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="3097b-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="3097b-117">-ValuesToInclude</span></span>
<span data-ttu-id="3097b-118">Wartości IncludeValues</span><span class="sxs-lookup"><span data-stu-id="3097b-118">The IncludeValues</span></span>

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

### <span data-ttu-id="3097b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3097b-119">CommonParameters</span></span>
<span data-ttu-id="3097b-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3097b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3097b-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3097b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3097b-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3097b-122">INPUTS</span></span>

### <span data-ttu-id="3097b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3097b-123">System.String</span></span>

### <span data-ttu-id="3097b-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3097b-124">System.String[]</span></span>

## <span data-ttu-id="3097b-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3097b-125">OUTPUTS</span></span>

### <span data-ttu-id="3097b-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="3097b-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="3097b-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3097b-127">NOTES</span></span>

## <span data-ttu-id="3097b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3097b-128">RELATED LINKS</span></span>
