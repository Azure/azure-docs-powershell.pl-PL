---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c4399146d99da6317c70fc08f7b01dc9679525a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542116"
---
# <span data-ttu-id="4b729-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="4b729-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="4b729-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b729-102">SYNOPSIS</span></span>
<span data-ttu-id="4b729-103">Pobiera metryki dla gniazda aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4b729-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b729-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b729-104">SYNTAX</span></span>

### <span data-ttu-id="4b729-105">S1</span><span class="sxs-lookup"><span data-stu-id="4b729-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b729-106">S2</span><span class="sxs-lookup"><span data-stu-id="4b729-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b729-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4b729-107">DESCRIPTION</span></span>
<span data-ttu-id="4b729-108">**AzureRmWebAppSlotMetrics** pobiera metryki aplikacji sieci Web dla określonego gniazda.</span><span class="sxs-lookup"><span data-stu-id="4b729-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="4b729-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b729-109">EXAMPLES</span></span>

### <span data-ttu-id="4b729-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4b729-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="4b729-111">To polecenie pobiera żądanie określonej aplikacji sieci Web na minutę (PT1M — czas sondowania: 1 minuta) między godziną rozpoczęcia a EndTime.</span><span class="sxs-lookup"><span data-stu-id="4b729-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="4b729-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b729-112">PARAMETERS</span></span>

### <span data-ttu-id="4b729-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b729-113">-DefaultProfile</span></span>
<span data-ttu-id="4b729-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b729-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b729-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4b729-115">-EndTime</span></span>
<span data-ttu-id="4b729-116">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="4b729-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b729-117">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="4b729-117">-Granularity</span></span>
<span data-ttu-id="4b729-118">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="4b729-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b729-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="4b729-119">-InstanceDetails</span></span>
<span data-ttu-id="4b729-120">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="4b729-120">Instance Details</span></span>

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

### <span data-ttu-id="4b729-121">-Metryki</span><span class="sxs-lookup"><span data-stu-id="4b729-121">-Metrics</span></span>
<span data-ttu-id="4b729-122">Miar</span><span class="sxs-lookup"><span data-stu-id="4b729-122">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b729-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4b729-123">-Name</span></span>
<span data-ttu-id="4b729-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="4b729-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b729-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b729-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b729-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4b729-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4b729-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="4b729-127">-Slot</span></span>
<span data-ttu-id="4b729-128">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="4b729-128">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b729-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4b729-129">-StartTime</span></span>
<span data-ttu-id="4b729-130">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="4b729-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b729-131">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="4b729-131">-WebApp</span></span>
<span data-ttu-id="4b729-132">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="4b729-132">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b729-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b729-133">CommonParameters</span></span>
<span data-ttu-id="4b729-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b729-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b729-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b729-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b729-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b729-136">INPUTS</span></span>

### <span data-ttu-id="4b729-137">Klienta</span><span class="sxs-lookup"><span data-stu-id="4b729-137">Site</span></span>
<span data-ttu-id="4b729-138">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="4b729-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4b729-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b729-139">OUTPUTS</span></span>

## <span data-ttu-id="4b729-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b729-140">NOTES</span></span>

## <span data-ttu-id="4b729-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b729-141">RELATED LINKS</span></span>

[<span data-ttu-id="4b729-142">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="4b729-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="4b729-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4b729-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="4b729-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4b729-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
