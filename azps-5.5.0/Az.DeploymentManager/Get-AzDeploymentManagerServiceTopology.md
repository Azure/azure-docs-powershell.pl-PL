---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177003"
---
# <span data-ttu-id="fe926-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="fe926-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="fe926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe926-102">SYNOPSIS</span></span>
<span data-ttu-id="fe926-103">Pobiera topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="fe926-103">Gets the service topology.</span></span>

## <span data-ttu-id="fe926-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe926-104">SYNTAX</span></span>

### <span data-ttu-id="fe926-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fe926-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe926-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe926-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe926-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe926-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe926-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe926-108">DESCRIPTION</span></span>
<span data-ttu-id="fe926-109">Polecenie **cmdlet Get-AzDeploymentManagerServiceTopology** uzyskuje topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="fe926-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="fe926-110">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do topologii za pomocą Set-AzDeploymentManagerServiceTopology cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe926-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="fe926-111">Określanie topologii usługi według jej nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe926-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="fe926-112">Ewentualnie można udostępnić obiekt ServiceTopology lub identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="fe926-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="fe926-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe926-113">EXAMPLES</span></span>

### <span data-ttu-id="fe926-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe926-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="fe926-115">To polecenie pobiera topologię usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe926-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fe926-116">Przykład 2. Uzyskiwanie topologii usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="fe926-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="fe926-117">To polecenie pobiera topologię usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fe926-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fe926-118">Przykład 3. Uzyskiwanie topologii usługi przy użyciu obiektu topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="fe926-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="fe926-119">To polecenie pobiera topologię usługi, której nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $serviceTopologyObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="fe926-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="fe926-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe926-120">PARAMETERS</span></span>

### <span data-ttu-id="fe926-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe926-121">-DefaultProfile</span></span>
<span data-ttu-id="fe926-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe926-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe926-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe926-123">-InputObject</span></span>
<span data-ttu-id="fe926-124">Obiekt zasobu topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="fe926-124">Service topology resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe926-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe926-125">-Name</span></span>
<span data-ttu-id="fe926-126">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="fe926-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe926-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe926-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe926-128">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe926-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe926-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe926-129">-ResourceId</span></span>
<span data-ttu-id="fe926-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="fe926-130">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe926-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe926-131">CommonParameters</span></span>
<span data-ttu-id="fe926-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe926-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe926-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe926-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe926-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe926-134">INPUTS</span></span>

### <span data-ttu-id="fe926-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fe926-135">System.String</span></span>

### <span data-ttu-id="fe926-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fe926-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fe926-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe926-137">OUTPUTS</span></span>

### <span data-ttu-id="fe926-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fe926-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fe926-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe926-139">NOTES</span></span>

## <span data-ttu-id="fe926-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe926-140">RELATED LINKS</span></span>
