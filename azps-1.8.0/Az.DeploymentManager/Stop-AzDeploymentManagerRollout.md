---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: d68ca0e13c279e58715b57ae73a2c8e2f4f30d8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709932"
---
# <span data-ttu-id="e9758-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="e9758-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="e9758-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9758-102">SYNOPSIS</span></span>
<span data-ttu-id="e9758-103">Zatrzymuje wprowadzanie.</span><span class="sxs-lookup"><span data-stu-id="e9758-103">Stops the rollout.</span></span>

## <span data-ttu-id="e9758-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9758-104">SYNTAX</span></span>

### <span data-ttu-id="e9758-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e9758-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9758-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e9758-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9758-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="e9758-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9758-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e9758-108">DESCRIPTION</span></span>
<span data-ttu-id="e9758-109">Polecenie cmdlet **stop-AzDeploymentManagerRollout** zatrzymuje wprowadzanie w toku i zwraca obiekt reprezentujący bieżący stan wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e9758-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="e9758-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e9758-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="e9758-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e9758-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="e9758-112">Pamiętaj, że po zatrzymaniu rozmieszczenia nie można go wznowić ani uruchomić ponownie.</span><span class="sxs-lookup"><span data-stu-id="e9758-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="e9758-113">Można utworzyć tylko nowe rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="e9758-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="e9758-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9758-114">EXAMPLES</span></span>

### <span data-ttu-id="e9758-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e9758-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="e9758-116">To polecenie zatrzymuje wprowadzanie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e9758-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="e9758-117">Przykład 2: zatrzymywanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="e9758-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="e9758-118">To polecenie zatrzymuje wprowadzanie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e9758-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e9758-119">Przykład 3: zatrzymywanie rozmieszczenia przy użyciu obiektu rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="e9758-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="e9758-120">To polecenie zatrzymuje wprowadzanie, których nazwa i przyciąganie źródłowe są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="e9758-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="e9758-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9758-121">PARAMETERS</span></span>

### <span data-ttu-id="e9758-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9758-122">-DefaultProfile</span></span>
<span data-ttu-id="e9758-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9758-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9758-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e9758-124">-Force</span></span>
<span data-ttu-id="e9758-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e9758-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e9758-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e9758-126">-InputObject</span></span>
<span data-ttu-id="e9758-127">Rozszerzenie, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="e9758-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="e9758-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9758-128">-Name</span></span>
<span data-ttu-id="e9758-129">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="e9758-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="e9758-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9758-130">-ResourceGroupName</span></span>
<span data-ttu-id="e9758-131">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="e9758-131">The resource group.</span></span>

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

### <span data-ttu-id="e9758-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9758-132">-ResourceId</span></span>
<span data-ttu-id="e9758-133">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e9758-133">The resource identifier.</span></span>

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

### <span data-ttu-id="e9758-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9758-134">-Confirm</span></span>
<span data-ttu-id="e9758-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9758-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9758-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9758-136">-WhatIf</span></span>
<span data-ttu-id="e9758-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9758-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9758-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9758-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9758-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9758-139">CommonParameters</span></span>
<span data-ttu-id="e9758-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9758-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9758-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9758-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9758-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9758-142">INPUTS</span></span>

### <span data-ttu-id="e9758-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e9758-143">System.String</span></span>

### <span data-ttu-id="e9758-144">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="e9758-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e9758-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9758-145">OUTPUTS</span></span>

### <span data-ttu-id="e9758-146">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="e9758-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e9758-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9758-147">NOTES</span></span>

## <span data-ttu-id="e9758-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9758-148">RELATED LINKS</span></span>