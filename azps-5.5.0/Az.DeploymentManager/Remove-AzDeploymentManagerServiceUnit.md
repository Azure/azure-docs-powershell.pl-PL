---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: d4248a13282824c60e698b2257b3e38a78ce3a6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238080"
---
# <span data-ttu-id="a4f68-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a4f68-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="a4f68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4f68-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f68-103">Usuwa jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-103">Deletes the service unit.</span></span>

## <span data-ttu-id="a4f68-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4f68-104">SYNTAX</span></span>

### <span data-ttu-id="a4f68-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a4f68-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f68-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a4f68-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f68-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a4f68-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f68-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="a4f68-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f68-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a4f68-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f68-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4f68-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f68-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="a4f68-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f68-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4f68-112">DESCRIPTION</span></span>
<span data-ttu-id="a4f68-113">Polecenie **cmdlet Remove-AzDeploymentManagerServiceUnit** usuwa jednostkę usługi w usłudze.</span><span class="sxs-lookup"><span data-stu-id="a4f68-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="a4f68-114">Określ jednostkę usługi według jej nazwy, usługi, w ramach której została zdefiniowana, nazwy topologii usługi i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4f68-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="a4f68-115">Ewentualnie możesz podać obiekt ServiceUnit lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a4f68-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="a4f68-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4f68-116">EXAMPLES</span></span>

### <span data-ttu-id="a4f68-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4f68-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="a4f68-118">To polecenie usuwa jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a4f68-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a4f68-119">Przykład 2. Usuwanie jednostki usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="a4f68-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="a4f68-120">To polecenie pobiera jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a4f68-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a4f68-121">Przykład 3. Usuwanie jednostki usługi przy użyciu obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="a4f68-122">To polecenie usuwa jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa Usługi), ServiceTopologyName (Nazwa_usługi) i ResourceGroupName (Nazwa Grupy Zasobów) $serviceUnitObject grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4f68-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="a4f68-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4f68-123">PARAMETERS</span></span>

### <span data-ttu-id="a4f68-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f68-124">-DefaultProfile</span></span>
<span data-ttu-id="a4f68-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f68-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4f68-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4f68-126">-InputObject</span></span>
<span data-ttu-id="a4f68-127">Obiekt zasobu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-127">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f68-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a4f68-128">-Name</span></span>
<span data-ttu-id="a4f68-129">Nazwa jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f68-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4f68-130">-PassThru</span></span>
<span data-ttu-id="a4f68-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a4f68-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a4f68-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f68-132">-ResourceGroupName</span></span>
<span data-ttu-id="a4f68-133">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4f68-133">The resource group.</span></span>

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

### <span data-ttu-id="a4f68-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4f68-134">-ResourceId</span></span>
<span data-ttu-id="a4f68-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a4f68-135">The resource identifier.</span></span>

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

### <span data-ttu-id="a4f68-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a4f68-136">-ServiceName</span></span>
<span data-ttu-id="a4f68-137">Nazwa usługi, do których należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-137">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f68-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="a4f68-138">-ServiceObject</span></span>
<span data-ttu-id="a4f68-139">Obiekt usługi, w którym powinna zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-139">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f68-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a4f68-140">-ServiceResourceId</span></span>
<span data-ttu-id="a4f68-141">Identyfikator zasobu usługi, w którym powinna zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-141">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f68-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="a4f68-142">-ServiceTopologyName</span></span>
<span data-ttu-id="a4f68-143">Nazwa topologii usługi, do których należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="a4f68-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="a4f68-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="a4f68-145">Obiekt topologii usługi, w którym powinna zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-145">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f68-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="a4f68-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="a4f68-147">Identyfikator zasobu topologii usługi, w którym powinna zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a4f68-147">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f68-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4f68-148">-Confirm</span></span>
<span data-ttu-id="a4f68-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4f68-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f68-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f68-150">-WhatIf</span></span>
<span data-ttu-id="a4f68-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4f68-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f68-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a4f68-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f68-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f68-153">CommonParameters</span></span>
<span data-ttu-id="a4f68-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4f68-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f68-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4f68-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f68-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4f68-156">INPUTS</span></span>

### <span data-ttu-id="a4f68-157">System.String</span><span class="sxs-lookup"><span data-stu-id="a4f68-157">System.String</span></span>

### <span data-ttu-id="a4f68-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="a4f68-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="a4f68-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4f68-159">OUTPUTS</span></span>

### <span data-ttu-id="a4f68-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4f68-160">System.Boolean</span></span>

## <span data-ttu-id="a4f68-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4f68-161">NOTES</span></span>

## <span data-ttu-id="a4f68-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4f68-162">RELATED LINKS</span></span>
