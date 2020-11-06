---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c336c1bb2c2485c5bef691a5d5560a1b8795360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524209"
---
# <span data-ttu-id="69868-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="69868-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="69868-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69868-102">SYNOPSIS</span></span>
<span data-ttu-id="69868-103">Pobiera metryki dla gniazda aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="69868-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69868-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69868-104">SYNTAX</span></span>

### <span data-ttu-id="69868-105">S1</span><span class="sxs-lookup"><span data-stu-id="69868-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69868-106">S2</span><span class="sxs-lookup"><span data-stu-id="69868-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69868-107">Opis</span><span class="sxs-lookup"><span data-stu-id="69868-107">DESCRIPTION</span></span>
<span data-ttu-id="69868-108">**AzureRmWebAppSlotMetrics** pobiera metryki aplikacji sieci Web dla określonego gniazda.</span><span class="sxs-lookup"><span data-stu-id="69868-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="69868-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69868-109">EXAMPLES</span></span>

### <span data-ttu-id="69868-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69868-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="69868-111">To polecenie pobiera żądanie określonej aplikacji sieci Web na minutę (PT1M — czas sondowania: 1 minuta) między godziną rozpoczęcia a EndTime.</span><span class="sxs-lookup"><span data-stu-id="69868-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="69868-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69868-112">PARAMETERS</span></span>

### <span data-ttu-id="69868-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69868-113">-DefaultProfile</span></span>
<span data-ttu-id="69868-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69868-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69868-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="69868-115">-EndTime</span></span>
<span data-ttu-id="69868-116">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="69868-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69868-117">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="69868-117">-Granularity</span></span>
<span data-ttu-id="69868-118">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="69868-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69868-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="69868-119">-InstanceDetails</span></span>
<span data-ttu-id="69868-120">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="69868-120">Instance Details</span></span>

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

### <span data-ttu-id="69868-121">-Metryki</span><span class="sxs-lookup"><span data-stu-id="69868-121">-Metrics</span></span>
<span data-ttu-id="69868-122">Miar</span><span class="sxs-lookup"><span data-stu-id="69868-122">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69868-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69868-123">-Name</span></span>
<span data-ttu-id="69868-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="69868-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69868-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69868-125">-ResourceGroupName</span></span>
<span data-ttu-id="69868-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="69868-126">Resource Group Name</span></span>

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

### <span data-ttu-id="69868-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="69868-127">-Slot</span></span>
<span data-ttu-id="69868-128">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="69868-128">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69868-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="69868-129">-StartTime</span></span>
<span data-ttu-id="69868-130">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="69868-130">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69868-131">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="69868-131">-WebApp</span></span>
<span data-ttu-id="69868-132">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="69868-132">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69868-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69868-133">CommonParameters</span></span>
<span data-ttu-id="69868-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69868-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69868-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69868-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69868-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69868-136">INPUTS</span></span>

### <span data-ttu-id="69868-137">System. String</span><span class="sxs-lookup"><span data-stu-id="69868-137">System.String</span></span>

### <span data-ttu-id="69868-138">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="69868-138">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="69868-139">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="69868-139">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="69868-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69868-140">OUTPUTS</span></span>

### <span data-ttu-id="69868-141">Microsoft. Azure. Management. Web. MODELES. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="69868-141">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="69868-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69868-142">NOTES</span></span>

## <span data-ttu-id="69868-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69868-143">RELATED LINKS</span></span>

[<span data-ttu-id="69868-144">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="69868-144">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="69868-145">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69868-145">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="69868-146">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="69868-146">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
