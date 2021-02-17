---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194530"
---
# <span data-ttu-id="7cf0b-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7cf0b-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="7cf0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cf0b-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf0b-103">Ponowne uruchamianie nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="7cf0b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7cf0b-104">SYNTAX</span></span>

### <span data-ttu-id="7cf0b-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="7cf0b-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf0b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf0b-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cf0b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7cf0b-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf0b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7cf0b-108">DESCRIPTION</span></span>
<span data-ttu-id="7cf0b-109">Polecenie **cmdlet Restart-AzDeploymentManagerRollout** powoduje ponowne uruchomienie nieudanego uruchomienia i zwraca obiekt reprezentujący to rzutowanie ze wszystkimi szczegółowymi informacjami o postępie uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="7cf0b-110">Określ wycofanie według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7cf0b-111">Ewentualnie możesz podać obiekt Rollout lub Identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="7cf0b-112">Parametr opcjonalny SkipSucceed pozwala pominąć wszystkie kolejne kroki w poprzednim uruchomieniu uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="7cf0b-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7cf0b-113">EXAMPLES</span></span>

### <span data-ttu-id="7cf0b-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7cf0b-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="7cf0b-115">To polecenie powoduje ponowne uruchomienie zadania o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="7cf0b-116">Flaga SkipSucceed (Pomijanie) wskazuje, że wszystkie kroki, które już zostały ukończone pomyślnie, powinny zostać pominięte, a realizacja powinna być kontynuowana od miejsca, w którym ostatnio nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="7cf0b-117">Przykład 2. Ponowne uruchomienie uruchomienia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="7cf0b-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7cf0b-118">To polecenie powoduje ponowne uruchomienie uruchomienia o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7cf0b-119">Przykład 3. Ponowne uruchamianie przy użyciu obiektu rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="7cf0b-120">To polecenie powoduje ponowne uruchomienie uruchomienia, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $rolloutObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="7cf0b-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7cf0b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cf0b-121">PARAMETERS</span></span>

### <span data-ttu-id="7cf0b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf0b-122">-DefaultProfile</span></span>
<span data-ttu-id="7cf0b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf0b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cf0b-124">-InputObject</span></span>
<span data-ttu-id="7cf0b-125">Zasób do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="7cf0b-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7cf0b-126">-Name</span></span>
<span data-ttu-id="7cf0b-127">Nazwa tego rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="7cf0b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf0b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7cf0b-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-129">The resource group.</span></span>

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

### <span data-ttu-id="7cf0b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cf0b-130">-ResourceId</span></span>
<span data-ttu-id="7cf0b-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-131">The resource identifier.</span></span>

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

### <span data-ttu-id="7cf0b-132">- SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="7cf0b-132">-SkipSucceeded</span></span>
<span data-ttu-id="7cf0b-133">Pomiń kroki, które zakończyły się powodzeniem w poprzednim uruchomieniu procesu wycofywania.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="7cf0b-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cf0b-134">-Confirm</span></span>
<span data-ttu-id="7cf0b-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf0b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf0b-136">-WhatIf</span></span>
<span data-ttu-id="7cf0b-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf0b-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf0b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf0b-139">CommonParameters</span></span>
<span data-ttu-id="7cf0b-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf0b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf0b-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cf0b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf0b-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cf0b-142">INPUTS</span></span>

### <span data-ttu-id="7cf0b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7cf0b-143">System.String</span></span>

### <span data-ttu-id="7cf0b-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="7cf0b-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7cf0b-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cf0b-145">OUTPUTS</span></span>

### <span data-ttu-id="7cf0b-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="7cf0b-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7cf0b-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7cf0b-147">NOTES</span></span>

## <span data-ttu-id="7cf0b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cf0b-148">RELATED LINKS</span></span>
