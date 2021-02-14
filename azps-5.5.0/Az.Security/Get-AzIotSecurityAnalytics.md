---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176354"
---
# <span data-ttu-id="c0ea2-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="c0ea2-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="c0ea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ea2-103">Uzyskiwanie analizy zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="c0ea2-103">Get IoT security analytics</span></span>

## <span data-ttu-id="c0ea2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0ea2-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0ea2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0ea2-105">DESCRIPTION</span></span>
<span data-ttu-id="c0ea2-106">Polecenie Get-AzIotSecurityAnalytics cmdlet zwraca zestaw analizy zabezpieczeń określonego rozwiązania zabezpieczeń iot.</span><span class="sxs-lookup"><span data-stu-id="c0ea2-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="c0ea2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0ea2-107">EXAMPLES</span></span>

### <span data-ttu-id="c0ea2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0ea2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalytics -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Default

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default"
Name: "default"
Type: "Microsoft.Security/IoTSecuritySolutionAnalyticsModel"
Metrics: {
            High": 5
            Medium: 200
            Low: 102
          }
UnhealthyDeviceCount: 1200
DevicesMetrics: [
            {
              Date: "2019-02-01T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 15
                Low: 70
              }
            }
            {
              Date: "2019-02-02T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 45
                Low: 65
              }
            }
          ]
TopAlertedDevices: [
            {
              DeviceId: "id1"
              AlertsCount: 200
            }
            {
              DeviceId": "id2"
              AlertsCount": 170
            }
            {
              DeviceId": "id3"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceAlerts: [
            {
              AlertDisplayName: "Custom Alert - number of device to cloud messages in AMQP protocol is not in the allowed range"
              ReportedSeverity: "Low"
              AlertsCount: 200
            }
            {
              AlertDisplayName: "Custom Alert - execution of a process that is not allowed"
              ReportedSeverity: "Medium"
              AlertsCount: 170
            }
            {
              AlertDisplayName": "Successful Bruteforce"
              ReportedSeverity": "Low"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceRecommendations: [
            {
              RecommendationDisplayName: "Install the Azure Security of Things Agent"
              ReportedSeverity: "Low"
              DevicesCount: 200
            }
            {
              RecommendationDisplayName: "High level permissions configured in Edge model twin for Edge module"
              ReportedSeverity: "Low"
              DevicesCount: 170
            }
            {
              RrecommendationDisplayName: "Same Authentication Credentials used by multiple devices"
              ReportedSeverity: "Medium"
              DevicesCount: 150
            }
          ]
        }
      }
```

<span data-ttu-id="c0ea2-109">Uzyskaj niesłyszące analizy zabezpieczeń IoT dla rozwiązania zabezpieczeń "MySolution" w grupie ponownego źródła "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="c0ea2-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="c0ea2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0ea2-110">PARAMETERS</span></span>

### <span data-ttu-id="c0ea2-111">— Domyślne</span><span class="sxs-lookup"><span data-stu-id="c0ea2-111">-Default</span></span>
<span data-ttu-id="c0ea2-112">Jeśli są obecne, uzyskaj domyślny zestaw analiz, a w przeciwnym razie uzyskaj listę wszystkich zestawów analiz.</span><span class="sxs-lookup"><span data-stu-id="c0ea2-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ea2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ea2-113">-DefaultProfile</span></span>
<span data-ttu-id="c0ea2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ea2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ea2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ea2-115">-ResourceGroupName</span></span>
<span data-ttu-id="c0ea2-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0ea2-116">Resource group name.</span></span>

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

### <span data-ttu-id="c0ea2-117">—SolutionName</span><span class="sxs-lookup"><span data-stu-id="c0ea2-117">-SolutionName</span></span>
<span data-ttu-id="c0ea2-118">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="c0ea2-118">Solution name</span></span>

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

### <span data-ttu-id="c0ea2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ea2-119">CommonParameters</span></span>
<span data-ttu-id="c0ea2-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0ea2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ea2-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0ea2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ea2-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0ea2-122">INPUTS</span></span>

### <span data-ttu-id="c0ea2-123">Brak</span><span class="sxs-lookup"><span data-stu-id="c0ea2-123">None</span></span>

## <span data-ttu-id="c0ea2-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0ea2-124">OUTPUTS</span></span>

### <span data-ttu-id="c0ea2-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="c0ea2-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="c0ea2-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0ea2-126">NOTES</span></span>

## <span data-ttu-id="c0ea2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0ea2-127">RELATED LINKS</span></span>
