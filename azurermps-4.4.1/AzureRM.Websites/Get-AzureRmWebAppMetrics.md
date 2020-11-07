---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppMetrics.md
ms.openlocfilehash: 00e8814c72f0e9d52fae2504a41bef3e8e94e7ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717540"
---
# <span data-ttu-id="654ab-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="654ab-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="654ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="654ab-102">SYNOPSIS</span></span>
<span data-ttu-id="654ab-103">Pobiera metryki aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="654ab-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="654ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="654ab-104">SYNTAX</span></span>

### <span data-ttu-id="654ab-105">S1</span><span class="sxs-lookup"><span data-stu-id="654ab-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="654ab-106">S2</span><span class="sxs-lookup"><span data-stu-id="654ab-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="654ab-107">Opis</span><span class="sxs-lookup"><span data-stu-id="654ab-107">DESCRIPTION</span></span>
<span data-ttu-id="654ab-108">**AzureRmWebAppMetrics** pobiera metryki aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="654ab-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="654ab-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="654ab-109">EXAMPLES</span></span>

### <span data-ttu-id="654ab-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="654ab-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="654ab-111">To polecenie pobiera żądania ContosoWebApp aplikacji sieci Web za minutę (PT1M — czas sondowania: 1 minuta) między godziną rozpoczęcia a EndTime</span><span class="sxs-lookup"><span data-stu-id="654ab-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="654ab-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="654ab-112">PARAMETERS</span></span>

### <span data-ttu-id="654ab-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="654ab-113">-EndTime</span></span>
<span data-ttu-id="654ab-114">Czas zakończenia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="654ab-114">End Time in UTC</span></span>

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

### <span data-ttu-id="654ab-115">-Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="654ab-115">-Granularity</span></span>
<span data-ttu-id="654ab-116">Ziarnistość</span><span class="sxs-lookup"><span data-stu-id="654ab-116">Granularity</span></span>

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

### <span data-ttu-id="654ab-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="654ab-117">-InstanceDetails</span></span>
<span data-ttu-id="654ab-118">Szczegóły wystąpienia</span><span class="sxs-lookup"><span data-stu-id="654ab-118">Instance Details</span></span>

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

### <span data-ttu-id="654ab-119">-Metryki</span><span class="sxs-lookup"><span data-stu-id="654ab-119">-Metrics</span></span>
<span data-ttu-id="654ab-120">Metryki jako tablicę ciągów</span><span class="sxs-lookup"><span data-stu-id="654ab-120">Metrics as a string array</span></span>

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

### <span data-ttu-id="654ab-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="654ab-121">-Name</span></span>
<span data-ttu-id="654ab-122">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="654ab-122">WebApp Name</span></span>

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

### <span data-ttu-id="654ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="654ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="654ab-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="654ab-124">Resource Group Name</span></span>

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

### <span data-ttu-id="654ab-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="654ab-125">-StartTime</span></span>
<span data-ttu-id="654ab-126">Czas rozpoczęcia w formacie UTC</span><span class="sxs-lookup"><span data-stu-id="654ab-126">Start Time in UTC</span></span>

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

### <span data-ttu-id="654ab-127">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="654ab-127">-WebApp</span></span>
<span data-ttu-id="654ab-128">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="654ab-128">WebApp object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="654ab-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="654ab-129">-DefaultProfile</span></span>
<span data-ttu-id="654ab-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="654ab-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="654ab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="654ab-131">CommonParameters</span></span>
<span data-ttu-id="654ab-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="654ab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="654ab-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="654ab-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="654ab-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="654ab-134">INPUTS</span></span>

### <span data-ttu-id="654ab-135">Klienta</span><span class="sxs-lookup"><span data-stu-id="654ab-135">Site</span></span>
<span data-ttu-id="654ab-136">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="654ab-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="654ab-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="654ab-137">OUTPUTS</span></span>

## <span data-ttu-id="654ab-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="654ab-138">NOTES</span></span>

## <span data-ttu-id="654ab-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="654ab-139">RELATED LINKS</span></span>

[<span data-ttu-id="654ab-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="654ab-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

