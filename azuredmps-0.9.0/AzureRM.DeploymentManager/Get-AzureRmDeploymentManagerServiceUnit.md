---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e83f619bd14a2e0ba2012a206d0c3dffd5204863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710671"
---
# <span data-ttu-id="71695-101">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="71695-101">Get-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="71695-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71695-102">SYNOPSIS</span></span>
<span data-ttu-id="71695-103">Pobiera jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-103">Gets a service unit.</span></span>

## <span data-ttu-id="71695-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71695-104">SYNTAX</span></span>

### <span data-ttu-id="71695-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="71695-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71695-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="71695-106">ByServiceObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71695-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="71695-107">ByServiceResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71695-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="71695-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71695-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="71695-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71695-110">Zasobów</span><span class="sxs-lookup"><span data-stu-id="71695-110">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71695-111">Inputobject</span><span class="sxs-lookup"><span data-stu-id="71695-111">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71695-112">Opis</span><span class="sxs-lookup"><span data-stu-id="71695-112">DESCRIPTION</span></span>
<span data-ttu-id="71695-113">Polecenie cmdlet **Get-AzureRmDeploymentManagerServiceUnit** pobiera jednostkę usługi w usłudze.</span><span class="sxs-lookup"><span data-stu-id="71695-113">The **Get-AzureRmDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="71695-114">Określ jednostkę usługi według jej nazwy, usługę, w której została ona zdefiniowana, nazwę topologii usług i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71695-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="71695-115">Alternatywnie możesz podać obiekt serviceunit lub identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="71695-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="71695-116">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do jednostki usługi za pomocą polecenia cmdlet Set-AzureRmDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="71695-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzureRmDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="71695-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71695-117">EXAMPLES</span></span>

### <span data-ttu-id="71695-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71695-118">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="71695-119">To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="71695-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="71695-120">Przykład 2: uzyskiwanie jednostki usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="71695-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="71695-121">To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="71695-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="71695-122">Przykład 3: uzyskiwanie jednostki usługi przy użyciu obiektu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="71695-123">To polecenie uzyskuje jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i element źródła $serviceUnitObject danych są zgodne odpowiednio z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="71695-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="71695-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71695-124">PARAMETERS</span></span>

### <span data-ttu-id="71695-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71695-125">-DefaultProfile</span></span>
<span data-ttu-id="71695-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71695-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71695-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71695-127">-Name</span></span>
<span data-ttu-id="71695-128">Nazwa jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71695-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71695-129">-ResourceGroupName</span></span>
<span data-ttu-id="71695-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="71695-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71695-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71695-131">-ResourceId</span></span>
<span data-ttu-id="71695-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="71695-132">The resource identifier.</span></span>

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

### <span data-ttu-id="71695-133">-Service</span><span class="sxs-lookup"><span data-stu-id="71695-133">-Service</span></span>
<span data-ttu-id="71695-134">Obiekt usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-134">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="71695-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="71695-135">-ServiceName</span></span>
<span data-ttu-id="71695-136">Nazwa usługi, do której należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="71695-137">-Serviceresourceid</span><span class="sxs-lookup"><span data-stu-id="71695-137">-ServiceResourceId</span></span>
<span data-ttu-id="71695-138">Identyfikator zasobu usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="71695-139">-Servicetopology</span><span class="sxs-lookup"><span data-stu-id="71695-139">-ServiceTopology</span></span>
<span data-ttu-id="71695-140">Obiekt z topologią usług, w którym należy utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-140">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="71695-141">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="71695-141">-ServiceTopologyName</span></span>
<span data-ttu-id="71695-142">Nazwa topologii usługi, do której należy jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="71695-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="71695-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="71695-144">Identyfikator zasobu topologii usług, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="71695-145">-Serviceunit</span><span class="sxs-lookup"><span data-stu-id="71695-145">-ServiceUnit</span></span>
<span data-ttu-id="71695-146">Obiekt zasobu jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="71695-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="71695-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71695-147">CommonParameters</span></span>
<span data-ttu-id="71695-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71695-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71695-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71695-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71695-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71695-150">INPUTS</span></span>

### <span data-ttu-id="71695-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="71695-151">None</span></span>

## <span data-ttu-id="71695-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71695-152">OUTPUTS</span></span>

### <span data-ttu-id="71695-153">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="71695-153">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="71695-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71695-154">NOTES</span></span>

## <span data-ttu-id="71695-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71695-155">RELATED LINKS</span></span>

[<span data-ttu-id="71695-156">Nowe — AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="71695-156">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="71695-157">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="71695-157">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="71695-158">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="71695-158">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)