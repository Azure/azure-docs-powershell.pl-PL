---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062267"
---
# <span data-ttu-id="faded-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="faded-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="faded-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="faded-102">SYNOPSIS</span></span>
<span data-ttu-id="faded-103">Umożliwia usunięcie wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="faded-103">Deletes the rollout.</span></span>

## <span data-ttu-id="faded-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="faded-104">SYNTAX</span></span>

### <span data-ttu-id="faded-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="faded-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faded-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="faded-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faded-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="faded-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faded-108">Opis</span><span class="sxs-lookup"><span data-stu-id="faded-108">DESCRIPTION</span></span>
<span data-ttu-id="faded-109">Polecenie cmdlet **Remove-AzDeploymentManagerRollout** usuwa rozmieszczenie w stanie terminalu.</span><span class="sxs-lookup"><span data-stu-id="faded-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="faded-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="faded-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="faded-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="faded-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="faded-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="faded-112">EXAMPLES</span></span>

### <span data-ttu-id="faded-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="faded-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="faded-114">To polecenie usuwa rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="faded-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="faded-115">Przykład 2: usuwanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="faded-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="faded-116">To polecenie usuwa rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="faded-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="faded-117">Przykład 3: usuwanie rozmieszczenia przy użyciu obiektu rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="faded-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="faded-118">To polecenie powoduje usunięcie wdrożenia, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="faded-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="faded-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="faded-119">PARAMETERS</span></span>

### <span data-ttu-id="faded-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faded-120">-DefaultProfile</span></span>
<span data-ttu-id="faded-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="faded-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faded-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="faded-122">-InputObject</span></span>
<span data-ttu-id="faded-123">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="faded-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="faded-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="faded-124">-Name</span></span>
<span data-ttu-id="faded-125">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="faded-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="faded-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="faded-126">-PassThru</span></span>
<span data-ttu-id="faded-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="faded-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="faded-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faded-128">-ResourceGroupName</span></span>
<span data-ttu-id="faded-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="faded-129">The resource group.</span></span>

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

### <span data-ttu-id="faded-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="faded-130">-ResourceId</span></span>
<span data-ttu-id="faded-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="faded-131">The resource identifier.</span></span>

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

### <span data-ttu-id="faded-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="faded-132">-Confirm</span></span>
<span data-ttu-id="faded-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faded-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faded-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faded-134">-WhatIf</span></span>
<span data-ttu-id="faded-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faded-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faded-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="faded-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faded-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faded-137">CommonParameters</span></span>
<span data-ttu-id="faded-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faded-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faded-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faded-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faded-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="faded-140">INPUTS</span></span>

### <span data-ttu-id="faded-141">System. String</span><span class="sxs-lookup"><span data-stu-id="faded-141">System.String</span></span>

### <span data-ttu-id="faded-142">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="faded-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="faded-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="faded-143">OUTPUTS</span></span>

### <span data-ttu-id="faded-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="faded-144">System.Boolean</span></span>

## <span data-ttu-id="faded-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="faded-145">NOTES</span></span>

## <span data-ttu-id="faded-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="faded-146">RELATED LINKS</span></span>
