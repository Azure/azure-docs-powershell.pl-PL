---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4a91c2f8fdda1d2cda7c75f0cf7cfab165701f3d
ms.sourcegitcommit: e57be0da5162efeb0a01f396e2343dd137920063
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/05/2021
ms.locfileid: "99572109"
---
# <span data-ttu-id="0e206-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="0e206-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="0e206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e206-102">SYNOPSIS</span></span>
<span data-ttu-id="0e206-103">Pobiera usługę w topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="0e206-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="0e206-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e206-104">SYNTAX</span></span>

### <span data-ttu-id="0e206-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0e206-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e206-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="0e206-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e206-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="0e206-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e206-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e206-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e206-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="0e206-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e206-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e206-110">DESCRIPTION</span></span>
<span data-ttu-id="0e206-111">Polecenie **cmdlet Get-AzureRmDeploymentManagerService** pobiera usługę w topologii usługi i zwraca obiekt reprezentujący usługę.</span><span class="sxs-lookup"><span data-stu-id="0e206-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="0e206-112">Określ usługę według jej nazwy, topologii usługi oraz nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e206-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="0e206-113">Ewentualnie możesz podać obiekt Service lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0e206-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="0e206-114">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do usługi za pomocą Set-AzureRmDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e206-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="0e206-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e206-115">EXAMPLES</span></span>

### <span data-ttu-id="0e206-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e206-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="0e206-117">To polecenie pobiera usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0e206-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0e206-118">Przykład 2. Uzyskiwanie usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="0e206-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="0e206-119">To polecenie pobiera usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0e206-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0e206-120">Przykład 3. Uzyskiwanie usługi przy użyciu obiektu usługi.</span><span class="sxs-lookup"><span data-stu-id="0e206-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="0e206-121">To polecenie pobiera usługę, której nazwa, nazwa topologii usługi i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa_usługi) i NazwaGrupy Zasobów ($serviceObject Nazwa Grupy Zasobów).</span><span class="sxs-lookup"><span data-stu-id="0e206-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="0e206-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e206-122">PARAMETERS</span></span>

### <span data-ttu-id="0e206-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e206-123">-DefaultProfile</span></span>
<span data-ttu-id="0e206-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e206-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e206-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0e206-125">-Name</span></span>
<span data-ttu-id="0e206-126">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="0e206-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e206-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e206-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e206-128">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e206-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e206-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e206-129">-ResourceId</span></span>
<span data-ttu-id="0e206-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="0e206-130">The resource identifier.</span></span>

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

### <span data-ttu-id="0e206-131">— Usługa</span><span class="sxs-lookup"><span data-stu-id="0e206-131">-Service</span></span>
<span data-ttu-id="0e206-132">Obiekt Service.</span><span class="sxs-lookup"><span data-stu-id="0e206-132">Service object.</span></span>

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

### <span data-ttu-id="0e206-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="0e206-133">-ServiceTopology</span></span>
<span data-ttu-id="0e206-134">Obiekt topologii usługi, w którym powinna zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="0e206-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="0e206-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="0e206-135">-ServiceTopologyName</span></span>
<span data-ttu-id="0e206-136">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="0e206-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="0e206-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="0e206-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="0e206-138">Identyfikator zasobu topologii usługi, w którym należy utworzyć usługę.</span><span class="sxs-lookup"><span data-stu-id="0e206-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="0e206-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e206-139">CommonParameters</span></span>
<span data-ttu-id="0e206-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e206-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e206-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e206-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e206-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e206-142">INPUTS</span></span>

### <span data-ttu-id="0e206-143">Brak</span><span class="sxs-lookup"><span data-stu-id="0e206-143">None</span></span>

## <span data-ttu-id="0e206-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e206-144">OUTPUTS</span></span>

### <span data-ttu-id="0e206-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="0e206-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="0e206-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e206-146">NOTES</span></span>

## <span data-ttu-id="0e206-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e206-147">RELATED LINKS</span></span>

[<span data-ttu-id="0e206-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="0e206-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="0e206-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="0e206-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="0e206-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="0e206-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)
