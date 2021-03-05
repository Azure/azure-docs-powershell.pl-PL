---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: cb077b2bdc6c91ccb3dc1c9099490c1d8bf6bea6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012698"
---
# <span data-ttu-id="d52fe-101">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="d52fe-101">Get-AzCloudServiceInstanceView</span></span>

## <span data-ttu-id="d52fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d52fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d52fe-103">Pobiera stan usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d52fe-103">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="d52fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d52fe-104">SYNTAX</span></span>

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d52fe-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d52fe-105">DESCRIPTION</span></span>
<span data-ttu-id="d52fe-106">Pobiera stan usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d52fe-106">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="d52fe-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d52fe-107">EXAMPLES</span></span>

### <span data-ttu-id="d52fe-108">Przykład 1. Uzyskiwanie widoku wystąpienia usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="d52fe-108">Example 1: Get cloud service instance view</span></span>
```powershell
PS C:\>$cloudServiceInstanceView = Get-AzCloudServiceInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

PS C:\>$cloudServiceInstanceView
RoleInstanceStatusesSummary                                   Statuses
---------------------------                                   --------
{{ProvisioningState/succeeded : 4}, {PowerState/started : 4}} {Provisioning succeeded, Started, Current Upgrade Domain of cloud service is -1., Max Upgrade Domain of cloud service is 1.}

PS C:\>$cloudServiceInstanceView.ToJsonString()
{
  "roleInstance": {
    "statusesSummary": [
      {
        "code": "ProvisioningState/succeeded",
        "count": 4
      },
      {
        "code": "PowerState/started",
        "count": 4
      }
    ]
  },
  "statuses": [
    {
      "code": "ProvisioningState/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "PowerState/started",
      "displayStatus": "Started",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "CurrentUpgradeDomain/-1",
      "displayStatus": "Current Upgrade Domain of cloud service is -1.",
      "level": "Info"
    },
    {
      "code": "MaxUpgradeDomain/1",
      "displayStatus": "Max Upgrade Domain of cloud service is 1.",
      "level": "Info"
    }
  ]
}
```

<span data-ttu-id="d52fe-109">To polecenie cmdlet pobiera widok wystąpienia usługi w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="d52fe-109">This cmdlet gets the instance view of the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="d52fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d52fe-110">PARAMETERS</span></span>

### <span data-ttu-id="d52fe-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="d52fe-111">-CloudServiceName</span></span>
<span data-ttu-id="d52fe-112">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="d52fe-112">Name of the cloud service.</span></span>

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

### <span data-ttu-id="d52fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d52fe-113">-DefaultProfile</span></span>
<span data-ttu-id="d52fe-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d52fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d52fe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d52fe-115">-ResourceGroupName</span></span>
<span data-ttu-id="d52fe-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d52fe-116">Name of the resource group.</span></span>

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

### <span data-ttu-id="d52fe-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d52fe-117">-SubscriptionId</span></span>
<span data-ttu-id="d52fe-118">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d52fe-118">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d52fe-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d52fe-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d52fe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d52fe-120">CommonParameters</span></span>
<span data-ttu-id="d52fe-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d52fe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d52fe-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d52fe-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d52fe-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d52fe-123">INPUTS</span></span>

## <span data-ttu-id="d52fe-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d52fe-124">OUTPUTS</span></span>

### <span data-ttu-id="d52fe-125">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="d52fe-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span></span>

## <span data-ttu-id="d52fe-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d52fe-126">NOTES</span></span>

<span data-ttu-id="d52fe-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d52fe-127">ALIASES</span></span>

## <span data-ttu-id="d52fe-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d52fe-128">RELATED LINKS</span></span>

