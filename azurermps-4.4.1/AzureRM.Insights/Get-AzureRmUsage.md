---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551000"
---
# <span data-ttu-id="1c0b2-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="1c0b2-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="1c0b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0b2-103">Pobiera metryki użycia zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c0b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c0b2-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c0b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c0b2-105">DESCRIPTION</span></span>
<span data-ttu-id="1c0b2-106">Polecenie cmdlet **Get-AzureRmUsage** pobiera metryki użycia określonego zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="1c0b2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c0b2-107">EXAMPLES</span></span>

### <span data-ttu-id="1c0b2-108">Przykład 1: uzyskiwanie metryki użycia według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="1c0b2-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="1c0b2-109">To polecenie pobiera metryki użycia dla określonej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="1c0b2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c0b2-110">PARAMETERS</span></span>

### <span data-ttu-id="1c0b2-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1c0b2-111">-ApiVersion</span></span>
<span data-ttu-id="1c0b2-112">Określa ciąg wersji API, na przykład 2014-04-01, który jest akceptowany przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c0b2-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1c0b2-113">-EndTime</span></span>
<span data-ttu-id="1c0b2-114">Określa najnowszą godzinę i datę wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="1c0b2-115">Możesz użyć polecenia cmdlet Get-Date, aby uzyskać obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="1c0b2-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c0b2-116">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="1c0b2-116">-MetricNames</span></span>
<span data-ttu-id="1c0b2-117">Określa tablicę nazw metryk.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-117">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="1c0b2-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c0b2-118">-ResourceId</span></span>
<span data-ttu-id="1c0b2-119">Określa identyfikator zasobu dla metryki.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-119">Specifies the ID of the resource for the metric.</span></span>

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

### <span data-ttu-id="1c0b2-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1c0b2-120">-StartTime</span></span>
<span data-ttu-id="1c0b2-121">Określa najwcześniejszą godzinę i datę wyszukania.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="1c0b2-122">Możesz użyć polecenia cmdlet Get-Date, aby uzyskać obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="1c0b2-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c0b2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0b2-123">-DefaultProfile</span></span>
<span data-ttu-id="1c0b2-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c0b2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0b2-125">CommonParameters</span></span>
<span data-ttu-id="1c0b2-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0b2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0b2-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c0b2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0b2-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c0b2-128">INPUTS</span></span>

## <span data-ttu-id="1c0b2-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c0b2-129">OUTPUTS</span></span>

### <span data-ttu-id="1c0b2-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSUsageMetric []</span><span class="sxs-lookup"><span data-stu-id="1c0b2-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="1c0b2-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c0b2-131">NOTES</span></span>

## <span data-ttu-id="1c0b2-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c0b2-132">RELATED LINKS</span></span>

[<span data-ttu-id="1c0b2-133">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="1c0b2-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


