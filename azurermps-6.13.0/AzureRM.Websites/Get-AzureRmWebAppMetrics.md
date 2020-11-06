---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 47fa876ff021dd920627ce4f08089c5fd04fb885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543303"
---
# <span data-ttu-id="9e5e8-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="9e5e8-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="9e5e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5e8-103">Pobiera metryki aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9e5e8-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e5e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e5e8-104">SYNTAX</span></span>

### <span data-ttu-id="9e5e8-105">S1</span><span class="sxs-lookup"><span data-stu-id="9e5e8-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e5e8-106">S2</span><span class="sxs-lookup"><span data-stu-id="9e5e8-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e5e8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9e5e8-107">DESCRIPTION</span></span>
<span data-ttu-id="9e5e8-108">**AzureRmWebAppMetrics** pobiera metryki aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="9e5e8-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="9e5e8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e5e8-109">EXAMPLES</span></span>

### <span data-ttu-id="9e5e8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e5e8-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="9e5e8-111">To polecenie pobiera żądania ContosoWebApp aplikacji sieci Web za minutę (PT1M — czas sondowania: 1 minuta) między godziną rozpoczęcia a EndTime</span><span class="sxs-lookup"><span data-stu-id="9e5e8-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="9e5e8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e5e8-112">PARAMETERS</span></span>

### <span data-ttu-id="9e5e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5e8-113">-DefaultProfile</span></span>
<span data-ttu-id="9e5e8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e5e8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e5e8-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9e5e8-115">-EndTime</span></span>
<span data-ttu-id="9e5e8-116">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="9e5e8-116">End Time in UTC</span></span>

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

### <span data-ttu-id="9e5e8-117">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="9e5e8-117">-Granularity</span></span>
<span data-ttu-id="9e5e8-118">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="9e5e8-118">Granularity</span></span>

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

### <span data-ttu-id="9e5e8-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="9e5e8-119">-InstanceDetails</span></span>
<span data-ttu-id="9e5e8-120">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="9e5e8-120">Instance Details</span></span>

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

### <span data-ttu-id="9e5e8-121">-Metryki</span><span class="sxs-lookup"><span data-stu-id="9e5e8-121">-Metrics</span></span>
<span data-ttu-id="9e5e8-122">Metryki jako tablicę ciągów</span><span class="sxs-lookup"><span data-stu-id="9e5e8-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="9e5e8-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e5e8-123">-Name</span></span>
<span data-ttu-id="9e5e8-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="9e5e8-124">WebApp Name</span></span>

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

### <span data-ttu-id="9e5e8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e5e8-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e5e8-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9e5e8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="9e5e8-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9e5e8-127">-StartTime</span></span>
<span data-ttu-id="9e5e8-128">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="9e5e8-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="9e5e8-129">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="9e5e8-129">-WebApp</span></span>
<span data-ttu-id="9e5e8-130">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="9e5e8-130">WebApp object</span></span>

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

### <span data-ttu-id="9e5e8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5e8-131">CommonParameters</span></span>
<span data-ttu-id="9e5e8-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e5e8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5e8-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e5e8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5e8-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e5e8-134">INPUTS</span></span>

### <span data-ttu-id="9e5e8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9e5e8-135">System.String</span></span>

### <span data-ttu-id="9e5e8-136">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="9e5e8-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="9e5e8-137">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9e5e8-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="9e5e8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e5e8-138">OUTPUTS</span></span>

### <span data-ttu-id="9e5e8-139">Microsoft. Azure. Management. Web. MODELES. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="9e5e8-139">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="9e5e8-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e5e8-140">NOTES</span></span>

## <span data-ttu-id="9e5e8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e5e8-141">RELATED LINKS</span></span>

[<span data-ttu-id="9e5e8-142">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="9e5e8-142">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

