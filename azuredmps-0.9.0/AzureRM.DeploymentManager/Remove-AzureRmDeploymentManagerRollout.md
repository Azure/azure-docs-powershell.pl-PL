---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523078"
---
# <span data-ttu-id="76aaa-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="76aaa-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="76aaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="76aaa-103">Usuwanie rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="76aaa-103">Deletes a rollout.</span></span>

## <span data-ttu-id="76aaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76aaa-104">SYNTAX</span></span>

### <span data-ttu-id="76aaa-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="76aaa-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76aaa-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="76aaa-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76aaa-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="76aaa-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76aaa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="76aaa-108">DESCRIPTION</span></span>
<span data-ttu-id="76aaa-109">Polecenie cmdlet **Remove-AzureRmDeploymentManagerRollout** usuwa rozmieszczenie w stanie terminalu.</span><span class="sxs-lookup"><span data-stu-id="76aaa-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="76aaa-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="76aaa-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="76aaa-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="76aaa-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="76aaa-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76aaa-112">EXAMPLES</span></span>

### <span data-ttu-id="76aaa-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76aaa-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="76aaa-114">To polecenie usuwa rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76aaa-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="76aaa-115">Przykład 2: usuwanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="76aaa-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="76aaa-116">To polecenie usuwa rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="76aaa-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="76aaa-117">Przykład 3: usuwanie rozmieszczenia przy użyciu obiektu rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="76aaa-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="76aaa-118">To polecenie powoduje usunięcie wdrożenia, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="76aaa-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="76aaa-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76aaa-119">PARAMETERS</span></span>

### <span data-ttu-id="76aaa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76aaa-120">-DefaultProfile</span></span>
<span data-ttu-id="76aaa-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76aaa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76aaa-122">-Force</span><span class="sxs-lookup"><span data-stu-id="76aaa-122">-Force</span></span>
<span data-ttu-id="76aaa-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76aaa-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="76aaa-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76aaa-124">-Name</span></span>
<span data-ttu-id="76aaa-125">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="76aaa-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="76aaa-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76aaa-126">-PassThru</span></span>
<span data-ttu-id="76aaa-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="76aaa-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="76aaa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76aaa-128">-ResourceGroupName</span></span>
<span data-ttu-id="76aaa-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="76aaa-129">The resource group.</span></span>

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

### <span data-ttu-id="76aaa-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76aaa-130">-ResourceId</span></span>
<span data-ttu-id="76aaa-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="76aaa-131">The resource identifier.</span></span>

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

### <span data-ttu-id="76aaa-132">— Wprowadzanie</span><span class="sxs-lookup"><span data-stu-id="76aaa-132">-Rollout</span></span>
<span data-ttu-id="76aaa-133">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="76aaa-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="76aaa-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76aaa-134">-Confirm</span></span>
<span data-ttu-id="76aaa-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76aaa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76aaa-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76aaa-136">-WhatIf</span></span>
<span data-ttu-id="76aaa-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76aaa-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76aaa-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76aaa-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76aaa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76aaa-139">CommonParameters</span></span>
<span data-ttu-id="76aaa-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76aaa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76aaa-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76aaa-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76aaa-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76aaa-142">INPUTS</span></span>

### <span data-ttu-id="76aaa-143">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="76aaa-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="76aaa-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76aaa-144">OUTPUTS</span></span>

### <span data-ttu-id="76aaa-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76aaa-145">System.Boolean</span></span>

## <span data-ttu-id="76aaa-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76aaa-146">NOTES</span></span>

## <span data-ttu-id="76aaa-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76aaa-147">RELATED LINKS</span></span>

[<span data-ttu-id="76aaa-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="76aaa-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="76aaa-149">Zatrzymaj — AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="76aaa-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="76aaa-150">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="76aaa-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)