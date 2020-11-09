---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304998"
---
# <span data-ttu-id="6dc01-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="6dc01-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="6dc01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6dc01-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc01-103">Pobiera usługę.</span><span class="sxs-lookup"><span data-stu-id="6dc01-103">Gets the service.</span></span>

## <span data-ttu-id="6dc01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6dc01-104">SYNTAX</span></span>

### <span data-ttu-id="6dc01-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6dc01-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dc01-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="6dc01-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dc01-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="6dc01-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dc01-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="6dc01-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dc01-109">Inputobject</span><span class="sxs-lookup"><span data-stu-id="6dc01-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dc01-110">Opis</span><span class="sxs-lookup"><span data-stu-id="6dc01-110">DESCRIPTION</span></span>
<span data-ttu-id="6dc01-111">Polecenie cmdlet **Get-AzDeploymentManagerService** pobiera usługę w ramach topologii usług i zwraca obiekt reprezentujący tę usługę.</span><span class="sxs-lookup"><span data-stu-id="6dc01-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="6dc01-112">Określ usługę za pomocą jej nazwy, topologii usługi i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6dc01-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="6dc01-113">Alternatywnie możesz podać obiekt Service lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6dc01-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="6dc01-114">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w usłudze za pomocą polecenia cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="6dc01-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="6dc01-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6dc01-115">EXAMPLES</span></span>

### <span data-ttu-id="6dc01-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6dc01-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="6dc01-117">To polecenie uzyskuje usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6dc01-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6dc01-118">Przykład 2: Uzyskiwanie usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="6dc01-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="6dc01-119">To polecenie uzyskuje usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6dc01-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6dc01-120">Przykład 3: Uzyskiwanie usługi przy użyciu przedmiotu serwisu.</span><span class="sxs-lookup"><span data-stu-id="6dc01-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="6dc01-121">To polecenie uzyskuje usługę, której nazwa, nazwa topologii usługi i nazwa źródła zasobów są zgodne z właściwościami Name, servicetopologyname i ResourceGroupName w $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="6dc01-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="6dc01-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6dc01-122">PARAMETERS</span></span>

### <span data-ttu-id="6dc01-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc01-123">-DefaultProfile</span></span>
<span data-ttu-id="6dc01-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6dc01-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dc01-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6dc01-125">-InputObject</span></span>
<span data-ttu-id="6dc01-126">Obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="6dc01-126">Service object.</span></span>

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

### <span data-ttu-id="6dc01-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6dc01-127">-Name</span></span>
<span data-ttu-id="6dc01-128">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="6dc01-128">The name of the service.</span></span>

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

### <span data-ttu-id="6dc01-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc01-129">-ResourceGroupName</span></span>
<span data-ttu-id="6dc01-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="6dc01-130">The resource group.</span></span>

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

### <span data-ttu-id="6dc01-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dc01-131">-ResourceId</span></span>
<span data-ttu-id="6dc01-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="6dc01-132">The resource identifier.</span></span>

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

### <span data-ttu-id="6dc01-133">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="6dc01-133">-ServiceTopologyName</span></span>
<span data-ttu-id="6dc01-134">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="6dc01-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="6dc01-135">-Servicetopologyobject</span><span class="sxs-lookup"><span data-stu-id="6dc01-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="6dc01-136">Obiekt z topologią usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="6dc01-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="6dc01-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="6dc01-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="6dc01-138">Identyfikator zasobu topologii usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="6dc01-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="6dc01-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc01-139">CommonParameters</span></span>
<span data-ttu-id="6dc01-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc01-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc01-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dc01-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc01-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6dc01-142">INPUTS</span></span>

### <span data-ttu-id="6dc01-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc01-143">System.String</span></span>

### <span data-ttu-id="6dc01-144">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="6dc01-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="6dc01-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6dc01-145">OUTPUTS</span></span>

### <span data-ttu-id="6dc01-146">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="6dc01-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="6dc01-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6dc01-147">NOTES</span></span>

## <span data-ttu-id="6dc01-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6dc01-148">RELATED LINKS</span></span>
