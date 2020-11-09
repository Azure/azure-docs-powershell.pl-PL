---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304914"
---
# <span data-ttu-id="21b70-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="21b70-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="21b70-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21b70-102">SYNOPSIS</span></span>
<span data-ttu-id="21b70-103">Ponowne rozmieszczenie zakończone niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="21b70-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="21b70-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21b70-104">SYNTAX</span></span>

### <span data-ttu-id="21b70-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="21b70-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21b70-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="21b70-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21b70-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="21b70-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21b70-108">Opis</span><span class="sxs-lookup"><span data-stu-id="21b70-108">DESCRIPTION</span></span>
<span data-ttu-id="21b70-109">Polecenie cmdlet **restart-AzDeploymentManagerRollout** powoduje ponowne uruchomienie nieprawidłowego rozmieszczenia i zwraca obiekt reprezentujący to rozmieszczenie wraz ze wszystkimi szczegółowymi informacjami na temat postępu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="21b70-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="21b70-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21b70-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="21b70-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="21b70-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="21b70-112">Parametr opcjonalny SkipSucceeded umożliwia pominięcie wszystkich udanych kroków w poprzednim uruchomieniu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="21b70-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="21b70-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21b70-113">EXAMPLES</span></span>

### <span data-ttu-id="21b70-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21b70-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="21b70-115">To polecenie powoduje ponowne uruchomienie wdrożenia o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="21b70-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="21b70-116">Flaga SkipSucceeded wskazuje, że wszystkie kroki, które zostały już pomyślnie wykonane, powinny zostać pominięte, a rozmieszczenie powinno być kontynuowane od miejsca, w którym nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="21b70-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="21b70-117">Przykład 2: ponowne wprowadzanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="21b70-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="21b70-118">To polecenie powoduje ponowne uruchomienie wdrożenia o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="21b70-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="21b70-119">Przykład 3: ponowne wprowadzanie rozmieszczenia przy użyciu obiektu rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="21b70-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="21b70-120">To polecenie powoduje ponowne uruchomienie wdrożenia, którego nazwa i przysourcename są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="21b70-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="21b70-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21b70-121">PARAMETERS</span></span>

### <span data-ttu-id="21b70-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b70-122">-DefaultProfile</span></span>
<span data-ttu-id="21b70-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21b70-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21b70-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21b70-124">-InputObject</span></span>
<span data-ttu-id="21b70-125">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="21b70-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="21b70-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21b70-126">-Name</span></span>
<span data-ttu-id="21b70-127">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="21b70-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="21b70-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21b70-128">-ResourceGroupName</span></span>
<span data-ttu-id="21b70-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="21b70-129">The resource group.</span></span>

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

### <span data-ttu-id="21b70-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21b70-130">-ResourceId</span></span>
<span data-ttu-id="21b70-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="21b70-131">The resource identifier.</span></span>

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

### <span data-ttu-id="21b70-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="21b70-132">-SkipSucceeded</span></span>
<span data-ttu-id="21b70-133">Pomiń kroki, które powiodło się w poprzednim uruchomieniu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="21b70-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="21b70-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21b70-134">-Confirm</span></span>
<span data-ttu-id="21b70-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21b70-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21b70-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21b70-136">-WhatIf</span></span>
<span data-ttu-id="21b70-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21b70-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21b70-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21b70-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21b70-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b70-139">CommonParameters</span></span>
<span data-ttu-id="21b70-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21b70-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b70-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21b70-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b70-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21b70-142">INPUTS</span></span>

### <span data-ttu-id="21b70-143">System. String</span><span class="sxs-lookup"><span data-stu-id="21b70-143">System.String</span></span>

### <span data-ttu-id="21b70-144">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="21b70-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="21b70-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21b70-145">OUTPUTS</span></span>

### <span data-ttu-id="21b70-146">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="21b70-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="21b70-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21b70-147">NOTES</span></span>

## <span data-ttu-id="21b70-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21b70-148">RELATED LINKS</span></span>
