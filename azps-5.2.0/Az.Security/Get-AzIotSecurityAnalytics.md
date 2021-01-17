---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337441"
---
# <span data-ttu-id="21570-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="21570-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="21570-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21570-102">SYNOPSIS</span></span>
<span data-ttu-id="21570-103">Uzyskaj analiza zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="21570-103">Get IoT security analytics</span></span>

## <span data-ttu-id="21570-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21570-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21570-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21570-105">DESCRIPTION</span></span>
<span data-ttu-id="21570-106">Polecenie cmdlet Get-AzIotSecurityAnalytics zwraca zestaw funkcji analizy zabezpieczeń konkretnego rozwiązania dotyczącego zabezpieczeń IoT</span><span class="sxs-lookup"><span data-stu-id="21570-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="21570-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21570-107">EXAMPLES</span></span>

### <span data-ttu-id="21570-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21570-108">Example 1</span></span>
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

<span data-ttu-id="21570-109">Pobierz deafult internetowa analiza bezpieczeństwa dla rozwiązania zabezpieczeń "Moje rozwiązanie" w grupie reasource "Moja zasobów"</span><span class="sxs-lookup"><span data-stu-id="21570-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="21570-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21570-110">PARAMETERS</span></span>

### <span data-ttu-id="21570-111">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="21570-111">-Default</span></span>
<span data-ttu-id="21570-112">Jeśli jest obecny, Pobierz domyślny zestaw analiz, w przeciwnym razie Pobierz listę wszystkich zestawów analiz.</span><span class="sxs-lookup"><span data-stu-id="21570-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

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

### <span data-ttu-id="21570-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21570-113">-DefaultProfile</span></span>
<span data-ttu-id="21570-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21570-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21570-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21570-115">-ResourceGroupName</span></span>
<span data-ttu-id="21570-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21570-116">Resource group name.</span></span>

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

### <span data-ttu-id="21570-117">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="21570-117">-SolutionName</span></span>
<span data-ttu-id="21570-118">Nazwa rozwiązania</span><span class="sxs-lookup"><span data-stu-id="21570-118">Solution name</span></span>

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

### <span data-ttu-id="21570-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21570-119">CommonParameters</span></span>
<span data-ttu-id="21570-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21570-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21570-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21570-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21570-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21570-122">INPUTS</span></span>

### <span data-ttu-id="21570-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="21570-123">None</span></span>

## <span data-ttu-id="21570-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21570-124">OUTPUTS</span></span>

### <span data-ttu-id="21570-125">Microsoft. Azure. Commands. Security. models. IotSecuritySolutionAnalytics. PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="21570-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="21570-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21570-126">NOTES</span></span>

## <span data-ttu-id="21570-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21570-127">RELATED LINKS</span></span>
