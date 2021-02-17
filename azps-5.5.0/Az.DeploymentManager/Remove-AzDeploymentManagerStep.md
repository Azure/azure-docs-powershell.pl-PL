---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198011"
---
# <span data-ttu-id="5ba7f-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="5ba7f-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="5ba7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ba7f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba7f-103">Usuwa krok.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-103">Deletes the step.</span></span>

## <span data-ttu-id="5ba7f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ba7f-104">SYNTAX</span></span>

### <span data-ttu-id="5ba7f-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5ba7f-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ba7f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ba7f-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ba7f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5ba7f-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ba7f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ba7f-108">DESCRIPTION</span></span>
<span data-ttu-id="5ba7f-109">Polecenie **cmdlet Remove-AzDeploymentManagerStep** usuwa krok.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="5ba7f-110">Określ krok według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="5ba7f-111">Ewentualnie możesz podać obiekt Step lub Identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="5ba7f-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ba7f-112">EXAMPLES</span></span>

### <span data-ttu-id="5ba7f-113">Przykład 1. Usuwanie kroku</span><span class="sxs-lookup"><span data-stu-id="5ba7f-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="5ba7f-114">To polecenie usuwa krok o nazwie ContosoService1WaitStep w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5ba7f-115">Przykład 2. Usuwanie etapu przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="5ba7f-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="5ba7f-116">To polecenie usuwa krok o nazwie ContosoService1WaitStep w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5ba7f-117">Przykład 3. Usuwanie etapu przy użyciu obiektu zwróconego przez New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="5ba7f-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="5ba7f-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ba7f-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="5ba7f-119">To polecenie usuwa etap, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $stepObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="5ba7f-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="5ba7f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ba7f-120">PARAMETERS</span></span>

### <span data-ttu-id="5ba7f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba7f-121">-DefaultProfile</span></span>
<span data-ttu-id="5ba7f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba7f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ba7f-123">-InputObject</span></span>
<span data-ttu-id="5ba7f-124">Krok do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ba7f-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5ba7f-125">-Name</span></span>
<span data-ttu-id="5ba7f-126">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-126">The name of the step.</span></span>

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

### <span data-ttu-id="5ba7f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ba7f-127">-PassThru</span></span>
<span data-ttu-id="5ba7f-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5ba7f-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5ba7f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba7f-129">-ResourceGroupName</span></span>
<span data-ttu-id="5ba7f-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-130">The resource group.</span></span>

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

### <span data-ttu-id="5ba7f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ba7f-131">-ResourceId</span></span>
<span data-ttu-id="5ba7f-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-132">The resource identifier.</span></span>

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

### <span data-ttu-id="5ba7f-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ba7f-133">-Confirm</span></span>
<span data-ttu-id="5ba7f-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ba7f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ba7f-135">-WhatIf</span></span>
<span data-ttu-id="5ba7f-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ba7f-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ba7f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba7f-138">CommonParameters</span></span>
<span data-ttu-id="5ba7f-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba7f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba7f-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ba7f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba7f-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ba7f-141">INPUTS</span></span>

### <span data-ttu-id="5ba7f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5ba7f-142">System.String</span></span>

### <span data-ttu-id="5ba7f-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="5ba7f-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="5ba7f-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ba7f-144">OUTPUTS</span></span>

### <span data-ttu-id="5ba7f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ba7f-145">System.Boolean</span></span>

## <span data-ttu-id="5ba7f-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ba7f-146">NOTES</span></span>

## <span data-ttu-id="5ba7f-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ba7f-147">RELATED LINKS</span></span>
