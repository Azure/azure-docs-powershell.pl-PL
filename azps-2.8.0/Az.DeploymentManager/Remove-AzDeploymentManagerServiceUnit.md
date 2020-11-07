---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3ba27cf26ccc555ea79a2b46100bee6be7e3c7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705609"
---
# <span data-ttu-id="19580-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="19580-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="19580-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19580-102">SYNOPSIS</span></span>
<span data-ttu-id="19580-103">Usuwa jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-103">Deletes the service unit.</span></span>

## <span data-ttu-id="19580-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19580-104">SYNTAX</span></span>

### <span data-ttu-id="19580-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="19580-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19580-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="19580-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19580-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="19580-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19580-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="19580-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19580-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="19580-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19580-110">Zasobów</span><span class="sxs-lookup"><span data-stu-id="19580-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19580-111">Inputobject</span><span class="sxs-lookup"><span data-stu-id="19580-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19580-112">Opis</span><span class="sxs-lookup"><span data-stu-id="19580-112">DESCRIPTION</span></span>
<span data-ttu-id="19580-113">Polecenie cmdlet **Remove-AzDeploymentManagerServiceUnit** usuwa jednostkę usługi w usłudze.</span><span class="sxs-lookup"><span data-stu-id="19580-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="19580-114">Określ jednostkę usługi według jej nazwy, usługę, w której została ona zdefiniowana, nazwę topologii usług i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="19580-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="19580-115">Alternatywnie możesz podać obiekt serviceunit lub identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="19580-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="19580-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19580-116">EXAMPLES</span></span>

### <span data-ttu-id="19580-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="19580-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="19580-118">To polecenie usuwa jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19580-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="19580-119">Przykład 2: Usunięcie jednostki usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="19580-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="19580-120">To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19580-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="19580-121">Przykład 3: Usunięcie jednostki usługi za pomocą obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="19580-122">To polecenie usuwa jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i element źródła danych są zgodne z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName w $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="19580-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="19580-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19580-123">PARAMETERS</span></span>

### <span data-ttu-id="19580-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19580-124">-DefaultProfile</span></span>
<span data-ttu-id="19580-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19580-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19580-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="19580-126">-InputObject</span></span>
<span data-ttu-id="19580-127">Obiekt zasobu jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-127">Service unit resource object.</span></span>

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

### <span data-ttu-id="19580-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19580-128">-Name</span></span>
<span data-ttu-id="19580-129">Nazwa jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-129">The name of the service unit.</span></span>

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

### <span data-ttu-id="19580-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19580-130">-PassThru</span></span>
<span data-ttu-id="19580-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="19580-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="19580-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19580-132">-ResourceGroupName</span></span>
<span data-ttu-id="19580-133">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="19580-133">The resource group.</span></span>

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

### <span data-ttu-id="19580-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19580-134">-ResourceId</span></span>
<span data-ttu-id="19580-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="19580-135">The resource identifier.</span></span>

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

### <span data-ttu-id="19580-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="19580-136">-ServiceName</span></span>
<span data-ttu-id="19580-137">Nazwa usługi, do której należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-137">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="19580-138">-Serviceobject</span><span class="sxs-lookup"><span data-stu-id="19580-138">-ServiceObject</span></span>
<span data-ttu-id="19580-139">Obiekt usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-139">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="19580-140">-Serviceresourceid</span><span class="sxs-lookup"><span data-stu-id="19580-140">-ServiceResourceId</span></span>
<span data-ttu-id="19580-141">Identyfikator zasobu usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="19580-142">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="19580-142">-ServiceTopologyName</span></span>
<span data-ttu-id="19580-143">Nazwa topologii usługi, do której należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="19580-144">-Servicetopologyobject</span><span class="sxs-lookup"><span data-stu-id="19580-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="19580-145">Obiekt z topologią usług, w którym należy utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-145">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="19580-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="19580-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="19580-147">Identyfikator zasobu topologii usług, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="19580-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="19580-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19580-148">-Confirm</span></span>
<span data-ttu-id="19580-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19580-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19580-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19580-150">-WhatIf</span></span>
<span data-ttu-id="19580-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19580-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19580-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19580-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19580-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19580-153">CommonParameters</span></span>
<span data-ttu-id="19580-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19580-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19580-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19580-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19580-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19580-156">INPUTS</span></span>

### <span data-ttu-id="19580-157">System. String</span><span class="sxs-lookup"><span data-stu-id="19580-157">System.String</span></span>

### <span data-ttu-id="19580-158">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="19580-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="19580-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19580-159">OUTPUTS</span></span>

### <span data-ttu-id="19580-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19580-160">System.Boolean</span></span>

## <span data-ttu-id="19580-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19580-161">NOTES</span></span>

## <span data-ttu-id="19580-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19580-162">RELATED LINKS</span></span>