---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplanmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlanMetric.md
ms.openlocfilehash: d3a2cd8d0907d26a137df547f1599c9ed09cb7b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895089"
---
# <span data-ttu-id="e2894-101">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="e2894-101">Get-AzAppServicePlanMetric</span></span>

## <span data-ttu-id="e2894-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2894-102">SYNOPSIS</span></span>

## <span data-ttu-id="e2894-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2894-103">SYNTAX</span></span>

### <span data-ttu-id="e2894-104">S1</span><span class="sxs-lookup"><span data-stu-id="e2894-104">S1</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2894-105">S2</span><span class="sxs-lookup"><span data-stu-id="e2894-105">S2</span></span>
```
Get-AzAppServicePlanMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2894-106">Opis</span><span class="sxs-lookup"><span data-stu-id="e2894-106">DESCRIPTION</span></span>
<span data-ttu-id="e2894-107">**Get-AzAppServicePlanMetric** pobiera metryki planu usługi App Service.</span><span class="sxs-lookup"><span data-stu-id="e2894-107">The **Get-AzAppServicePlanMetric** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="e2894-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2894-108">EXAMPLES</span></span>

### <span data-ttu-id="e2894-109">1:1</span><span class="sxs-lookup"><span data-stu-id="e2894-109">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="e2894-110">To polecenie pobiera wartość procentową CPU planu usługi App Service na minutę (PT1M — czas sondowania: 1 minuta) między godzinami rozpoczęcia i EndTime</span><span class="sxs-lookup"><span data-stu-id="e2894-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="e2894-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2894-111">PARAMETERS</span></span>

### <span data-ttu-id="e2894-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2894-112">-AppServicePlan</span></span>
<span data-ttu-id="e2894-113">Obiekt plan usługi App Service</span><span class="sxs-lookup"><span data-stu-id="e2894-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="e2894-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2894-114">-DefaultProfile</span></span>
<span data-ttu-id="e2894-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2894-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2894-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e2894-116">-EndTime</span></span>
<span data-ttu-id="e2894-117">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="e2894-117">End Time in UTC</span></span>

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

### <span data-ttu-id="e2894-118">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="e2894-118">-Granularity</span></span>
<span data-ttu-id="e2894-119">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="e2894-119">Granularity</span></span>

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

### <span data-ttu-id="e2894-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="e2894-120">-InstanceDetails</span></span>
<span data-ttu-id="e2894-121">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="e2894-121">Instance Details</span></span>

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

### <span data-ttu-id="e2894-122">-Metryki</span><span class="sxs-lookup"><span data-stu-id="e2894-122">-Metrics</span></span>
<span data-ttu-id="e2894-123">Miar</span><span class="sxs-lookup"><span data-stu-id="e2894-123">Metrics</span></span>

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

### <span data-ttu-id="e2894-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2894-124">-Name</span></span>
<span data-ttu-id="e2894-125">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="e2894-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="e2894-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2894-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2894-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e2894-127">Resource Group Name</span></span>

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

### <span data-ttu-id="e2894-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e2894-128">-StartTime</span></span>
<span data-ttu-id="e2894-129">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="e2894-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="e2894-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2894-130">CommonParameters</span></span>
<span data-ttu-id="e2894-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2894-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2894-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2894-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2894-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2894-133">INPUTS</span></span>

### <span data-ttu-id="e2894-134">Microsoft. Azure. Commands. webapps. modele. aplikacji. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e2894-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="e2894-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2894-135">OUTPUTS</span></span>

### <span data-ttu-id="e2894-136">Microsoft. Azure. Management. Web. MODELES. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="e2894-136">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="e2894-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2894-137">NOTES</span></span>

## <span data-ttu-id="e2894-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2894-138">RELATED LINKS</span></span>
