---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387359"
---
# <span data-ttu-id="2232c-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="2232c-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="2232c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2232c-102">SYNOPSIS</span></span>
<span data-ttu-id="2232c-103">Usuwa usługę...</span><span class="sxs-lookup"><span data-stu-id="2232c-103">Deletes the service..</span></span> <span data-ttu-id="2232c-104">Przed usunięciem usługi należy usunąć wszystkie jednostki usług utworzone w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="2232c-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="2232c-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2232c-105">SYNTAX</span></span>

### <span data-ttu-id="2232c-106">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2232c-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2232c-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="2232c-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2232c-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="2232c-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2232c-109">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2232c-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2232c-110">Inputobject</span><span class="sxs-lookup"><span data-stu-id="2232c-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2232c-111">Opis</span><span class="sxs-lookup"><span data-stu-id="2232c-111">DESCRIPTION</span></span>
<span data-ttu-id="2232c-112">Polecenie cmdlet **Remove-AzDeploymentManagerService** usuwa usługę w ramach topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="2232c-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="2232c-113">Określ usługę za pomocą jej nazwy, topologii usługi i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2232c-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="2232c-114">Alternatywnie możesz podać obiekt Service lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2232c-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="2232c-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2232c-115">EXAMPLES</span></span>

### <span data-ttu-id="2232c-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2232c-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="2232c-117">To polecenie usuwa usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2232c-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2232c-118">Przykład 2: Usunięcie usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="2232c-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="2232c-119">To polecenie usuwa usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2232c-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2232c-120">Przykład 3: Usuwanie usługi za pomocą obiektu usługi.</span><span class="sxs-lookup"><span data-stu-id="2232c-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="2232c-121">To polecenie usuwa usługę, której nazwa, nazwa topologii usługi i nazwa źródła zasobów są zgodne z właściwościami Name, servicetopologyname i ResourceGroupName w $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="2232c-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="2232c-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2232c-122">PARAMETERS</span></span>

### <span data-ttu-id="2232c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2232c-123">-DefaultProfile</span></span>
<span data-ttu-id="2232c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2232c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2232c-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2232c-125">-InputObject</span></span>
<span data-ttu-id="2232c-126">Obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="2232c-126">Service object.</span></span>

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

### <span data-ttu-id="2232c-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2232c-127">-Name</span></span>
<span data-ttu-id="2232c-128">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="2232c-128">The name of the service.</span></span>

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

### <span data-ttu-id="2232c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2232c-129">-PassThru</span></span>
<span data-ttu-id="2232c-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2232c-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2232c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2232c-131">-ResourceGroupName</span></span>
<span data-ttu-id="2232c-132">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="2232c-132">The resource group.</span></span>

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

### <span data-ttu-id="2232c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2232c-133">-ResourceId</span></span>
<span data-ttu-id="2232c-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2232c-134">The resource identifier.</span></span>

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

### <span data-ttu-id="2232c-135">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="2232c-135">-ServiceTopologyName</span></span>
<span data-ttu-id="2232c-136">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="2232c-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="2232c-137">-Servicetopologyobject</span><span class="sxs-lookup"><span data-stu-id="2232c-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="2232c-138">Obiekt z topologią usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="2232c-138">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="2232c-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="2232c-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="2232c-140">Identyfikator zasobu topologii usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="2232c-140">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="2232c-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2232c-141">-Confirm</span></span>
<span data-ttu-id="2232c-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2232c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2232c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2232c-143">-WhatIf</span></span>
<span data-ttu-id="2232c-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2232c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2232c-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2232c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2232c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2232c-146">CommonParameters</span></span>
<span data-ttu-id="2232c-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2232c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2232c-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2232c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2232c-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2232c-149">INPUTS</span></span>

### <span data-ttu-id="2232c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2232c-150">System.String</span></span>

### <span data-ttu-id="2232c-151">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="2232c-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="2232c-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2232c-152">OUTPUTS</span></span>

### <span data-ttu-id="2232c-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2232c-153">System.Boolean</span></span>

## <span data-ttu-id="2232c-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2232c-154">NOTES</span></span>

## <span data-ttu-id="2232c-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2232c-155">RELATED LINKS</span></span>
