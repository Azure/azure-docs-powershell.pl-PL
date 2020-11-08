---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062263"
---
# <span data-ttu-id="a9fe8-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="a9fe8-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="a9fe8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fe8-103">Usuwa krok.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-103">Deletes the step.</span></span>

## <span data-ttu-id="a9fe8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9fe8-104">SYNTAX</span></span>

### <span data-ttu-id="a9fe8-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a9fe8-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9fe8-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a9fe8-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9fe8-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9fe8-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9fe8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9fe8-108">DESCRIPTION</span></span>
<span data-ttu-id="a9fe8-109">Polecenie cmdlet **Remove-AzDeploymentManagerStep** umożliwia usunięcie kroku.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="a9fe8-110">Określ krok według jego nazwy i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="a9fe8-111">Alternatywnie możesz podać obiekt Step lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="a9fe8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9fe8-112">EXAMPLES</span></span>

### <span data-ttu-id="a9fe8-113">Przykład 1: Usuwanie kroku</span><span class="sxs-lookup"><span data-stu-id="a9fe8-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="a9fe8-114">To polecenie usuwa krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a9fe8-115">Przykład 2: Usuwanie kroku przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="a9fe8-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="a9fe8-116">To polecenie usuwa krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a9fe8-117">Przykład 3: Usuwanie kroku za pomocą obiektu zwróconego przez New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="a9fe8-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="a9fe8-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9fe8-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="a9fe8-119">To polecenie usuwa krok, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $stepObject.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="a9fe8-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9fe8-120">PARAMETERS</span></span>

### <span data-ttu-id="a9fe8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe8-121">-DefaultProfile</span></span>
<span data-ttu-id="a9fe8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9fe8-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9fe8-123">-InputObject</span></span>
<span data-ttu-id="a9fe8-124">Krok, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-124">The step to be removed.</span></span>

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

### <span data-ttu-id="a9fe8-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9fe8-125">-Name</span></span>
<span data-ttu-id="a9fe8-126">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-126">The name of the step.</span></span>

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

### <span data-ttu-id="a9fe8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9fe8-127">-PassThru</span></span>
<span data-ttu-id="a9fe8-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a9fe8-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a9fe8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fe8-129">-ResourceGroupName</span></span>
<span data-ttu-id="a9fe8-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-130">The resource group.</span></span>

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

### <span data-ttu-id="a9fe8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9fe8-131">-ResourceId</span></span>
<span data-ttu-id="a9fe8-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-132">The resource identifier.</span></span>

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

### <span data-ttu-id="a9fe8-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9fe8-133">-Confirm</span></span>
<span data-ttu-id="a9fe8-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9fe8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9fe8-135">-WhatIf</span></span>
<span data-ttu-id="a9fe8-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9fe8-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9fe8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fe8-138">CommonParameters</span></span>
<span data-ttu-id="a9fe8-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fe8-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9fe8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fe8-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9fe8-141">INPUTS</span></span>

### <span data-ttu-id="a9fe8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a9fe8-142">System.String</span></span>

### <span data-ttu-id="a9fe8-143">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="a9fe8-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="a9fe8-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9fe8-144">OUTPUTS</span></span>

### <span data-ttu-id="a9fe8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9fe8-145">System.Boolean</span></span>

## <span data-ttu-id="a9fe8-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9fe8-146">NOTES</span></span>

## <span data-ttu-id="a9fe8-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9fe8-147">RELATED LINKS</span></span>
