---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: 4ad5b8a7b4369a5a0dd2b5ccc883ddc561a40af5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200754"
---
# <span data-ttu-id="6696c-101">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="6696c-101">Get-AzCloudServiceInstanceView</span></span>

## <span data-ttu-id="6696c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6696c-102">SYNOPSIS</span></span>
<span data-ttu-id="6696c-103">Pobiera stan usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="6696c-103">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="6696c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6696c-104">SYNTAX</span></span>

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6696c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6696c-105">DESCRIPTION</span></span>
<span data-ttu-id="6696c-106">Pobiera stan usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="6696c-106">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="6696c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6696c-107">EXAMPLES</span></span>

### <span data-ttu-id="6696c-108">Przykład 1. Uzyskiwanie widoku wystąpienia usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="6696c-108">Example 1: Get cloud service instance view</span></span>
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

<span data-ttu-id="6696c-109">To polecenie cmdlet pobiera widok wystąpienia usługi w chmurze o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="6696c-109">This cmdlet gets the instance view of the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="6696c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6696c-110">PARAMETERS</span></span>

### <span data-ttu-id="6696c-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="6696c-111">-CloudServiceName</span></span>
<span data-ttu-id="6696c-112">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="6696c-112">Name of the cloud service.</span></span>

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

### <span data-ttu-id="6696c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6696c-113">-DefaultProfile</span></span>
<span data-ttu-id="6696c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6696c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6696c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6696c-115">-ResourceGroupName</span></span>
<span data-ttu-id="6696c-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6696c-116">Name of the resource group.</span></span>

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

### <span data-ttu-id="6696c-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6696c-117">-SubscriptionId</span></span>
<span data-ttu-id="6696c-118">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6696c-118">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6696c-119">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="6696c-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6696c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6696c-120">CommonParameters</span></span>
<span data-ttu-id="6696c-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6696c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6696c-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6696c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6696c-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6696c-123">INPUTS</span></span>

## <span data-ttu-id="6696c-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6696c-124">OUTPUTS</span></span>

### <span data-ttu-id="6696c-125">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="6696c-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span></span>

## <span data-ttu-id="6696c-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6696c-126">NOTES</span></span>

<span data-ttu-id="6696c-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="6696c-127">ALIASES</span></span>

## <span data-ttu-id="6696c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6696c-128">RELATED LINKS</span></span>

