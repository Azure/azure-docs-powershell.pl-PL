---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
content_git_url: ''
ms.openlocfilehash: 655cfeeae35d1b48bbfe2149fd4262dffe72ae09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524093"
---
# <span data-ttu-id="60a46-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="60a46-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="60a46-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60a46-102">SYNOPSIS</span></span>
<span data-ttu-id="60a46-103">Pobiera usługę w topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="60a46-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="60a46-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60a46-104">SYNTAX</span></span>

### <span data-ttu-id="60a46-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="60a46-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60a46-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="60a46-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60a46-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="60a46-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60a46-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="60a46-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60a46-109">Inputobject</span><span class="sxs-lookup"><span data-stu-id="60a46-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60a46-110">Opis</span><span class="sxs-lookup"><span data-stu-id="60a46-110">DESCRIPTION</span></span>
<span data-ttu-id="60a46-111">Polecenie cmdlet **Get-AzureRmDeploymentManagerService** pobiera usługę w ramach topologii usług i zwraca obiekt reprezentujący tę usługę.</span><span class="sxs-lookup"><span data-stu-id="60a46-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="60a46-112">Określ usługę za pomocą jej nazwy, topologii usługi i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="60a46-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="60a46-113">Alternatywnie możesz podać obiekt Service lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="60a46-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="60a46-114">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w usłudze za pomocą polecenia cmdlet Set-AzureRmDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="60a46-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="60a46-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60a46-115">EXAMPLES</span></span>

### <span data-ttu-id="60a46-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60a46-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="60a46-117">To polecenie uzyskuje usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="60a46-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="60a46-118">Przykład 2: Uzyskiwanie usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="60a46-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="60a46-119">To polecenie uzyskuje usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="60a46-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="60a46-120">Przykład 3: Uzyskiwanie usługi przy użyciu przedmiotu serwisu.</span><span class="sxs-lookup"><span data-stu-id="60a46-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="60a46-121">To polecenie uzyskuje usługę, której nazwa, nazwa topologii usługi i nazwa źródła zasobów są zgodne z właściwościami Name, servicetopologyname i ResourceGroupName w $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="60a46-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="60a46-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60a46-122">PARAMETERS</span></span>

### <span data-ttu-id="60a46-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a46-123">-DefaultProfile</span></span>
<span data-ttu-id="60a46-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60a46-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a46-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60a46-125">-Name</span></span>
<span data-ttu-id="60a46-126">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="60a46-126">The name of the service.</span></span>

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

### <span data-ttu-id="60a46-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a46-127">-ResourceGroupName</span></span>
<span data-ttu-id="60a46-128">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="60a46-128">The resource group.</span></span>

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

### <span data-ttu-id="60a46-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60a46-129">-ResourceId</span></span>
<span data-ttu-id="60a46-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="60a46-130">The resource identifier.</span></span>

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

### <span data-ttu-id="60a46-131">-Service</span><span class="sxs-lookup"><span data-stu-id="60a46-131">-Service</span></span>
<span data-ttu-id="60a46-132">Obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="60a46-132">Service object.</span></span>

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

### <span data-ttu-id="60a46-133">-Servicetopology</span><span class="sxs-lookup"><span data-stu-id="60a46-133">-ServiceTopology</span></span>
<span data-ttu-id="60a46-134">Obiekt z topologią usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="60a46-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="60a46-135">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="60a46-135">-ServiceTopologyName</span></span>
<span data-ttu-id="60a46-136">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="60a46-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="60a46-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="60a46-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="60a46-138">Identyfikator zasobu topologii usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="60a46-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="60a46-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a46-139">CommonParameters</span></span>
<span data-ttu-id="60a46-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a46-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a46-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a46-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a46-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60a46-142">INPUTS</span></span>

### <span data-ttu-id="60a46-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="60a46-143">None</span></span>

## <span data-ttu-id="60a46-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60a46-144">OUTPUTS</span></span>

### <span data-ttu-id="60a46-145">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="60a46-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="60a46-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60a46-146">NOTES</span></span>

## <span data-ttu-id="60a46-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60a46-147">RELATED LINKS</span></span>

[<span data-ttu-id="60a46-148">Nowe — AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="60a46-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="60a46-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="60a46-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="60a46-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="60a46-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)