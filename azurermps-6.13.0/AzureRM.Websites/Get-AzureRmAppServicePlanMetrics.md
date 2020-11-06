---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: a8bb330315cfdd43e30ab790afcdeba0b09cef08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546343"
---
# <span data-ttu-id="4c309-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="4c309-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="4c309-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c309-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c309-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c309-103">SYNTAX</span></span>

### <span data-ttu-id="4c309-104">S1</span><span class="sxs-lookup"><span data-stu-id="4c309-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c309-105">S2</span><span class="sxs-lookup"><span data-stu-id="4c309-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c309-106">Opis</span><span class="sxs-lookup"><span data-stu-id="4c309-106">DESCRIPTION</span></span>
<span data-ttu-id="4c309-107">**Get-AzureRmAppServicePlanMetrics** pobiera metryki planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="4c309-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="4c309-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c309-108">EXAMPLES</span></span>

### <span data-ttu-id="4c309-109">1:1</span><span class="sxs-lookup"><span data-stu-id="4c309-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="4c309-110">To polecenie pobiera wartość procentową CPU planu usługi App Service na minutę (PT1M — czas sondowania: 1 minuta) między godzinami rozpoczęcia i EndTime</span><span class="sxs-lookup"><span data-stu-id="4c309-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="4c309-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c309-111">PARAMETERS</span></span>

### <span data-ttu-id="4c309-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4c309-112">-AppServicePlan</span></span>
<span data-ttu-id="4c309-113">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="4c309-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c309-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c309-114">-DefaultProfile</span></span>
<span data-ttu-id="4c309-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c309-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c309-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4c309-116">-EndTime</span></span>
<span data-ttu-id="4c309-117">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="4c309-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c309-118">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="4c309-118">-Granularity</span></span>
<span data-ttu-id="4c309-119">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="4c309-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c309-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="4c309-120">-InstanceDetails</span></span>
<span data-ttu-id="4c309-121">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="4c309-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c309-122">-Metryki</span><span class="sxs-lookup"><span data-stu-id="4c309-122">-Metrics</span></span>
<span data-ttu-id="4c309-123">Miar</span><span class="sxs-lookup"><span data-stu-id="4c309-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c309-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c309-124">-Name</span></span>
<span data-ttu-id="4c309-125">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="4c309-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c309-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c309-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c309-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4c309-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c309-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4c309-128">-StartTime</span></span>
<span data-ttu-id="4c309-129">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="4c309-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c309-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c309-130">CommonParameters</span></span>
<span data-ttu-id="4c309-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c309-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c309-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c309-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c309-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c309-133">INPUTS</span></span>

### <span data-ttu-id="4c309-134">Microsoft. Azure. Management. Web. MODELES. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4c309-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="4c309-135">Parametry: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4c309-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="4c309-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c309-136">OUTPUTS</span></span>

### <span data-ttu-id="4c309-137">Microsoft. Azure. Management. Web. MODELES. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="4c309-137">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="4c309-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c309-138">NOTES</span></span>

## <span data-ttu-id="4c309-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c309-139">RELATED LINKS</span></span>
