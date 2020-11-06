---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: 993b250b0c49efc448c0198c4e9a3aea29f77714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523854"
---
# <span data-ttu-id="0d25e-101">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="0d25e-101">Remove-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="0d25e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d25e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d25e-103">Usuwa jednostkę usługi usługi w topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="0d25e-103">Deletes the service unit of a service in a service topology.</span></span>

## <span data-ttu-id="0d25e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d25e-104">SYNTAX</span></span>

### <span data-ttu-id="0d25e-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="0d25e-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d25e-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="0d25e-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d25e-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="0d25e-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d25e-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="0d25e-108">ByServiceObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d25e-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="0d25e-109">ByServiceResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d25e-110">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0d25e-110">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d25e-111">Inputobject</span><span class="sxs-lookup"><span data-stu-id="0d25e-111">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d25e-112">Opis</span><span class="sxs-lookup"><span data-stu-id="0d25e-112">DESCRIPTION</span></span>
<span data-ttu-id="0d25e-113">Polecenie cmdlet **Remove-AzureRmDeploymentManagerServiceUnit** usuwa jednostkę usługi w usłudze.</span><span class="sxs-lookup"><span data-stu-id="0d25e-113">The **Remove-AzureRmDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="0d25e-114">Określ jednostkę usługi według jej nazwy, usługę, w której została ona zdefiniowana, nazwę topologii usług i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d25e-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="0d25e-115">Alternatywnie możesz podać obiekt serviceunit lub identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0d25e-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="0d25e-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d25e-116">EXAMPLES</span></span>

### <span data-ttu-id="0d25e-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d25e-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="0d25e-118">To polecenie usuwa jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0d25e-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0d25e-119">Przykład 2: Usunięcie jednostki usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="0d25e-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="0d25e-120">To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0d25e-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0d25e-121">Przykład 3: Usunięcie jednostki usługi za pomocą obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="0d25e-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="0d25e-122">To polecenie usuwa jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i element źródła danych są zgodne z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName w $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="0d25e-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="0d25e-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d25e-123">PARAMETERS</span></span>

### <span data-ttu-id="0d25e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d25e-124">-DefaultProfile</span></span>
<span data-ttu-id="0d25e-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d25e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d25e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="0d25e-126">-Force</span></span>
<span data-ttu-id="0d25e-127">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0d25e-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0d25e-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d25e-128">-Name</span></span>
<span data-ttu-id="0d25e-129">Nazwa jednostki usługi, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="0d25e-129">The name of the service unit to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d25e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d25e-130">-PassThru</span></span>
<span data-ttu-id="0d25e-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0d25e-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0d25e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d25e-132">-ResourceGroupName</span></span>
<span data-ttu-id="0d25e-133">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d25e-133">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d25e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d25e-134">-ResourceId</span></span>
<span data-ttu-id="0d25e-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0d25e-135">The resource identifier.</span></span>

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

### <span data-ttu-id="0d25e-136">-Service</span><span class="sxs-lookup"><span data-stu-id="0d25e-136">-Service</span></span>
<span data-ttu-id="0d25e-137">Obiekt usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="0d25e-137">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="0d25e-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0d25e-138">-ServiceName</span></span>
<span data-ttu-id="0d25e-139">Nazwa usługi, do której należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="0d25e-139">The name of the service the service unit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d25e-140">-Serviceresourceid</span><span class="sxs-lookup"><span data-stu-id="0d25e-140">-ServiceResourceId</span></span>
<span data-ttu-id="0d25e-141">Identyfikator zasobu usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="0d25e-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="0d25e-142">-Servicetopology</span><span class="sxs-lookup"><span data-stu-id="0d25e-142">-ServiceTopology</span></span>
<span data-ttu-id="0d25e-143">Obiekt z topologią usług, w którym należy utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="0d25e-143">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="0d25e-144">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="0d25e-144">-ServiceTopologyName</span></span>
<span data-ttu-id="0d25e-145">Nazwa topologii usługi, do której należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="0d25e-145">The name of the service topology the service unit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d25e-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="0d25e-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="0d25e-147">Identyfikator zasobu topologii usług, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="0d25e-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="0d25e-148">-Serviceunit</span><span class="sxs-lookup"><span data-stu-id="0d25e-148">-ServiceUnit</span></span>
<span data-ttu-id="0d25e-149">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="0d25e-149">The resource to be removed.</span></span>

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

### <span data-ttu-id="0d25e-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d25e-150">-Confirm</span></span>
<span data-ttu-id="0d25e-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d25e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d25e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d25e-152">-WhatIf</span></span>
<span data-ttu-id="0d25e-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d25e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d25e-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d25e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d25e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d25e-155">CommonParameters</span></span>
<span data-ttu-id="0d25e-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d25e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d25e-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d25e-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d25e-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d25e-158">INPUTS</span></span>

### <span data-ttu-id="0d25e-159">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="0d25e-159">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="0d25e-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d25e-160">OUTPUTS</span></span>

### <span data-ttu-id="0d25e-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d25e-161">System.Boolean</span></span>

## <span data-ttu-id="0d25e-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d25e-162">NOTES</span></span>

## <span data-ttu-id="0d25e-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d25e-163">RELATED LINKS</span></span>

[<span data-ttu-id="0d25e-164">Nowe — AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="0d25e-164">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="0d25e-165">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="0d25e-165">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="0d25e-166">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="0d25e-166">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)