---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222952"
---
# <span data-ttu-id="1c4fc-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="1c4fc-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="1c4fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c4fc-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4fc-103">Uzyskaj zbiorcze zalecenie dotyczące zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="1c4fc-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="1c4fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c4fc-104">SYNTAX</span></span>

### <span data-ttu-id="1c4fc-105">SolutionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c4fc-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c4fc-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="1c4fc-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c4fc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1c4fc-107">DESCRIPTION</span></span>
<span data-ttu-id="1c4fc-108">Polecenie cmdlet Get-AzIotSecurityAnalyticsAggregatedAlert zwraca co najmniej jedno zagregowane rekomendacje na urządzeniach Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="1c4fc-109">Nazwa zagregowanego zalecenia to typ</span><span class="sxs-lookup"><span data-stu-id="1c4fc-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="1c4fc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c4fc-110">EXAMPLES</span></span>

### <span data-ttu-id="1c4fc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c4fc-111">Example 1</span></span>
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

<span data-ttu-id="1c4fc-112">Uzyskiwanie zagregowanego rekomendacji "IoT_OpenPorts" w rozwiązaniu bezpieczeństwa "Moje rozwiązanie" i Grupa zasobów "Moja rezasób"</span><span class="sxs-lookup"><span data-stu-id="1c4fc-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="1c4fc-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1c4fc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="1c4fc-114">Zapoznaj się z listą zbiorczych rekomendacji dotyczących rozwiązania zabezpieczeń "Moje rozwiązanie" i Grupa zasobów "Moja zasobów".</span><span class="sxs-lookup"><span data-stu-id="1c4fc-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="1c4fc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c4fc-115">PARAMETERS</span></span>

### <span data-ttu-id="1c4fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4fc-116">-DefaultProfile</span></span>
<span data-ttu-id="1c4fc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c4fc-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c4fc-118">-Name</span></span>
<span data-ttu-id="1c4fc-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-119">Resource name.</span></span>

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

### <span data-ttu-id="1c4fc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c4fc-120">-ResourceGroupName</span></span>
<span data-ttu-id="1c4fc-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-121">Resource group name.</span></span>

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

### <span data-ttu-id="1c4fc-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="1c4fc-122">-SolutionName</span></span>
<span data-ttu-id="1c4fc-123">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="1c4fc-123">Solution name</span></span>

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

### <span data-ttu-id="1c4fc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4fc-124">CommonParameters</span></span>
<span data-ttu-id="1c4fc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c4fc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4fc-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c4fc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4fc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c4fc-127">INPUTS</span></span>

### <span data-ttu-id="1c4fc-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1c4fc-128">None</span></span>

## <span data-ttu-id="1c4fc-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c4fc-129">OUTPUTS</span></span>

### <span data-ttu-id="1c4fc-130">Microsoft. Azure. Commands. Security. models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="1c4fc-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="1c4fc-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c4fc-131">NOTES</span></span>

## <span data-ttu-id="1c4fc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c4fc-132">RELATED LINKS</span></span>
