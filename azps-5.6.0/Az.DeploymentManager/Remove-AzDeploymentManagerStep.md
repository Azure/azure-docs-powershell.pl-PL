---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 96f5f9e3dd0390d714b0ee7a74b3f585b46dcc1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966305"
---
# <span data-ttu-id="d107d-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="d107d-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="d107d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d107d-102">SYNOPSIS</span></span>
<span data-ttu-id="d107d-103">Usuwa krok.</span><span class="sxs-lookup"><span data-stu-id="d107d-103">Deletes the step.</span></span>

## <span data-ttu-id="d107d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d107d-104">SYNTAX</span></span>

### <span data-ttu-id="d107d-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d107d-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d107d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d107d-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d107d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d107d-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d107d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d107d-108">DESCRIPTION</span></span>
<span data-ttu-id="d107d-109">Polecenie **cmdlet Remove-AzDeploymentManagerStep** usuwa krok.</span><span class="sxs-lookup"><span data-stu-id="d107d-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="d107d-110">Określ krok według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d107d-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="d107d-111">Ewentualnie możesz podać obiekt Step lub Identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="d107d-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="d107d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d107d-112">EXAMPLES</span></span>

### <span data-ttu-id="d107d-113">Przykład 1. Usuwanie kroku</span><span class="sxs-lookup"><span data-stu-id="d107d-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="d107d-114">To polecenie usuwa krok o nazwie ContosoService1WaitStep w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d107d-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d107d-115">Przykład 2. Usuwanie etapu przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="d107d-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="d107d-116">To polecenie usuwa krok o nazwie ContosoService1WaitStep w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d107d-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="d107d-117">Przykład 3. Usuwanie etapu przy użyciu obiektu zwróconego przez New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="d107d-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="d107d-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d107d-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="d107d-119">To polecenie usuwa etap, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $stepObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="d107d-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="d107d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d107d-120">PARAMETERS</span></span>

### <span data-ttu-id="d107d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d107d-121">-DefaultProfile</span></span>
<span data-ttu-id="d107d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d107d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d107d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d107d-123">-InputObject</span></span>
<span data-ttu-id="d107d-124">Krok do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d107d-124">The step to be removed.</span></span>

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

### <span data-ttu-id="d107d-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d107d-125">-Name</span></span>
<span data-ttu-id="d107d-126">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="d107d-126">The name of the step.</span></span>

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

### <span data-ttu-id="d107d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d107d-127">-PassThru</span></span>
<span data-ttu-id="d107d-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d107d-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d107d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d107d-129">-ResourceGroupName</span></span>
<span data-ttu-id="d107d-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="d107d-130">The resource group.</span></span>

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

### <span data-ttu-id="d107d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d107d-131">-ResourceId</span></span>
<span data-ttu-id="d107d-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d107d-132">The resource identifier.</span></span>

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

### <span data-ttu-id="d107d-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d107d-133">-Confirm</span></span>
<span data-ttu-id="d107d-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d107d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d107d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d107d-135">-WhatIf</span></span>
<span data-ttu-id="d107d-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d107d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d107d-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d107d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d107d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d107d-138">CommonParameters</span></span>
<span data-ttu-id="d107d-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d107d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d107d-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d107d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d107d-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d107d-141">INPUTS</span></span>

### <span data-ttu-id="d107d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d107d-142">System.String</span></span>

### <span data-ttu-id="d107d-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="d107d-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="d107d-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d107d-144">OUTPUTS</span></span>

### <span data-ttu-id="d107d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d107d-145">System.Boolean</span></span>

## <span data-ttu-id="d107d-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d107d-146">NOTES</span></span>

## <span data-ttu-id="d107d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d107d-147">RELATED LINKS</span></span>
