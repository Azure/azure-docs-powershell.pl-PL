---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 607e094a03d43704057af80266a6f9f2b669d3b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709972"
---
# <span data-ttu-id="1aeab-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="1aeab-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="1aeab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1aeab-102">SYNOPSIS</span></span>
<span data-ttu-id="1aeab-103">Pobiera jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-103">Gets the service unit.</span></span>

## <span data-ttu-id="1aeab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1aeab-104">SYNTAX</span></span>

### <span data-ttu-id="1aeab-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1aeab-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aeab-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="1aeab-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aeab-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="1aeab-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> [-ServiceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aeab-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="1aeab-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1aeab-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="1aeab-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aeab-110">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1aeab-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1aeab-111">Inputobject</span><span class="sxs-lookup"><span data-stu-id="1aeab-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ServiceUnitObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aeab-112">Opis</span><span class="sxs-lookup"><span data-stu-id="1aeab-112">DESCRIPTION</span></span>
<span data-ttu-id="1aeab-113">Polecenie cmdlet **Get-AzDeploymentManagerServiceUnit** pobiera jednostkę usługi w usłudze.</span><span class="sxs-lookup"><span data-stu-id="1aeab-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="1aeab-114">Określ jednostkę usługi według jej nazwy, usługę, w której została ona zdefiniowana, nazwę topologii usług i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1aeab-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="1aeab-115">Alternatywnie możesz podać obiekt serviceunit lub identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1aeab-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="1aeab-116">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do jednostki usługi za pomocą polecenia cmdlet Set-AzDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="1aeab-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="1aeab-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1aeab-117">EXAMPLES</span></span>

### <span data-ttu-id="1aeab-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1aeab-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="1aeab-119">To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1aeab-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1aeab-120">Przykład 2: uzyskiwanie jednostki usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="1aeab-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="1aeab-121">To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1aeab-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1aeab-122">Przykład 3: uzyskiwanie jednostki usługi przy użyciu obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="1aeab-123">To polecenie uzyskuje jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i element źródła $serviceUnitObject danych są zgodne odpowiednio z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="1aeab-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="1aeab-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1aeab-124">PARAMETERS</span></span>

### <span data-ttu-id="1aeab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aeab-125">-DefaultProfile</span></span>
<span data-ttu-id="1aeab-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1aeab-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aeab-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1aeab-127">-Name</span></span>
<span data-ttu-id="1aeab-128">Nazwa jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aeab-129">-ResourceGroupName</span></span>
<span data-ttu-id="1aeab-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="1aeab-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeab-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aeab-131">-ResourceId</span></span>
<span data-ttu-id="1aeab-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1aeab-132">The resource identifier.</span></span>

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

### <span data-ttu-id="1aeab-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1aeab-133">-ServiceName</span></span>
<span data-ttu-id="1aeab-134">Nazwa usługi, do której należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-134">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="1aeab-135">-Serviceobject</span><span class="sxs-lookup"><span data-stu-id="1aeab-135">-ServiceObject</span></span>
<span data-ttu-id="1aeab-136">Obiekt usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-136">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="1aeab-137">-Serviceresourceid</span><span class="sxs-lookup"><span data-stu-id="1aeab-137">-ServiceResourceId</span></span>
<span data-ttu-id="1aeab-138">Identyfikator zasobu usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="1aeab-139">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="1aeab-139">-ServiceTopologyName</span></span>
<span data-ttu-id="1aeab-140">Nazwa topologii usługi, do której należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-140">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="1aeab-141">-Servicetopologyobject</span><span class="sxs-lookup"><span data-stu-id="1aeab-141">-ServiceTopologyObject</span></span>
<span data-ttu-id="1aeab-142">Obiekt z topologią usług, w którym należy utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-142">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="1aeab-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="1aeab-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="1aeab-144">Identyfikator zasobu topologii usług, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="1aeab-145">-Serviceunitobject</span><span class="sxs-lookup"><span data-stu-id="1aeab-145">-ServiceUnitObject</span></span>
<span data-ttu-id="1aeab-146">Obiekt zasobu jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="1aeab-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="1aeab-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aeab-147">CommonParameters</span></span>
<span data-ttu-id="1aeab-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aeab-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aeab-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aeab-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aeab-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1aeab-150">INPUTS</span></span>

### <span data-ttu-id="1aeab-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1aeab-151">System.String</span></span>

### <span data-ttu-id="1aeab-152">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="1aeab-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="1aeab-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1aeab-153">OUTPUTS</span></span>

### <span data-ttu-id="1aeab-154">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="1aeab-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="1aeab-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1aeab-155">NOTES</span></span>

## <span data-ttu-id="1aeab-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1aeab-156">RELATED LINKS</span></span>