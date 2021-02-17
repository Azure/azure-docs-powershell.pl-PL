---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177010"
---
# <span data-ttu-id="88a41-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="88a41-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="88a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88a41-102">SYNOPSIS</span></span>
<span data-ttu-id="88a41-103">Pobiera usługę.</span><span class="sxs-lookup"><span data-stu-id="88a41-103">Gets the service.</span></span>

## <span data-ttu-id="88a41-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88a41-104">SYNTAX</span></span>

### <span data-ttu-id="88a41-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="88a41-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88a41-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="88a41-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88a41-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="88a41-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88a41-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="88a41-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88a41-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="88a41-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88a41-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="88a41-110">DESCRIPTION</span></span>
<span data-ttu-id="88a41-111">Polecenie **cmdlet Get-AzDeploymentManagerService** pobiera usługę w topologii usługi i zwraca obiekt reprezentujący usługę.</span><span class="sxs-lookup"><span data-stu-id="88a41-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="88a41-112">Określ usługę według jej nazwy, topologii usługi oraz nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88a41-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="88a41-113">Ewentualnie możesz podać obiekt Service lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="88a41-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="88a41-114">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do usługi za pomocą Set-AzDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88a41-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="88a41-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88a41-115">EXAMPLES</span></span>

### <span data-ttu-id="88a41-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88a41-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="88a41-117">To polecenie pobiera usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="88a41-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="88a41-118">Przykład 2. Uzyskiwanie usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="88a41-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="88a41-119">To polecenie pobiera usługę o nazwie ContosoService1 w topologii usługi ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="88a41-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="88a41-120">Przykład 3. Uzyskiwanie usługi przy użyciu obiektu usługi.</span><span class="sxs-lookup"><span data-stu-id="88a41-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="88a41-121">To polecenie pobiera usługę, której nazwa, nazwa topologii usługi i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa_usługi) i NazwaGrupy Zasobów ($serviceObject Nazwa Grupy Zasobów).</span><span class="sxs-lookup"><span data-stu-id="88a41-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="88a41-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88a41-122">PARAMETERS</span></span>

### <span data-ttu-id="88a41-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a41-123">-DefaultProfile</span></span>
<span data-ttu-id="88a41-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="88a41-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88a41-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88a41-125">-InputObject</span></span>
<span data-ttu-id="88a41-126">Obiekt Service.</span><span class="sxs-lookup"><span data-stu-id="88a41-126">Service object.</span></span>

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

### <span data-ttu-id="88a41-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="88a41-127">-Name</span></span>
<span data-ttu-id="88a41-128">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="88a41-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a41-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88a41-129">-ResourceGroupName</span></span>
<span data-ttu-id="88a41-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="88a41-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a41-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88a41-131">-ResourceId</span></span>
<span data-ttu-id="88a41-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="88a41-132">The resource identifier.</span></span>

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

### <span data-ttu-id="88a41-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="88a41-133">-ServiceTopologyName</span></span>
<span data-ttu-id="88a41-134">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="88a41-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="88a41-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="88a41-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="88a41-136">Obiekt topologii usługi, w którym powinna zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="88a41-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a41-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="88a41-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="88a41-138">Identyfikator zasobu topologii usługi, w którym należy utworzyć usługę.</span><span class="sxs-lookup"><span data-stu-id="88a41-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a41-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a41-139">CommonParameters</span></span>
<span data-ttu-id="88a41-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88a41-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a41-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88a41-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a41-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88a41-142">INPUTS</span></span>

### <span data-ttu-id="88a41-143">System.String</span><span class="sxs-lookup"><span data-stu-id="88a41-143">System.String</span></span>

### <span data-ttu-id="88a41-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="88a41-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="88a41-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88a41-145">OUTPUTS</span></span>

### <span data-ttu-id="88a41-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="88a41-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="88a41-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88a41-147">NOTES</span></span>

## <span data-ttu-id="88a41-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88a41-148">RELATED LINKS</span></span>
