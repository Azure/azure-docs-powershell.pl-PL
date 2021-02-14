---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176355"
---
# <span data-ttu-id="80d38-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="80d38-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="80d38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80d38-102">SYNOPSIS</span></span>
<span data-ttu-id="80d38-103">Alert zagregowany zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="80d38-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="80d38-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80d38-104">SYNTAX</span></span>

### <span data-ttu-id="80d38-105">SolutionScope (domyślna)</span><span class="sxs-lookup"><span data-stu-id="80d38-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80d38-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="80d38-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80d38-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="80d38-107">DESCRIPTION</span></span>
<span data-ttu-id="80d38-108">Polecenie Get-AzIotSecurityAnalyticsAggregatedAlert zwraca co najmniej jeden zagregowany alert na urządzeniach centrum iot.</span><span class="sxs-lookup"><span data-stu-id="80d38-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="80d38-109">Nazwa alertów agregowanych to kombinacja typu alertu i daty zagregowanej alertu, oddzielona przecinkiem "/".</span><span class="sxs-lookup"><span data-stu-id="80d38-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="80d38-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80d38-110">EXAMPLES</span></span>

### <span data-ttu-id="80d38-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80d38-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name "IoT_Bruteforce_Fail/2019-02-02"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedAlerts/IoT_Bruteforce_Fail/2019-02-02"
Name: "IoT_Bruteforce_Fail/2019-02-02"
Type: "Microsoft.Security/IoTSecurityAggregatedAlert"
AlertType: "IoT_Bruteforce_Fail"
AlertDisplayName: "Failed Bruteforce"
AggregatedDateUtc: "2019-02-02"
VendorName: "Microsoft"
ReportedSeverity: "Low"
RemediationSteps: ""
Description: "Multiple unsuccsseful login attempts identified. A Bruteforce attack on the device failed."
Count: 50
EffectedResourceType: "IoT Device"
SystemSource: "Devices"
ActionTaken: "Detected"
LogAnalyticsQuery: "SecurityAlert | where tolower(ResourceId) == tolower('/subscriptions/b77ec8a9-04ed-48d2-a87a-e5887b978ba6/resourceGroups/IoT-Solution-DemoEnv/providers/Microsoft.Devices/IotHubs/rtogm-hub') and tolower(AlertName) == tolower('Custom Alert - number of device to cloud messages in MQTT protocol is not in the allowed range') | extend DeviceId=parse_json(ExtendedProperties)['DeviceId'] | project DeviceId, TimeGenerated, DisplayName, AlertSeverity, Description, RemediationSteps, ExtendedProperties"
TopDevicesList: [
                {
                  DeviceId: "testDevice1"
                  AlertsCount: 45
                  LastOccurrence: "10:42"
                }
                {
                  DeviceId: "testDevice2"
                  AlertsCount: 30
                  LastOccurrence: "15:42"
                }
              ]
```

<span data-ttu-id="80d38-112">Alert zagregowany "IoT_Bruteforce_Fail-2019-02-02" (nazwa połączona z typem alertu i zagregowaną datą) w rozwiązaniu "MySolution" i grupie zasobów "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="80d38-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="80d38-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="80d38-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="80d38-114">Uzyskiwanie listy wszystkich alertów zagregowanych w rozwiązaniu "MySolution" i grupie zasobów "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="80d38-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="80d38-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80d38-115">PARAMETERS</span></span>

### <span data-ttu-id="80d38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d38-116">-DefaultProfile</span></span>
<span data-ttu-id="80d38-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="80d38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80d38-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="80d38-118">-Name</span></span>
<span data-ttu-id="80d38-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="80d38-119">Resource name.</span></span>

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

### <span data-ttu-id="80d38-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80d38-120">-ResourceGroupName</span></span>
<span data-ttu-id="80d38-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="80d38-121">Resource group name.</span></span>

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

### <span data-ttu-id="80d38-122">—SolutionName</span><span class="sxs-lookup"><span data-stu-id="80d38-122">-SolutionName</span></span>
<span data-ttu-id="80d38-123">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="80d38-123">Solution name</span></span>

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

### <span data-ttu-id="80d38-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d38-124">CommonParameters</span></span>
<span data-ttu-id="80d38-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d38-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d38-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80d38-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d38-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80d38-127">INPUTS</span></span>

### <span data-ttu-id="80d38-128">Brak</span><span class="sxs-lookup"><span data-stu-id="80d38-128">None</span></span>

## <span data-ttu-id="80d38-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80d38-129">OUTPUTS</span></span>

### <span data-ttu-id="80d38-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="80d38-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="80d38-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80d38-131">NOTES</span></span>

## <span data-ttu-id="80d38-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80d38-132">RELATED LINKS</span></span>
