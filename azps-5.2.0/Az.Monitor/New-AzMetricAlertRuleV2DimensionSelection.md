---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 500a0bed47fad0174e3e7efb3ee27e2bb98a9894
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331582"
---
# <span data-ttu-id="9d4a0-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="9d4a0-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="9d4a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d4a0-103">Tworzy obiekt lokalnego wyboru wymiaru, którego można użyć do skonstruowania kryteriów alertu metryki.</span><span class="sxs-lookup"><span data-stu-id="9d4a0-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="9d4a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d4a0-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d4a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9d4a0-105">DESCRIPTION</span></span>
<span data-ttu-id="9d4a0-106">Polecenie cmdlet **New-AzMetricAlertRuleV2DimensionSelection** umożliwia utworzenie obiektu lokalnego zaznaczania wymiaru w celu ułatwienia konstruowania kryteriów alertów metrycznych przy użyciu polecenia cmdlet [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) .</span><span class="sxs-lookup"><span data-stu-id="9d4a0-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="9d4a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d4a0-107">EXAMPLES</span></span>

### <span data-ttu-id="9d4a0-108">Przykład 1. Tworzenie obiektu wyboru wymiaru</span><span class="sxs-lookup"><span data-stu-id="9d4a0-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="9d4a0-109">To polecenie tworzy obiekt wyboru wymiaru, który określa, że {1,3,4} należy wybrać wartości dla wymiaru LUN.</span><span class="sxs-lookup"><span data-stu-id="9d4a0-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="9d4a0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d4a0-110">PARAMETERS</span></span>

### <span data-ttu-id="9d4a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d4a0-111">-DefaultProfile</span></span>
<span data-ttu-id="9d4a0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d4a0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d4a0-113">-Dimensionname</span><span class="sxs-lookup"><span data-stu-id="9d4a0-113">-DimensionName</span></span>
<span data-ttu-id="9d4a0-114">Nazwa wymiaru</span><span class="sxs-lookup"><span data-stu-id="9d4a0-114">The Dimension name</span></span>

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

### <span data-ttu-id="9d4a0-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="9d4a0-115">-ValuesToExclude</span></span>
<span data-ttu-id="9d4a0-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="9d4a0-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="9d4a0-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="9d4a0-117">-ValuesToInclude</span></span>
<span data-ttu-id="9d4a0-118">IncludeValues</span><span class="sxs-lookup"><span data-stu-id="9d4a0-118">The IncludeValues</span></span>

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

### <span data-ttu-id="9d4a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d4a0-119">CommonParameters</span></span>
<span data-ttu-id="9d4a0-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d4a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d4a0-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d4a0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d4a0-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d4a0-122">INPUTS</span></span>

### <span data-ttu-id="9d4a0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9d4a0-123">System.String</span></span>

### <span data-ttu-id="9d4a0-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="9d4a0-124">System.String[]</span></span>

## <span data-ttu-id="9d4a0-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d4a0-125">OUTPUTS</span></span>

### <span data-ttu-id="9d4a0-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="9d4a0-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="9d4a0-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d4a0-127">NOTES</span></span>

## <span data-ttu-id="9d4a0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d4a0-128">RELATED LINKS</span></span>
