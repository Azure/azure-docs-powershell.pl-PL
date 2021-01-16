---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387452"
---
# <span data-ttu-id="fab7e-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="fab7e-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="fab7e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fab7e-102">SYNOPSIS</span></span>
<span data-ttu-id="fab7e-103">Pobiera topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="fab7e-103">Gets the service topology.</span></span>

## <span data-ttu-id="fab7e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fab7e-104">SYNTAX</span></span>

### <span data-ttu-id="fab7e-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fab7e-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fab7e-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="fab7e-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fab7e-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="fab7e-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fab7e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fab7e-108">DESCRIPTION</span></span>
<span data-ttu-id="fab7e-109">Polecenie cmdlet **Get-AzDeploymentManagerServiceTopology** pobiera topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="fab7e-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="fab7e-110">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w topologii, korzystając z polecenia cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="fab7e-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="fab7e-111">Określ topologię usługi według jej nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fab7e-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="fab7e-112">Alternatywnie możesz podać obiekt servicetopology lub identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="fab7e-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="fab7e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fab7e-113">EXAMPLES</span></span>

### <span data-ttu-id="fab7e-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fab7e-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="fab7e-115">To polecenie uzyskuje topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fab7e-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fab7e-116">Przykład 2: uzyskiwanie topologii usług przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="fab7e-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="fab7e-117">To polecenie uzyskuje topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fab7e-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fab7e-118">Przykład 3: uzyskiwanie topologii usług przy użyciu obiektu typu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="fab7e-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="fab7e-119">To polecenie pobiera topologię usługi, której nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="fab7e-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="fab7e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fab7e-120">PARAMETERS</span></span>

### <span data-ttu-id="fab7e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab7e-121">-DefaultProfile</span></span>
<span data-ttu-id="fab7e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fab7e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fab7e-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fab7e-123">-InputObject</span></span>
<span data-ttu-id="fab7e-124">Obiekt zasobu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="fab7e-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="fab7e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fab7e-125">-Name</span></span>
<span data-ttu-id="fab7e-126">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="fab7e-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab7e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab7e-127">-ResourceGroupName</span></span>
<span data-ttu-id="fab7e-128">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="fab7e-128">The resource group.</span></span>

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

### <span data-ttu-id="fab7e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fab7e-129">-ResourceId</span></span>
<span data-ttu-id="fab7e-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="fab7e-130">The resource identifier.</span></span>

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

### <span data-ttu-id="fab7e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab7e-131">CommonParameters</span></span>
<span data-ttu-id="fab7e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab7e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab7e-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fab7e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab7e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fab7e-134">INPUTS</span></span>

### <span data-ttu-id="fab7e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fab7e-135">System.String</span></span>

### <span data-ttu-id="fab7e-136">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fab7e-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fab7e-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fab7e-137">OUTPUTS</span></span>

### <span data-ttu-id="fab7e-138">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fab7e-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fab7e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fab7e-139">NOTES</span></span>

## <span data-ttu-id="fab7e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fab7e-140">RELATED LINKS</span></span>
