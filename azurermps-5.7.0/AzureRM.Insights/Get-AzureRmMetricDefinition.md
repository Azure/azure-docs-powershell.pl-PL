---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: de839f4b56f4aa1111e130bdf6396875f9aeb185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545723"
---
# <span data-ttu-id="94dad-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="94dad-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="94dad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94dad-102">SYNOPSIS</span></span>
<span data-ttu-id="94dad-103">Pobiera definicje metryk.</span><span class="sxs-lookup"><span data-stu-id="94dad-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94dad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94dad-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94dad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="94dad-105">DESCRIPTION</span></span>
<span data-ttu-id="94dad-106">Polecenie cmdlet **Get-AzureRmMetricDefinition** umożliwia pobieranie definicji metryk.</span><span class="sxs-lookup"><span data-stu-id="94dad-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="94dad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94dad-107">EXAMPLES</span></span>

### <span data-ttu-id="94dad-108">Przykład 1: uzyskiwanie definicji metryk dla zasobu</span><span class="sxs-lookup"><span data-stu-id="94dad-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="94dad-109">To polecenie pobiera definicje metryk dla określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="94dad-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="94dad-110">Przykład 2: uzyskiwanie definicji metryk ze szczegółowym wyjściem</span><span class="sxs-lookup"><span data-stu-id="94dad-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="94dad-111">To polecenie pobiera definicje metryk dla website2.</span><span class="sxs-lookup"><span data-stu-id="94dad-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="94dad-112">Wynik jest szczegółowy.</span><span class="sxs-lookup"><span data-stu-id="94dad-112">The output is detailed.</span></span>

### <span data-ttu-id="94dad-113">Przykład 3: uzyskiwanie definicji metryk według nazw</span><span class="sxs-lookup"><span data-stu-id="94dad-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="94dad-114">To polecenie pobiera definicje metryk BytesSent i CpuTime.</span><span class="sxs-lookup"><span data-stu-id="94dad-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="94dad-115">Wynik jest szczegółowy.</span><span class="sxs-lookup"><span data-stu-id="94dad-115">The output is detailed.</span></span>

## <span data-ttu-id="94dad-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94dad-116">PARAMETERS</span></span>

### <span data-ttu-id="94dad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94dad-117">-DefaultProfile</span></span>
<span data-ttu-id="94dad-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="94dad-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94dad-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="94dad-119">-DetailedOutput</span></span>
<span data-ttu-id="94dad-120">Wskazuje, że ta operacja zawiera szczegółowe dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="94dad-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="94dad-121">Jeśli ten parametr nie zostanie określony, dane wyjściowe zostaną podsumowane.</span><span class="sxs-lookup"><span data-stu-id="94dad-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94dad-122">-Metricname</span><span class="sxs-lookup"><span data-stu-id="94dad-122">-MetricName</span></span>
<span data-ttu-id="94dad-123">Określa tablicę nazw metryk.</span><span class="sxs-lookup"><span data-stu-id="94dad-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94dad-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94dad-124">-ResourceId</span></span>
<span data-ttu-id="94dad-125">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="94dad-125">Specifies the resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94dad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94dad-126">CommonParameters</span></span>
<span data-ttu-id="94dad-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94dad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94dad-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94dad-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94dad-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94dad-129">INPUTS</span></span>

### <span data-ttu-id="94dad-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="94dad-130">None</span></span>
<span data-ttu-id="94dad-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="94dad-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94dad-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94dad-132">OUTPUTS</span></span>

### <span data-ttu-id="94dad-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition []</span><span class="sxs-lookup"><span data-stu-id="94dad-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="94dad-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94dad-134">NOTES</span></span>

## <span data-ttu-id="94dad-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94dad-135">RELATED LINKS</span></span>

[<span data-ttu-id="94dad-136">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="94dad-136">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


