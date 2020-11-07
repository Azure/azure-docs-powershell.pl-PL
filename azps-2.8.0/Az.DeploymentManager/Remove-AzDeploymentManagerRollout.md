---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 066026331fa43af06fc2e3314ccb97d06a0f9b50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705615"
---
# <span data-ttu-id="e81e0-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="e81e0-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="e81e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e81e0-102">SYNOPSIS</span></span>
<span data-ttu-id="e81e0-103">Umożliwia usunięcie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e81e0-103">Deletes the rollout.</span></span>

## <span data-ttu-id="e81e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e81e0-104">SYNTAX</span></span>

### <span data-ttu-id="e81e0-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e81e0-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e81e0-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e81e0-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e81e0-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="e81e0-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e81e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e81e0-108">DESCRIPTION</span></span>
<span data-ttu-id="e81e0-109">Polecenie cmdlet **Remove-AzDeploymentManagerRollout** usuwa rozmieszczenie w stanie terminalu.</span><span class="sxs-lookup"><span data-stu-id="e81e0-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="e81e0-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e81e0-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="e81e0-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e81e0-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="e81e0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e81e0-112">EXAMPLES</span></span>

### <span data-ttu-id="e81e0-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e81e0-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="e81e0-114">To polecenie usuwa rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e81e0-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e81e0-115">Przykład 2: usuwanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="e81e0-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="e81e0-116">To polecenie usuwa rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e81e0-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e81e0-117">Przykład 3: usuwanie rozmieszczenia przy użyciu obiektu rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="e81e0-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="e81e0-118">To polecenie powoduje usunięcie wdrożenia, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="e81e0-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="e81e0-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e81e0-119">PARAMETERS</span></span>

### <span data-ttu-id="e81e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81e0-120">-DefaultProfile</span></span>
<span data-ttu-id="e81e0-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e81e0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e81e0-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e81e0-122">-InputObject</span></span>
<span data-ttu-id="e81e0-123">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e81e0-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="e81e0-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e81e0-124">-Name</span></span>
<span data-ttu-id="e81e0-125">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="e81e0-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="e81e0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e81e0-126">-PassThru</span></span>
<span data-ttu-id="e81e0-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e81e0-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e81e0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e81e0-128">-ResourceGroupName</span></span>
<span data-ttu-id="e81e0-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="e81e0-129">The resource group.</span></span>

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

### <span data-ttu-id="e81e0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e81e0-130">-ResourceId</span></span>
<span data-ttu-id="e81e0-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e81e0-131">The resource identifier.</span></span>

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

### <span data-ttu-id="e81e0-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e81e0-132">-Confirm</span></span>
<span data-ttu-id="e81e0-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81e0-134">-WhatIf</span></span>
<span data-ttu-id="e81e0-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81e0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e81e0-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e81e0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e81e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81e0-137">CommonParameters</span></span>
<span data-ttu-id="e81e0-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81e0-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e81e0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81e0-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e81e0-140">INPUTS</span></span>

### <span data-ttu-id="e81e0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e81e0-141">System.String</span></span>

### <span data-ttu-id="e81e0-142">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="e81e0-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e81e0-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e81e0-143">OUTPUTS</span></span>

### <span data-ttu-id="e81e0-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e81e0-144">System.Boolean</span></span>

## <span data-ttu-id="e81e0-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e81e0-145">NOTES</span></span>

## <span data-ttu-id="e81e0-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e81e0-146">RELATED LINKS</span></span>
