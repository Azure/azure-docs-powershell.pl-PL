---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
ms.openlocfilehash: 1382ec0f4a2eaa61493e05a762616d9fac54a7f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897765"
---
# <span data-ttu-id="3c22f-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="3c22f-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="3c22f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c22f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c22f-103">Pobiera metryki aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3c22f-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c22f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c22f-104">SYNTAX</span></span>

### <span data-ttu-id="3c22f-105">S1</span><span class="sxs-lookup"><span data-stu-id="3c22f-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c22f-106">S2</span><span class="sxs-lookup"><span data-stu-id="3c22f-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c22f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3c22f-107">DESCRIPTION</span></span>
<span data-ttu-id="3c22f-108">**AzureRmWebAppMetrics** pobiera metryki aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="3c22f-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="3c22f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c22f-109">EXAMPLES</span></span>

### <span data-ttu-id="3c22f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c22f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="3c22f-111">To polecenie pobiera żądania ContosoWebApp aplikacji sieci Web za minutę (PT1M — czas sondowania: 1 minuta) między godziną rozpoczęcia a EndTime</span><span class="sxs-lookup"><span data-stu-id="3c22f-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="3c22f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c22f-112">PARAMETERS</span></span>

### <span data-ttu-id="3c22f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c22f-113">-DefaultProfile</span></span>
<span data-ttu-id="3c22f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c22f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c22f-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3c22f-115">-EndTime</span></span>
<span data-ttu-id="3c22f-116">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="3c22f-116">End Time in UTC</span></span>

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

### <span data-ttu-id="3c22f-117">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="3c22f-117">-Granularity</span></span>
<span data-ttu-id="3c22f-118">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="3c22f-118">Granularity</span></span>

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

### <span data-ttu-id="3c22f-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="3c22f-119">-InstanceDetails</span></span>
<span data-ttu-id="3c22f-120">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="3c22f-120">Instance Details</span></span>

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

### <span data-ttu-id="3c22f-121">-Metryki</span><span class="sxs-lookup"><span data-stu-id="3c22f-121">-Metrics</span></span>
<span data-ttu-id="3c22f-122">Metryki jako tablicę ciągów</span><span class="sxs-lookup"><span data-stu-id="3c22f-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="3c22f-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3c22f-123">-Name</span></span>
<span data-ttu-id="3c22f-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="3c22f-124">WebApp Name</span></span>

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

### <span data-ttu-id="3c22f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c22f-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c22f-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3c22f-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3c22f-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3c22f-127">-StartTime</span></span>
<span data-ttu-id="3c22f-128">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="3c22f-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="3c22f-129">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="3c22f-129">-WebApp</span></span>
<span data-ttu-id="3c22f-130">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="3c22f-130">WebApp object</span></span>

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

### <span data-ttu-id="3c22f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c22f-131">CommonParameters</span></span>
<span data-ttu-id="3c22f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c22f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c22f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c22f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c22f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c22f-134">INPUTS</span></span>

### <span data-ttu-id="3c22f-135">Klienta</span><span class="sxs-lookup"><span data-stu-id="3c22f-135">Site</span></span>
<span data-ttu-id="3c22f-136">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="3c22f-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3c22f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c22f-137">OUTPUTS</span></span>

## <span data-ttu-id="3c22f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c22f-138">NOTES</span></span>

## <span data-ttu-id="3c22f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c22f-139">RELATED LINKS</span></span>

[<span data-ttu-id="3c22f-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="3c22f-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

