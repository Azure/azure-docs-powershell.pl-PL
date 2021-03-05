---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: d3716d18bc883d5407ee4acf3fa43960b63e7cd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980682"
---
# <span data-ttu-id="84b67-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="84b67-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="84b67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84b67-102">SYNOPSIS</span></span>
<span data-ttu-id="84b67-103">Usuwa topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="84b67-103">Deletes the service topology.</span></span> <span data-ttu-id="84b67-104">Wszystkie usługi utworzone w topologii usługi muszą zostać usunięte przed usunięciem topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="84b67-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="84b67-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84b67-105">SYNTAX</span></span>

### <span data-ttu-id="84b67-106">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="84b67-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b67-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="84b67-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b67-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="84b67-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b67-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="84b67-109">DESCRIPTION</span></span>
<span data-ttu-id="84b67-110">Polecenie **cmdlet Remove-AzDeploymentManagerServiceTopology** usuwa topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="84b67-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="84b67-111">Określanie topologii usługi według jej nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84b67-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="84b67-112">Można też udostępnić obiekt ServiceTopology lub identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="84b67-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="84b67-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84b67-113">EXAMPLES</span></span>

### <span data-ttu-id="84b67-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84b67-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="84b67-115">To polecenie usuwa topologię usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="84b67-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="84b67-116">Przykład 2. Usuwanie topologii usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="84b67-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="84b67-117">To polecenie usuwa topologię usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="84b67-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="84b67-118">Przykład 3. Usuwanie topologii usługi przy użyciu obiektu topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="84b67-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="84b67-119">To polecenie usuwa topologię usługi, której nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Nazwa i NazwaGrupy Zasobów $serviceTopologyObject grupy.</span><span class="sxs-lookup"><span data-stu-id="84b67-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="84b67-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84b67-120">PARAMETERS</span></span>

### <span data-ttu-id="84b67-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b67-121">-DefaultProfile</span></span>
<span data-ttu-id="84b67-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="84b67-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84b67-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84b67-123">-InputObject</span></span>
<span data-ttu-id="84b67-124">Zasób do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="84b67-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="84b67-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="84b67-125">-Name</span></span>
<span data-ttu-id="84b67-126">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="84b67-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b67-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84b67-127">-PassThru</span></span>
<span data-ttu-id="84b67-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="84b67-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="84b67-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b67-129">-ResourceGroupName</span></span>
<span data-ttu-id="84b67-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="84b67-130">The resource group.</span></span>

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

### <span data-ttu-id="84b67-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84b67-131">-ResourceId</span></span>
<span data-ttu-id="84b67-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="84b67-132">The resource identifier.</span></span>

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

### <span data-ttu-id="84b67-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84b67-133">-Confirm</span></span>
<span data-ttu-id="84b67-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84b67-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b67-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b67-135">-WhatIf</span></span>
<span data-ttu-id="84b67-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b67-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b67-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="84b67-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b67-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b67-138">CommonParameters</span></span>
<span data-ttu-id="84b67-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b67-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b67-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84b67-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b67-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84b67-141">INPUTS</span></span>

### <span data-ttu-id="84b67-142">System.String</span><span class="sxs-lookup"><span data-stu-id="84b67-142">System.String</span></span>

### <span data-ttu-id="84b67-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="84b67-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="84b67-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84b67-144">OUTPUTS</span></span>

### <span data-ttu-id="84b67-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="84b67-145">System.Boolean</span></span>

## <span data-ttu-id="84b67-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84b67-146">NOTES</span></span>

## <span data-ttu-id="84b67-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84b67-147">RELATED LINKS</span></span>
