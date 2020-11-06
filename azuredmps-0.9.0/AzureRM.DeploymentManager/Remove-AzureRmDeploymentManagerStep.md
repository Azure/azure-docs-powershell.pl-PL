---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523165"
---
# <span data-ttu-id="19677-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="19677-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="19677-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19677-102">SYNOPSIS</span></span>
<span data-ttu-id="19677-103">Usuwa krok.</span><span class="sxs-lookup"><span data-stu-id="19677-103">Deletes a step.</span></span>

## <span data-ttu-id="19677-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19677-104">SYNTAX</span></span>

### <span data-ttu-id="19677-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="19677-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19677-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="19677-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19677-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="19677-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19677-108">Opis</span><span class="sxs-lookup"><span data-stu-id="19677-108">DESCRIPTION</span></span>
<span data-ttu-id="19677-109">Polecenie cmdlet **Remove-AzureRmDeploymentManagerStep** umożliwia usunięcie kroku.</span><span class="sxs-lookup"><span data-stu-id="19677-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="19677-110">Określ krok według jego nazwy i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="19677-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="19677-111">Alternatywnie możesz podać obiekt Step lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="19677-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="19677-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19677-112">EXAMPLES</span></span>
### <span data-ttu-id="19677-113">Przykład 1: Usuwanie kroku</span><span class="sxs-lookup"><span data-stu-id="19677-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="19677-114">To polecenie usuwa krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19677-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="19677-115">Przykład 2: Usuwanie kroku przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="19677-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="19677-116">To polecenie usuwa krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19677-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="19677-117">Przykład 3: Usuwanie kroku za pomocą obiektu zwróconego przez New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="19677-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="19677-118">To polecenie usuwa krok, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $stepObject.</span><span class="sxs-lookup"><span data-stu-id="19677-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="19677-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19677-119">PARAMETERS</span></span>

### <span data-ttu-id="19677-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19677-120">-DefaultProfile</span></span>
<span data-ttu-id="19677-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19677-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19677-122">-Force</span><span class="sxs-lookup"><span data-stu-id="19677-122">-Force</span></span>
<span data-ttu-id="19677-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="19677-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="19677-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19677-124">-Name</span></span>
<span data-ttu-id="19677-125">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="19677-125">The name of the step.</span></span>

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

### <span data-ttu-id="19677-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19677-126">-PassThru</span></span>
<span data-ttu-id="19677-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="19677-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="19677-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19677-128">-ResourceGroupName</span></span>
<span data-ttu-id="19677-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="19677-129">The resource group.</span></span>

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

### <span data-ttu-id="19677-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19677-130">-ResourceId</span></span>
<span data-ttu-id="19677-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="19677-131">The resource identifier.</span></span>

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

### <span data-ttu-id="19677-132">-Krok</span><span class="sxs-lookup"><span data-stu-id="19677-132">-Step</span></span>
<span data-ttu-id="19677-133">Krok, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="19677-133">The step to be removed.</span></span>

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

### <span data-ttu-id="19677-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19677-134">-Confirm</span></span>
<span data-ttu-id="19677-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19677-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19677-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19677-136">-WhatIf</span></span>
<span data-ttu-id="19677-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19677-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19677-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19677-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19677-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19677-139">CommonParameters</span></span>
<span data-ttu-id="19677-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19677-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="19677-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19677-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19677-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19677-142">INPUTS</span></span>

### <span data-ttu-id="19677-143">System. String</span><span class="sxs-lookup"><span data-stu-id="19677-143">System.String</span></span>

### <span data-ttu-id="19677-144">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="19677-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="19677-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19677-145">OUTPUTS</span></span>

### <span data-ttu-id="19677-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19677-146">System.Boolean</span></span>

## <span data-ttu-id="19677-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19677-147">NOTES</span></span>

## <span data-ttu-id="19677-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19677-148">RELATED LINKS</span></span>
