---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: f053adcd90b013df6f1678ed6468b2efa26d3ff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962081"
---
# <span data-ttu-id="aa2d3-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="aa2d3-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="aa2d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2d3-103">Zatrzymuje rozsyłanie.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-103">Stops the rollout.</span></span>

## <span data-ttu-id="aa2d3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa2d3-104">SYNTAX</span></span>

### <span data-ttu-id="aa2d3-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="aa2d3-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa2d3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa2d3-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa2d3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="aa2d3-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa2d3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa2d3-108">DESCRIPTION</span></span>
<span data-ttu-id="aa2d3-109">Polecenie **cmdlet Stop-AzDeploymentManagerRollout** zatrzymuje w toku wycofywanie i zwraca obiekt, który reprezentuje bieżący stan tego rzutowania.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="aa2d3-110">Określ wycofanie według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="aa2d3-111">Ewentualnie możesz podać obiekt Rollout lub Identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="aa2d3-112">Pamiętaj, że po zatrzymaniu wycofywania nie można wznowić jego działania ani wznowić go ponownie.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="aa2d3-113">Możesz utworzyć tylko nowe rzutnie.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="aa2d3-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa2d3-114">EXAMPLES</span></span>

### <span data-ttu-id="aa2d3-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa2d3-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="aa2d3-116">To polecenie zatrzymuje wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="aa2d3-117">Przykład 2. Zatrzymanie wycofywania przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="aa2d3-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="aa2d3-118">To polecenie zatrzymuje wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="aa2d3-119">Przykład 3. Zatrzymanie rzutowania przy użyciu obiektu rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="aa2d3-120">To polecenie zatrzymuje rzutowanie, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $rolloutObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="aa2d3-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="aa2d3-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa2d3-121">PARAMETERS</span></span>

### <span data-ttu-id="aa2d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2d3-122">-DefaultProfile</span></span>
<span data-ttu-id="aa2d3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa2d3-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="aa2d3-124">-Force</span></span>
<span data-ttu-id="aa2d3-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="aa2d3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa2d3-126">-InputObject</span></span>
<span data-ttu-id="aa2d3-127">The rollout to be removed.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="aa2d3-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aa2d3-128">-Name</span></span>
<span data-ttu-id="aa2d3-129">Nazwa tego rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="aa2d3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2d3-130">-ResourceGroupName</span></span>
<span data-ttu-id="aa2d3-131">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-131">The resource group.</span></span>

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

### <span data-ttu-id="aa2d3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa2d3-132">-ResourceId</span></span>
<span data-ttu-id="aa2d3-133">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-133">The resource identifier.</span></span>

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

### <span data-ttu-id="aa2d3-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa2d3-134">-Confirm</span></span>
<span data-ttu-id="aa2d3-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa2d3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa2d3-136">-WhatIf</span></span>
<span data-ttu-id="aa2d3-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa2d3-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa2d3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2d3-139">CommonParameters</span></span>
<span data-ttu-id="aa2d3-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa2d3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2d3-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa2d3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2d3-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa2d3-142">INPUTS</span></span>

### <span data-ttu-id="aa2d3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="aa2d3-143">System.String</span></span>

### <span data-ttu-id="aa2d3-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="aa2d3-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="aa2d3-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa2d3-145">OUTPUTS</span></span>

### <span data-ttu-id="aa2d3-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="aa2d3-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="aa2d3-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa2d3-147">NOTES</span></span>

## <span data-ttu-id="aa2d3-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa2d3-148">RELATED LINKS</span></span>
