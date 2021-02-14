---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176346"
---
# <span data-ttu-id="d49a8-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="d49a8-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="d49a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d49a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d49a8-103">Uzyskaj zagregowane zalecenie dotyczące zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="d49a8-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="d49a8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d49a8-104">SYNTAX</span></span>

### <span data-ttu-id="d49a8-105">SolutionScope (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d49a8-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d49a8-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d49a8-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d49a8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d49a8-107">DESCRIPTION</span></span>
<span data-ttu-id="d49a8-108">Polecenie Get-AzIotSecurityAnalyticsAggregatedAlert zwraca co najmniej jedno zagregowane zalecenia dotyczące urządzeń centrum iot.</span><span class="sxs-lookup"><span data-stu-id="d49a8-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="d49a8-109">Nazwa zagregowanego zalecenia jest jej typem</span><span class="sxs-lookup"><span data-stu-id="d49a8-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="d49a8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d49a8-110">EXAMPLES</span></span>

### <span data-ttu-id="d49a8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d49a8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="d49a8-112">Uzyskaj zagregowane zalecenie "IoT_OpenPorts" w rozwiązaniu zabezpieczeń "MySolution" i grupie zasobów "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="d49a8-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="d49a8-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d49a8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="d49a8-114">Uzyskiwanie listy zagregowanych zaleceń w rozwiązaniu zabezpieczeń "MySolution" i grupie zasobów "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="d49a8-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="d49a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d49a8-115">PARAMETERS</span></span>

### <span data-ttu-id="d49a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49a8-116">-DefaultProfile</span></span>
<span data-ttu-id="d49a8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d49a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d49a8-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d49a8-118">-Name</span></span>
<span data-ttu-id="d49a8-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d49a8-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d49a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="d49a8-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d49a8-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49a8-122">—SolutionName</span><span class="sxs-lookup"><span data-stu-id="d49a8-122">-SolutionName</span></span>
<span data-ttu-id="d49a8-123">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="d49a8-123">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49a8-124">CommonParameters</span></span>
<span data-ttu-id="d49a8-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d49a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49a8-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d49a8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49a8-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d49a8-127">INPUTS</span></span>

### <span data-ttu-id="d49a8-128">Brak</span><span class="sxs-lookup"><span data-stu-id="d49a8-128">None</span></span>

## <span data-ttu-id="d49a8-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d49a8-129">OUTPUTS</span></span>

### <span data-ttu-id="d49a8-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="d49a8-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="d49a8-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d49a8-131">NOTES</span></span>

## <span data-ttu-id="d49a8-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d49a8-132">RELATED LINKS</span></span>
