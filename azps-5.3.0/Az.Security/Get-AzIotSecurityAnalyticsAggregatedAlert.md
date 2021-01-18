---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503074"
---
# <span data-ttu-id="0af7b-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="0af7b-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="0af7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0af7b-102">SYNOPSIS</span></span>
<span data-ttu-id="0af7b-103">Uzyskaj zbiorczy alert dotyczący zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="0af7b-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="0af7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0af7b-104">SYNTAX</span></span>

### <span data-ttu-id="0af7b-105">SolutionScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0af7b-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0af7b-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="0af7b-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0af7b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0af7b-107">DESCRIPTION</span></span>
<span data-ttu-id="0af7b-108">Polecenie cmdlet Get-AzIotSecurityAnalyticsAggregatedAlert zwraca co najmniej jedno zagregowane ostrzeżenie na urządzeniu Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="0af7b-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="0af7b-109">Nazwa zagregowanych alertów to kombinacja typu alertu i daty aggragted alertu rozdzielonej znakiem "/".</span><span class="sxs-lookup"><span data-stu-id="0af7b-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="0af7b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0af7b-110">EXAMPLES</span></span>

### <span data-ttu-id="0af7b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0af7b-111">Example 1</span></span>
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

<span data-ttu-id="0af7b-112">Uzyskiwanie zagregowanego alertu "IoT_Bruteforce_Fail/2019-02-02" (nazwa połączona z typu alertu i jego zagregowaną datą) w rozwiązaniu "Moje rozwiązanie" i "Grupa zasobów"</span><span class="sxs-lookup"><span data-stu-id="0af7b-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="0af7b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0af7b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="0af7b-114">Wyświetlanie listy wszystkich zagregowanych alertów w rozwiązaniu "Moje rozwiązanie" i Grupa zasobów "Moja zasobów"</span><span class="sxs-lookup"><span data-stu-id="0af7b-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="0af7b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0af7b-115">PARAMETERS</span></span>

### <span data-ttu-id="0af7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af7b-116">-DefaultProfile</span></span>
<span data-ttu-id="0af7b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0af7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0af7b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0af7b-118">-Name</span></span>
<span data-ttu-id="0af7b-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0af7b-119">Resource name.</span></span>

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

### <span data-ttu-id="0af7b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af7b-120">-ResourceGroupName</span></span>
<span data-ttu-id="0af7b-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0af7b-121">Resource group name.</span></span>

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

### <span data-ttu-id="0af7b-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="0af7b-122">-SolutionName</span></span>
<span data-ttu-id="0af7b-123">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="0af7b-123">Solution name</span></span>

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

### <span data-ttu-id="0af7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af7b-124">CommonParameters</span></span>
<span data-ttu-id="0af7b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af7b-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0af7b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af7b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0af7b-127">INPUTS</span></span>

### <span data-ttu-id="0af7b-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0af7b-128">None</span></span>

## <span data-ttu-id="0af7b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0af7b-129">OUTPUTS</span></span>

### <span data-ttu-id="0af7b-130">Microsoft. Azure. Commands. Security. models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="0af7b-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="0af7b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0af7b-131">NOTES</span></span>

## <span data-ttu-id="0af7b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0af7b-132">RELATED LINKS</span></span>
