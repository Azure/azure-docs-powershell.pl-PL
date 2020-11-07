---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/stop-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 3c4f221fc00187c4faea2dbcc1a5014822c476c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710670"
---
# <span data-ttu-id="2d586-101">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="2d586-101">Stop-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="2d586-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d586-102">SYNOPSIS</span></span>
<span data-ttu-id="2d586-103">Zatrzymuje trwające wprowadzanie.</span><span class="sxs-lookup"><span data-stu-id="2d586-103">Stops a rollout in progress.</span></span>

## <span data-ttu-id="2d586-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d586-104">SYNTAX</span></span>

### <span data-ttu-id="2d586-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2d586-105">Interactive (Default)</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d586-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2d586-106">ResourceId</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d586-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="2d586-107">InputObject</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d586-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2d586-108">DESCRIPTION</span></span>
<span data-ttu-id="2d586-109">Polecenie cmdlet **stop-AzureRmDeploymentManagerRollout** zatrzymuje wprowadzanie w toku i zwraca obiekt reprezentujący bieżący stan wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="2d586-109">The **Stop-AzureRmDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="2d586-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d586-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="2d586-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2d586-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="2d586-112">Pamiętaj, że po zatrzymaniu rozmieszczenia nie można go wznowić ani uruchomić ponownie.</span><span class="sxs-lookup"><span data-stu-id="2d586-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="2d586-113">Można utworzyć tylko nowe rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="2d586-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="2d586-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d586-114">EXAMPLES</span></span>

### <span data-ttu-id="2d586-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d586-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="2d586-116">To polecenie zatrzymuje wprowadzanie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2d586-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="2d586-117">Przykład 2: zatrzymywanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="2d586-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="2d586-118">To polecenie zatrzymuje wprowadzanie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2d586-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2d586-119">Przykład 3: zatrzymywanie rozmieszczenia przy użyciu obiektu rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="2d586-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="2d586-120">To polecenie zatrzymuje wprowadzanie, których nazwa i przyciąganie źródłowe są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="2d586-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="2d586-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d586-121">PARAMETERS</span></span>

### <span data-ttu-id="2d586-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d586-122">-DefaultProfile</span></span>
<span data-ttu-id="2d586-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d586-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d586-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2d586-124">-Force</span></span>
<span data-ttu-id="2d586-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2d586-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2d586-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d586-126">-Name</span></span>
<span data-ttu-id="2d586-127">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="2d586-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="2d586-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d586-128">-ResourceGroupName</span></span>
<span data-ttu-id="2d586-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d586-129">The resource group.</span></span>

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

### <span data-ttu-id="2d586-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d586-130">-ResourceId</span></span>
<span data-ttu-id="2d586-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2d586-131">The resource identifier.</span></span>

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

### <span data-ttu-id="2d586-132">— Wprowadzanie</span><span class="sxs-lookup"><span data-stu-id="2d586-132">-Rollout</span></span>
<span data-ttu-id="2d586-133">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="2d586-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="2d586-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d586-134">-Confirm</span></span>
<span data-ttu-id="2d586-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d586-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d586-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d586-136">-WhatIf</span></span>
<span data-ttu-id="2d586-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d586-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d586-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2d586-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d586-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d586-139">CommonParameters</span></span>
<span data-ttu-id="2d586-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d586-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d586-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d586-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d586-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d586-142">INPUTS</span></span>

### <span data-ttu-id="2d586-143">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="2d586-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="2d586-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d586-144">OUTPUTS</span></span>

### <span data-ttu-id="2d586-145">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="2d586-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="2d586-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d586-146">NOTES</span></span>

## <span data-ttu-id="2d586-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d586-147">RELATED LINKS</span></span>

[<span data-ttu-id="2d586-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="2d586-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="2d586-149">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="2d586-149">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="2d586-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="2d586-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)