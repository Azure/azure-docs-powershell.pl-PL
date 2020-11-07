---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 695a10eb71cc2c4bd1a6bc7eef6cba265d524fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705611"
---
# <span data-ttu-id="77ab1-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="77ab1-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="77ab1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="77ab1-103">Usuwa topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="77ab1-103">Deletes the service topology.</span></span> <span data-ttu-id="77ab1-104">Przed usunięciem topologii usługi należy usunąć wszystkie usługi utworzone w ramach topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="77ab1-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="77ab1-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77ab1-105">SYNTAX</span></span>

### <span data-ttu-id="77ab1-106">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="77ab1-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77ab1-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="77ab1-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77ab1-108">Inputobject</span><span class="sxs-lookup"><span data-stu-id="77ab1-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77ab1-109">Opis</span><span class="sxs-lookup"><span data-stu-id="77ab1-109">DESCRIPTION</span></span>
<span data-ttu-id="77ab1-110">Polecenie cmdlet **Remove-AzDeploymentManagerServiceTopology** usuwa topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="77ab1-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="77ab1-111">Określ topologię usługi według jej nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77ab1-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="77ab1-112">Alternatywnie możesz podać obiekt servicetopology lub identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="77ab1-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="77ab1-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77ab1-113">EXAMPLES</span></span>

### <span data-ttu-id="77ab1-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77ab1-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="77ab1-115">To polecenie usuwa topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="77ab1-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="77ab1-116">Przykład 2: usunięcie topologii usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="77ab1-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="77ab1-117">To polecenie usuwa topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="77ab1-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="77ab1-118">Przykład 3: usuwanie topologii usług przy użyciu obiektu typu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="77ab1-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="77ab1-119">To polecenie usuwa topologię usługi, której nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="77ab1-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="77ab1-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77ab1-120">PARAMETERS</span></span>

### <span data-ttu-id="77ab1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ab1-121">-DefaultProfile</span></span>
<span data-ttu-id="77ab1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77ab1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77ab1-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77ab1-123">-InputObject</span></span>
<span data-ttu-id="77ab1-124">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="77ab1-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="77ab1-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77ab1-125">-Name</span></span>
<span data-ttu-id="77ab1-126">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="77ab1-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="77ab1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77ab1-127">-PassThru</span></span>
<span data-ttu-id="77ab1-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="77ab1-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="77ab1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ab1-129">-ResourceGroupName</span></span>
<span data-ttu-id="77ab1-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="77ab1-130">The resource group.</span></span>

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

### <span data-ttu-id="77ab1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77ab1-131">-ResourceId</span></span>
<span data-ttu-id="77ab1-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="77ab1-132">The resource identifier.</span></span>

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

### <span data-ttu-id="77ab1-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77ab1-133">-Confirm</span></span>
<span data-ttu-id="77ab1-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77ab1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77ab1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77ab1-135">-WhatIf</span></span>
<span data-ttu-id="77ab1-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77ab1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77ab1-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77ab1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77ab1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ab1-138">CommonParameters</span></span>
<span data-ttu-id="77ab1-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77ab1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ab1-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77ab1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ab1-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77ab1-141">INPUTS</span></span>

### <span data-ttu-id="77ab1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="77ab1-142">System.String</span></span>

### <span data-ttu-id="77ab1-143">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="77ab1-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="77ab1-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77ab1-144">OUTPUTS</span></span>

### <span data-ttu-id="77ab1-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77ab1-145">System.Boolean</span></span>

## <span data-ttu-id="77ab1-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77ab1-146">NOTES</span></span>

## <span data-ttu-id="77ab1-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77ab1-147">RELATED LINKS</span></span>