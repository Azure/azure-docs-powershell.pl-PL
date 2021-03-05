---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: 3d3d8e5cd7855e03d5f02ddaee6b38c98aeacb0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008065"
---
# <span data-ttu-id="9585f-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="9585f-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="9585f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9585f-102">SYNOPSIS</span></span>
<span data-ttu-id="9585f-103">Pobiera informacje o stanie uruchamiania wystąpienia roli w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="9585f-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="9585f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9585f-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9585f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9585f-105">DESCRIPTION</span></span>
<span data-ttu-id="9585f-106">Pobiera informacje o stanie uruchamiania wystąpienia roli w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="9585f-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="9585f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9585f-107">EXAMPLES</span></span>

### <span data-ttu-id="9585f-108">Przykład 1. Uzyskiwanie szczegółów widoku wystąpienia dla wystąpienia roli usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="9585f-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="9585f-109">To polecenie cmdlet pobiera widok wystąpienia roli o nazwie ContosoFrontEnd_IN_0 o nazwie ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="9585f-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="9585f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9585f-110">PARAMETERS</span></span>

### <span data-ttu-id="9585f-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="9585f-111">-CloudServiceName</span></span>
<span data-ttu-id="9585f-112">.</span><span class="sxs-lookup"><span data-stu-id="9585f-112">.</span></span>

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

### <span data-ttu-id="9585f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9585f-113">-DefaultProfile</span></span>
<span data-ttu-id="9585f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9585f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9585f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9585f-115">-ResourceGroupName</span></span>
<span data-ttu-id="9585f-116">.</span><span class="sxs-lookup"><span data-stu-id="9585f-116">.</span></span>

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

### <span data-ttu-id="9585f-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="9585f-117">-RoleInstanceName</span></span>
<span data-ttu-id="9585f-118">Nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="9585f-118">Name of the role instance.</span></span>

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

### <span data-ttu-id="9585f-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9585f-119">-SubscriptionId</span></span>
<span data-ttu-id="9585f-120">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9585f-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9585f-121">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="9585f-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9585f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9585f-122">CommonParameters</span></span>
<span data-ttu-id="9585f-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9585f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9585f-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9585f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9585f-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9585f-125">INPUTS</span></span>

## <span data-ttu-id="9585f-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9585f-126">OUTPUTS</span></span>

### <span data-ttu-id="9585f-127">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="9585f-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="9585f-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9585f-128">NOTES</span></span>

<span data-ttu-id="9585f-129">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9585f-129">ALIASES</span></span>

## <span data-ttu-id="9585f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9585f-130">RELATED LINKS</span></span>

