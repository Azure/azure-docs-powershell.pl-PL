---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891958"
---
# <span data-ttu-id="6d3ea-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="6d3ea-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="6d3ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3ea-103">Pobiera metryki planu usługi sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="6d3ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d3ea-104">SYNTAX</span></span>

### <span data-ttu-id="6d3ea-105">S1</span><span class="sxs-lookup"><span data-stu-id="6d3ea-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d3ea-106">S2</span><span class="sxs-lookup"><span data-stu-id="6d3ea-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d3ea-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6d3ea-107">DESCRIPTION</span></span>
<span data-ttu-id="6d3ea-108">**Get-AzAppServicePlanMetrics** pobiera metryki planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="6d3ea-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d3ea-109">EXAMPLES</span></span>

### <span data-ttu-id="6d3ea-110">1:1</span><span class="sxs-lookup"><span data-stu-id="6d3ea-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="6d3ea-111">To polecenie pobiera wartość procentową CPU planu usługi App Service na minutę (PT1M — czas sondowania: 1 minuta) między godzinami rozpoczęcia i EndTime</span><span class="sxs-lookup"><span data-stu-id="6d3ea-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="6d3ea-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d3ea-112">PARAMETERS</span></span>

### <span data-ttu-id="6d3ea-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6d3ea-113">-AppServicePlan</span></span>
<span data-ttu-id="6d3ea-114">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="6d3ea-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ea-115">-DefaultProfile</span></span>
<span data-ttu-id="6d3ea-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6d3ea-117">-EndTime</span></span>
<span data-ttu-id="6d3ea-118">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="6d3ea-118">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-119">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="6d3ea-119">-Granularity</span></span>
<span data-ttu-id="6d3ea-120">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="6d3ea-120">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-121">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="6d3ea-121">-InstanceDetails</span></span>
<span data-ttu-id="6d3ea-122">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="6d3ea-122">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-123">-Metryki</span><span class="sxs-lookup"><span data-stu-id="6d3ea-123">-Metrics</span></span>
<span data-ttu-id="6d3ea-124">Miar</span><span class="sxs-lookup"><span data-stu-id="6d3ea-124">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6d3ea-125">-Name</span></span>
<span data-ttu-id="6d3ea-126">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="6d3ea-126">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d3ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d3ea-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6d3ea-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6d3ea-129">-StartTime</span></span>
<span data-ttu-id="6d3ea-130">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="6d3ea-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3ea-131">CommonParameters</span></span>
<span data-ttu-id="6d3ea-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3ea-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d3ea-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3ea-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d3ea-134">INPUTS</span></span>

### <span data-ttu-id="6d3ea-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="6d3ea-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="6d3ea-136">Parametr "AppServicePlan" akceptuje wartość typu "ServerFarmWithRichSku" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6d3ea-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="6d3ea-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d3ea-137">OUTPUTS</span></span>

## <span data-ttu-id="6d3ea-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d3ea-138">NOTES</span></span>

## <span data-ttu-id="6d3ea-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d3ea-139">RELATED LINKS</span></span>

