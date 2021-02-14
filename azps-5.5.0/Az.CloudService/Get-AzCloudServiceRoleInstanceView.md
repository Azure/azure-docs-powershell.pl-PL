---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: a86ebbda321f37a38b3d014377081087f37feb9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181794"
---
# <span data-ttu-id="a63bc-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="a63bc-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="a63bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a63bc-102">SYNOPSIS</span></span>
<span data-ttu-id="a63bc-103">Pobiera informacje o stanie uruchamiania wystąpienia roli w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="a63bc-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="a63bc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a63bc-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a63bc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a63bc-105">DESCRIPTION</span></span>
<span data-ttu-id="a63bc-106">Pobiera informacje o stanie uruchamiania wystąpienia roli w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="a63bc-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="a63bc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a63bc-107">EXAMPLES</span></span>

### <span data-ttu-id="a63bc-108">Przykład 1. Uzyskiwanie szczegółów widoku wystąpienia dla wystąpienia roli usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="a63bc-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="a63bc-109">To polecenie cmdlet pobiera widok wystąpienia roli o nazwie ContosoFrontEnd_IN_0 o nazwie Usługa w chmurze ContosoCS, która należy do grupy zasobów o nazwie ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="a63bc-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="a63bc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a63bc-110">PARAMETERS</span></span>

### <span data-ttu-id="a63bc-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="a63bc-111">-CloudServiceName</span></span>
<span data-ttu-id="a63bc-112">.</span><span class="sxs-lookup"><span data-stu-id="a63bc-112">.</span></span>

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

### <span data-ttu-id="a63bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63bc-113">-DefaultProfile</span></span>
<span data-ttu-id="a63bc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a63bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a63bc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63bc-115">-ResourceGroupName</span></span>
<span data-ttu-id="a63bc-116">.</span><span class="sxs-lookup"><span data-stu-id="a63bc-116">.</span></span>

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

### <span data-ttu-id="a63bc-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="a63bc-117">-RoleInstanceName</span></span>
<span data-ttu-id="a63bc-118">Nazwa wystąpienia roli.</span><span class="sxs-lookup"><span data-stu-id="a63bc-118">Name of the role instance.</span></span>

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

### <span data-ttu-id="a63bc-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a63bc-119">-SubscriptionId</span></span>
<span data-ttu-id="a63bc-120">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a63bc-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a63bc-121">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="a63bc-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a63bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63bc-122">CommonParameters</span></span>
<span data-ttu-id="a63bc-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a63bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63bc-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a63bc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63bc-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a63bc-125">INPUTS</span></span>

## <span data-ttu-id="a63bc-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a63bc-126">OUTPUTS</span></span>

### <span data-ttu-id="a63bc-127">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="a63bc-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="a63bc-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a63bc-128">NOTES</span></span>

<span data-ttu-id="a63bc-129">ALIASY</span><span class="sxs-lookup"><span data-stu-id="a63bc-129">ALIASES</span></span>

## <span data-ttu-id="a63bc-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a63bc-130">RELATED LINKS</span></span>

