---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: 696332f18074108fd0294248223777c15be0435d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888562"
---
# <span data-ttu-id="0b92f-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="0b92f-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="0b92f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b92f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b92f-103">Pobiera metryki dla gniazda aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0b92f-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="0b92f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b92f-104">SYNTAX</span></span>

### <span data-ttu-id="0b92f-105">S1</span><span class="sxs-lookup"><span data-stu-id="0b92f-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b92f-106">S2</span><span class="sxs-lookup"><span data-stu-id="0b92f-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b92f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0b92f-107">DESCRIPTION</span></span>
<span data-ttu-id="0b92f-108">**AzWebAppSlotMetric** pobiera metryki aplikacji sieci Web dla określonego gniazda.</span><span class="sxs-lookup"><span data-stu-id="0b92f-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="0b92f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b92f-109">EXAMPLES</span></span>

### <span data-ttu-id="0b92f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0b92f-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="0b92f-111">To polecenie pobiera żądanie określonej aplikacji sieci Web na minutę (PT1M — czas sondowania: 1 minuta) między godziną rozpoczęcia a EndTime.</span><span class="sxs-lookup"><span data-stu-id="0b92f-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="0b92f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b92f-112">PARAMETERS</span></span>

### <span data-ttu-id="0b92f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b92f-113">-DefaultProfile</span></span>
<span data-ttu-id="0b92f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b92f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b92f-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0b92f-115">-EndTime</span></span>
<span data-ttu-id="0b92f-116">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="0b92f-116">End Time in UTC</span></span>

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

### <span data-ttu-id="0b92f-117">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="0b92f-117">-Granularity</span></span>
<span data-ttu-id="0b92f-118">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="0b92f-118">Granularity</span></span>

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

### <span data-ttu-id="0b92f-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="0b92f-119">-InstanceDetails</span></span>
<span data-ttu-id="0b92f-120">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="0b92f-120">Instance Details</span></span>

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

### <span data-ttu-id="0b92f-121">-Metryki</span><span class="sxs-lookup"><span data-stu-id="0b92f-121">-Metrics</span></span>
<span data-ttu-id="0b92f-122">Miar</span><span class="sxs-lookup"><span data-stu-id="0b92f-122">Metrics</span></span>

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

### <span data-ttu-id="0b92f-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b92f-123">-Name</span></span>
<span data-ttu-id="0b92f-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="0b92f-124">WebApp Name</span></span>

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

### <span data-ttu-id="0b92f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b92f-125">-ResourceGroupName</span></span>
<span data-ttu-id="0b92f-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0b92f-126">Resource Group Name</span></span>

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

### <span data-ttu-id="0b92f-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="0b92f-127">-Slot</span></span>
<span data-ttu-id="0b92f-128">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="0b92f-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0b92f-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0b92f-129">-StartTime</span></span>
<span data-ttu-id="0b92f-130">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="0b92f-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="0b92f-131">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="0b92f-131">-WebApp</span></span>
<span data-ttu-id="0b92f-132">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="0b92f-132">WebApp Object</span></span>

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

### <span data-ttu-id="0b92f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b92f-133">CommonParameters</span></span>
<span data-ttu-id="0b92f-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b92f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b92f-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b92f-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b92f-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b92f-136">INPUTS</span></span>

### <span data-ttu-id="0b92f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0b92f-137">System.String</span></span>

### <span data-ttu-id="0b92f-138">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="0b92f-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0b92f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b92f-139">OUTPUTS</span></span>

### <span data-ttu-id="0b92f-140">Microsoft. Azure. Management. Web. MODELES. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="0b92f-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="0b92f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b92f-141">NOTES</span></span>

## <span data-ttu-id="0b92f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b92f-142">RELATED LINKS</span></span>

[<span data-ttu-id="0b92f-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="0b92f-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="0b92f-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0b92f-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0b92f-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0b92f-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
