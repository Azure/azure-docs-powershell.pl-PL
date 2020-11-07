---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: 4cb978b33b6bcb68d400f33fb2da06747ce9b763
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718199"
---
# <span data-ttu-id="15323-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="15323-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="15323-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15323-102">SYNOPSIS</span></span>
<span data-ttu-id="15323-103">Pobiera definicje metryk.</span><span class="sxs-lookup"><span data-stu-id="15323-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15323-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15323-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15323-105">Opis</span><span class="sxs-lookup"><span data-stu-id="15323-105">DESCRIPTION</span></span>
<span data-ttu-id="15323-106">Polecenie cmdlet **Get-AzureRmMetricDefinition** umożliwia pobieranie definicji metryk.</span><span class="sxs-lookup"><span data-stu-id="15323-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="15323-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15323-107">EXAMPLES</span></span>

### <span data-ttu-id="15323-108">Przykład 1: uzyskiwanie definicji metryk dla zasobu</span><span class="sxs-lookup"><span data-stu-id="15323-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="15323-109">To polecenie pobiera definicje metryk dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="15323-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="15323-110">Przykład 2: uzyskiwanie definicji metryk ze szczegółowym wyjściem</span><span class="sxs-lookup"><span data-stu-id="15323-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="15323-111">To polecenie pobiera definicje metryk dla website2.</span><span class="sxs-lookup"><span data-stu-id="15323-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="15323-112">Wynik jest szczegółowy.</span><span class="sxs-lookup"><span data-stu-id="15323-112">The output is detailed.</span></span>

### <span data-ttu-id="15323-113">Przykład 3: uzyskiwanie definicji metryk według nazw</span><span class="sxs-lookup"><span data-stu-id="15323-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="15323-114">To polecenie pobiera definicje metryk BytesSent i CpuTime.</span><span class="sxs-lookup"><span data-stu-id="15323-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="15323-115">Wynik jest szczegółowy.</span><span class="sxs-lookup"><span data-stu-id="15323-115">The output is detailed.</span></span>

## <span data-ttu-id="15323-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15323-116">PARAMETERS</span></span>

### <span data-ttu-id="15323-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="15323-117">-DetailedOutput</span></span>
<span data-ttu-id="15323-118">Wskazuje, że ta operacja zawiera szczegółowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="15323-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="15323-119">Jeśli ten parametr nie zostanie określony, dane wyjściowe zostaną podsumowane.</span><span class="sxs-lookup"><span data-stu-id="15323-119">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15323-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="15323-120">-MetricNames</span></span>
<span data-ttu-id="15323-121">Określa tablicę nazw metryk.</span><span class="sxs-lookup"><span data-stu-id="15323-121">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="15323-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15323-122">-ResourceId</span></span>
<span data-ttu-id="15323-123">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="15323-123">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15323-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15323-124">-DefaultProfile</span></span>
<span data-ttu-id="15323-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="15323-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15323-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15323-126">CommonParameters</span></span>
<span data-ttu-id="15323-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15323-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15323-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15323-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15323-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15323-129">INPUTS</span></span>

## <span data-ttu-id="15323-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15323-130">OUTPUTS</span></span>

### <span data-ttu-id="15323-131">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition []</span><span class="sxs-lookup"><span data-stu-id="15323-131">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="15323-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15323-132">NOTES</span></span>

## <span data-ttu-id="15323-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15323-133">RELATED LINKS</span></span>

[<span data-ttu-id="15323-134">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="15323-134">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


