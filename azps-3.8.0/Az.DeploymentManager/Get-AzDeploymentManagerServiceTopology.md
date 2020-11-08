---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053360"
---
# <span data-ttu-id="46538-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="46538-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="46538-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46538-102">SYNOPSIS</span></span>
<span data-ttu-id="46538-103">Pobiera topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="46538-103">Gets the service topology.</span></span>

## <span data-ttu-id="46538-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46538-104">SYNTAX</span></span>

### <span data-ttu-id="46538-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="46538-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46538-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="46538-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46538-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="46538-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46538-108">Opis</span><span class="sxs-lookup"><span data-stu-id="46538-108">DESCRIPTION</span></span>
<span data-ttu-id="46538-109">Polecenie cmdlet **Get-AzDeploymentManagerServiceTopology** pobiera topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="46538-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="46538-110">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w topologii, korzystając z polecenia cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="46538-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="46538-111">Określ topologię usługi według jej nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46538-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="46538-112">Alternatywnie możesz podać obiekt servicetopology lub identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="46538-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="46538-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46538-113">EXAMPLES</span></span>

### <span data-ttu-id="46538-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46538-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="46538-115">To polecenie uzyskuje topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="46538-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="46538-116">Przykład 2: uzyskiwanie topologii usług przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="46538-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="46538-117">To polecenie uzyskuje topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="46538-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="46538-118">Przykład 3: uzyskiwanie topologii usług przy użyciu obiektu typu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="46538-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="46538-119">To polecenie pobiera topologię usługi, której nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="46538-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="46538-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46538-120">PARAMETERS</span></span>

### <span data-ttu-id="46538-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46538-121">-DefaultProfile</span></span>
<span data-ttu-id="46538-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46538-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46538-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="46538-123">-InputObject</span></span>
<span data-ttu-id="46538-124">Obiekt zasobu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="46538-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="46538-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="46538-125">-Name</span></span>
<span data-ttu-id="46538-126">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="46538-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="46538-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46538-127">-ResourceGroupName</span></span>
<span data-ttu-id="46538-128">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="46538-128">The resource group.</span></span>

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

### <span data-ttu-id="46538-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46538-129">-ResourceId</span></span>
<span data-ttu-id="46538-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="46538-130">The resource identifier.</span></span>

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

### <span data-ttu-id="46538-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46538-131">CommonParameters</span></span>
<span data-ttu-id="46538-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46538-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46538-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46538-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46538-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46538-134">INPUTS</span></span>

### <span data-ttu-id="46538-135">System. String</span><span class="sxs-lookup"><span data-stu-id="46538-135">System.String</span></span>

### <span data-ttu-id="46538-136">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="46538-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="46538-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46538-137">OUTPUTS</span></span>

### <span data-ttu-id="46538-138">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="46538-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="46538-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46538-139">NOTES</span></span>

## <span data-ttu-id="46538-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46538-140">RELATED LINKS</span></span>
