---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523853"
---
# <span data-ttu-id="d07a3-101">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d07a3-101">Restart-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="d07a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d07a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d07a3-103">Ponownie Rozpocznij wprowadzanie zakończone niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d07a3-103">Restart a failed rollout.</span></span>

## <span data-ttu-id="d07a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d07a3-104">SYNTAX</span></span>

### <span data-ttu-id="d07a3-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d07a3-105">Interactive (Default)</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07a3-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="d07a3-106">ResourceId</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d07a3-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d07a3-107">InputObject</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d07a3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d07a3-108">DESCRIPTION</span></span>
<span data-ttu-id="d07a3-109">Polecenie cmdlet **restart-AzureRmDeploymentManagerRollout** powoduje ponowne uruchomienie nieprawidłowego rozmieszczenia i zwraca obiekt reprezentujący to rozmieszczenie wraz ze wszystkimi szczegółowymi informacjami na temat postępu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d07a3-109">The **Restart-AzureRmDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="d07a3-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d07a3-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="d07a3-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d07a3-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="d07a3-112">Parametr opcjonalny SkipSucceeded umożliwia pominięcie wszystkich udanych kroków w poprzednim uruchomieniu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d07a3-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="d07a3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d07a3-113">EXAMPLES</span></span>

### <span data-ttu-id="d07a3-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d07a3-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="d07a3-115">To polecenie powoduje ponowne uruchomienie wdrożenia o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d07a3-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="d07a3-116">Flaga SkipSucceeded wskazuje, że wszystkie kroki, które zostały już pomyślnie wykonane, powinny zostać pominięte, a rozmieszczenie powinno być kontynuowane od miejsca, w którym nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="d07a3-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="d07a3-117">Przykład 2: ponowne wprowadzanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="d07a3-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="d07a3-118">To polecenie powoduje ponowne uruchomienie wdrożenia o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d07a3-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d07a3-119">Przykład 3: ponowne wprowadzanie rozmieszczenia przy użyciu obiektu rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="d07a3-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="d07a3-120">To polecenie powoduje ponowne uruchomienie wdrożenia, którego nazwa i przysourcename są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="d07a3-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="d07a3-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d07a3-121">PARAMETERS</span></span>

### <span data-ttu-id="d07a3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07a3-122">-DefaultProfile</span></span>
<span data-ttu-id="d07a3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d07a3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d07a3-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d07a3-124">-Name</span></span>
<span data-ttu-id="d07a3-125">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="d07a3-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="d07a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="d07a3-127">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="d07a3-127">The resource group.</span></span>

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

### <span data-ttu-id="d07a3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d07a3-128">-ResourceId</span></span>
<span data-ttu-id="d07a3-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d07a3-129">The resource identifier.</span></span>

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

### <span data-ttu-id="d07a3-130">— Wprowadzanie</span><span class="sxs-lookup"><span data-stu-id="d07a3-130">-Rollout</span></span>
<span data-ttu-id="d07a3-131">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d07a3-131">The resource to be removed.</span></span>

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

### <span data-ttu-id="d07a3-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="d07a3-132">-SkipSucceeded</span></span>
<span data-ttu-id="d07a3-133">Pomiń kroki, które powiodło się w poprzednim uruchomieniu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d07a3-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="d07a3-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d07a3-134">-Confirm</span></span>
<span data-ttu-id="d07a3-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d07a3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d07a3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d07a3-136">-WhatIf</span></span>
<span data-ttu-id="d07a3-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d07a3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d07a3-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d07a3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d07a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07a3-139">CommonParameters</span></span>
<span data-ttu-id="d07a3-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d07a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07a3-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d07a3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07a3-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d07a3-142">INPUTS</span></span>

### <span data-ttu-id="d07a3-143">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="d07a3-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="d07a3-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d07a3-144">OUTPUTS</span></span>

### <span data-ttu-id="d07a3-145">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="d07a3-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="d07a3-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d07a3-146">NOTES</span></span>

## <span data-ttu-id="d07a3-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d07a3-147">RELATED LINKS</span></span>

[<span data-ttu-id="d07a3-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d07a3-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="d07a3-149">Zatrzymaj — AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d07a3-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="d07a3-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d07a3-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)