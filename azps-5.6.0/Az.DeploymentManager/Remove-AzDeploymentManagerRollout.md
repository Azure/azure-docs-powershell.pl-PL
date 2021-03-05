---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 3ade9bfd724a84e162c0cedd937f2255ebb5b6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980698"
---
# <span data-ttu-id="e39c5-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="e39c5-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="e39c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e39c5-102">SYNOPSIS</span></span>
<span data-ttu-id="e39c5-103">Usuwa to rozsyłanie.</span><span class="sxs-lookup"><span data-stu-id="e39c5-103">Deletes the rollout.</span></span>

## <span data-ttu-id="e39c5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e39c5-104">SYNTAX</span></span>

### <span data-ttu-id="e39c5-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="e39c5-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e39c5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e39c5-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e39c5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e39c5-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e39c5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e39c5-108">DESCRIPTION</span></span>
<span data-ttu-id="e39c5-109">Polecenie **cmdlet Remove-AzDeploymentManagerRollout** usuwa rolkę w stanie terminalu.</span><span class="sxs-lookup"><span data-stu-id="e39c5-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="e39c5-110">Określ wycofanie według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e39c5-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="e39c5-111">Ewentualnie możesz podać obiekt Rollout lub Identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="e39c5-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="e39c5-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e39c5-112">EXAMPLES</span></span>

### <span data-ttu-id="e39c5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e39c5-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="e39c5-114">To polecenie usuwa wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e39c5-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e39c5-115">Przykład 2. Usuwanie rzutowania przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="e39c5-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="e39c5-116">To polecenie usuwa wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e39c5-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e39c5-117">Przykład 3. Usuwanie rzutowania przy użyciu obiektu rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="e39c5-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="e39c5-118">To polecenie usuwa rzutowanie, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) i ResourceGroupName $rolloutObject grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e39c5-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="e39c5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e39c5-119">PARAMETERS</span></span>

### <span data-ttu-id="e39c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e39c5-120">-DefaultProfile</span></span>
<span data-ttu-id="e39c5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e39c5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e39c5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e39c5-122">-InputObject</span></span>
<span data-ttu-id="e39c5-123">Zasób do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e39c5-123">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e39c5-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e39c5-124">-Name</span></span>
<span data-ttu-id="e39c5-125">Nazwa tego rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="e39c5-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="e39c5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e39c5-126">-PassThru</span></span>
<span data-ttu-id="e39c5-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e39c5-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e39c5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e39c5-128">-ResourceGroupName</span></span>
<span data-ttu-id="e39c5-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="e39c5-129">The resource group.</span></span>

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

### <span data-ttu-id="e39c5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e39c5-130">-ResourceId</span></span>
<span data-ttu-id="e39c5-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e39c5-131">The resource identifier.</span></span>

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

### <span data-ttu-id="e39c5-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e39c5-132">-Confirm</span></span>
<span data-ttu-id="e39c5-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e39c5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e39c5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e39c5-134">-WhatIf</span></span>
<span data-ttu-id="e39c5-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e39c5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e39c5-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e39c5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e39c5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e39c5-137">CommonParameters</span></span>
<span data-ttu-id="e39c5-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e39c5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e39c5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e39c5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e39c5-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e39c5-140">INPUTS</span></span>

### <span data-ttu-id="e39c5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e39c5-141">System.String</span></span>

### <span data-ttu-id="e39c5-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="e39c5-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e39c5-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e39c5-143">OUTPUTS</span></span>

### <span data-ttu-id="e39c5-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e39c5-144">System.Boolean</span></span>

## <span data-ttu-id="e39c5-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e39c5-145">NOTES</span></span>

## <span data-ttu-id="e39c5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e39c5-146">RELATED LINKS</span></span>
