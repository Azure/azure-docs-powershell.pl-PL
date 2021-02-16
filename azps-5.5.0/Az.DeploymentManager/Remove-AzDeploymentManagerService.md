---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238099"
---
# <span data-ttu-id="520ba-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="520ba-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="520ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="520ba-102">SYNOPSIS</span></span>
<span data-ttu-id="520ba-103">Usuwa usługę.</span><span class="sxs-lookup"><span data-stu-id="520ba-103">Deletes the service..</span></span> <span data-ttu-id="520ba-104">Wszystkie jednostki usługi utworzone w ramach usługi muszą zostać usunięte przed usunięciem usługi.</span><span class="sxs-lookup"><span data-stu-id="520ba-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="520ba-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="520ba-105">SYNTAX</span></span>

### <span data-ttu-id="520ba-106">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="520ba-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="520ba-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="520ba-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="520ba-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="520ba-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="520ba-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="520ba-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="520ba-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="520ba-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="520ba-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="520ba-111">DESCRIPTION</span></span>
<span data-ttu-id="520ba-112">Polecenie **cmdlet Remove-AzDeploymentManagerService** usuwa usługę w topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="520ba-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="520ba-113">Określ usługę według jej nazwy, topologii usługi oraz nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="520ba-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="520ba-114">Ewentualnie możesz podać obiekt Service lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="520ba-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="520ba-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="520ba-115">EXAMPLES</span></span>

### <span data-ttu-id="520ba-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="520ba-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="520ba-117">To polecenie usuwa usługę o nazwie ContosoService1 w topologii usługi ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="520ba-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="520ba-118">Przykład 2. Usuwanie usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="520ba-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="520ba-119">To polecenie usuwa usługę o nazwie ContosoService1 w topologii usługi ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="520ba-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="520ba-120">Przykład 3. Usuwanie usługi przy użyciu obiektu usługi.</span><span class="sxs-lookup"><span data-stu-id="520ba-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="520ba-121">To polecenie usuwa usługę, której nazwa, nazwa topologii usługi i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa_usługi) i NazwaGrupy Zasobów $serviceObject Grupy Zasobów.</span><span class="sxs-lookup"><span data-stu-id="520ba-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="520ba-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="520ba-122">PARAMETERS</span></span>

### <span data-ttu-id="520ba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520ba-123">-DefaultProfile</span></span>
<span data-ttu-id="520ba-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="520ba-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="520ba-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="520ba-125">-InputObject</span></span>
<span data-ttu-id="520ba-126">Obiekt Service.</span><span class="sxs-lookup"><span data-stu-id="520ba-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="520ba-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="520ba-127">-Name</span></span>
<span data-ttu-id="520ba-128">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="520ba-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520ba-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="520ba-129">-PassThru</span></span>
<span data-ttu-id="520ba-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="520ba-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="520ba-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="520ba-131">-ResourceGroupName</span></span>
<span data-ttu-id="520ba-132">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="520ba-132">The resource group.</span></span>

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

### <span data-ttu-id="520ba-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="520ba-133">-ResourceId</span></span>
<span data-ttu-id="520ba-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="520ba-134">The resource identifier.</span></span>

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

### <span data-ttu-id="520ba-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="520ba-135">-ServiceTopologyName</span></span>
<span data-ttu-id="520ba-136">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="520ba-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="520ba-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="520ba-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="520ba-138">Obiekt topologii usługi, w którym powinna zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="520ba-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520ba-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="520ba-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="520ba-140">Identyfikator zasobu topologii usługi, w którym powinna zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="520ba-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520ba-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="520ba-141">-Confirm</span></span>
<span data-ttu-id="520ba-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="520ba-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="520ba-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="520ba-143">-WhatIf</span></span>
<span data-ttu-id="520ba-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="520ba-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="520ba-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="520ba-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="520ba-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520ba-146">CommonParameters</span></span>
<span data-ttu-id="520ba-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="520ba-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520ba-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="520ba-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520ba-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="520ba-149">INPUTS</span></span>

### <span data-ttu-id="520ba-150">System.String</span><span class="sxs-lookup"><span data-stu-id="520ba-150">System.String</span></span>

### <span data-ttu-id="520ba-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="520ba-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="520ba-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="520ba-152">OUTPUTS</span></span>

### <span data-ttu-id="520ba-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="520ba-153">System.Boolean</span></span>

## <span data-ttu-id="520ba-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="520ba-154">NOTES</span></span>

## <span data-ttu-id="520ba-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="520ba-155">RELATED LINKS</span></span>
