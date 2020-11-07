---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 604eec977e8cb821986e3dcc0690fa4dfb65b526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888505"
---
# <span data-ttu-id="b0a16-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="b0a16-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="b0a16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0a16-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a16-103">Pobiera metryki aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b0a16-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="b0a16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0a16-104">SYNTAX</span></span>

### <span data-ttu-id="b0a16-105">S1</span><span class="sxs-lookup"><span data-stu-id="b0a16-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0a16-106">S2</span><span class="sxs-lookup"><span data-stu-id="b0a16-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0a16-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b0a16-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a16-108">**AzWebAppMetric** pobiera metryki aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b0a16-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="b0a16-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0a16-109">EXAMPLES</span></span>

### <span data-ttu-id="b0a16-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0a16-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="b0a16-111">To polecenie pobiera żądania ContosoWebApp aplikacji sieci Web za minutę (PT1M — czas sondowania: 1 minuta) między godziną rozpoczęcia a EndTime</span><span class="sxs-lookup"><span data-stu-id="b0a16-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="b0a16-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0a16-112">PARAMETERS</span></span>

### <span data-ttu-id="b0a16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a16-113">-DefaultProfile</span></span>
<span data-ttu-id="b0a16-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a16-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0a16-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b0a16-115">-EndTime</span></span>
<span data-ttu-id="b0a16-116">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="b0a16-116">End Time in UTC</span></span>

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

### <span data-ttu-id="b0a16-117">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="b0a16-117">-Granularity</span></span>
<span data-ttu-id="b0a16-118">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="b0a16-118">Granularity</span></span>

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

### <span data-ttu-id="b0a16-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="b0a16-119">-InstanceDetails</span></span>
<span data-ttu-id="b0a16-120">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="b0a16-120">Instance Details</span></span>

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

### <span data-ttu-id="b0a16-121">-Metryki</span><span class="sxs-lookup"><span data-stu-id="b0a16-121">-Metrics</span></span>
<span data-ttu-id="b0a16-122">Metryki jako tablicę ciągów</span><span class="sxs-lookup"><span data-stu-id="b0a16-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="b0a16-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0a16-123">-Name</span></span>
<span data-ttu-id="b0a16-124">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b0a16-124">WebApp Name</span></span>

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

### <span data-ttu-id="b0a16-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a16-125">-ResourceGroupName</span></span>
<span data-ttu-id="b0a16-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b0a16-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b0a16-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b0a16-127">-StartTime</span></span>
<span data-ttu-id="b0a16-128">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="b0a16-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="b0a16-129">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="b0a16-129">-WebApp</span></span>
<span data-ttu-id="b0a16-130">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="b0a16-130">WebApp object</span></span>

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

### <span data-ttu-id="b0a16-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a16-131">CommonParameters</span></span>
<span data-ttu-id="b0a16-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a16-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a16-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0a16-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a16-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0a16-134">INPUTS</span></span>

### <span data-ttu-id="b0a16-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b0a16-135">System.String</span></span>

### <span data-ttu-id="b0a16-136">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="b0a16-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b0a16-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0a16-137">OUTPUTS</span></span>

### <span data-ttu-id="b0a16-138">Microsoft. Azure. Management. Web. MODELES. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="b0a16-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="b0a16-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0a16-139">NOTES</span></span>

## <span data-ttu-id="b0a16-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0a16-140">RELATED LINKS</span></span>

[<span data-ttu-id="b0a16-141">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="b0a16-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

