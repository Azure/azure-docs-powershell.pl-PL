---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524097"
---
# <span data-ttu-id="debfe-101">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="debfe-101">Get-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="debfe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="debfe-102">SYNOPSIS</span></span>
<span data-ttu-id="debfe-103">Pobiera topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="debfe-103">Gets a service topology.</span></span>

## <span data-ttu-id="debfe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="debfe-104">SYNTAX</span></span>

### <span data-ttu-id="debfe-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="debfe-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="debfe-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="debfe-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="debfe-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="debfe-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="debfe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="debfe-108">DESCRIPTION</span></span>
<span data-ttu-id="debfe-109">Polecenie cmdlet **Get-AzureRmDeploymentManagerServiceTopology** pobiera topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="debfe-109">The **Get-AzureRmDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="debfe-110">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w topologii, korzystając z polecenia cmdlet Set-AzureRmDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="debfe-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="debfe-111">Określ topologię usługi według jej nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="debfe-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="debfe-112">Alternatywnie możesz podać obiekt servicetopology lub identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="debfe-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="debfe-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="debfe-113">EXAMPLES</span></span>

### <span data-ttu-id="debfe-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="debfe-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="debfe-115">To polecenie uzyskuje topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="debfe-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="debfe-116">Przykład 2: uzyskiwanie topologii usług przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="debfe-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="debfe-117">To polecenie uzyskuje topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="debfe-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="debfe-118">Przykład 3: uzyskiwanie topologii usług przy użyciu obiektu typu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="debfe-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="debfe-119">To polecenie pobiera topologię usługi, której nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="debfe-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="debfe-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="debfe-120">PARAMETERS</span></span>

### <span data-ttu-id="debfe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debfe-121">-DefaultProfile</span></span>
<span data-ttu-id="debfe-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="debfe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="debfe-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="debfe-123">-Name</span></span>
<span data-ttu-id="debfe-124">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="debfe-124">The name of the service topology.</span></span>

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

### <span data-ttu-id="debfe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="debfe-125">-ResourceGroupName</span></span>
<span data-ttu-id="debfe-126">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="debfe-126">The resource group.</span></span>

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

### <span data-ttu-id="debfe-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="debfe-127">-ResourceId</span></span>
<span data-ttu-id="debfe-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="debfe-128">The resource identifier.</span></span>

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

### <span data-ttu-id="debfe-129">-Servicetopology</span><span class="sxs-lookup"><span data-stu-id="debfe-129">-ServiceTopology</span></span>
<span data-ttu-id="debfe-130">Obiekt zasobu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="debfe-130">Service topology resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="debfe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debfe-131">CommonParameters</span></span>
<span data-ttu-id="debfe-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="debfe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debfe-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="debfe-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debfe-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="debfe-134">INPUTS</span></span>

### <span data-ttu-id="debfe-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="debfe-135">None</span></span>

## <span data-ttu-id="debfe-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="debfe-136">OUTPUTS</span></span>

### <span data-ttu-id="debfe-137">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="debfe-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="debfe-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="debfe-138">NOTES</span></span>

## <span data-ttu-id="debfe-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="debfe-139">RELATED LINKS</span></span>

[<span data-ttu-id="debfe-140">Nowe — AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="debfe-140">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="debfe-141">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="debfe-141">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="debfe-142">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="debfe-142">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)