---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 5bf59cb766d82e2fc50bdc75c0a072e2b8d17a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966346"
---
# <span data-ttu-id="f36c7-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f36c7-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f36c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f36c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f36c7-103">Robi krok.</span><span class="sxs-lookup"><span data-stu-id="f36c7-103">Gets the step.</span></span>

## <span data-ttu-id="f36c7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f36c7-104">SYNTAX</span></span>

### <span data-ttu-id="f36c7-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f36c7-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f36c7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f36c7-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f36c7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f36c7-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f36c7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f36c7-108">DESCRIPTION</span></span>
<span data-ttu-id="f36c7-109">Polecenie **cmdlet Get-AzDeploymentManagerStep** pobiera krok i zwraca obiekt reprezentujący ten krok.</span><span class="sxs-lookup"><span data-stu-id="f36c7-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="f36c7-110">Określ krok według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f36c7-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="f36c7-111">Ewentualnie możesz podać obiekt Step lub Identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="f36c7-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="f36c7-112">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do źródła artefaktu za pomocą Set-AzDeploymentManagerStep cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f36c7-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="f36c7-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f36c7-113">EXAMPLES</span></span>

### <span data-ttu-id="f36c7-114">Przykład 1. Uzyskiwanie kroku</span><span class="sxs-lookup"><span data-stu-id="f36c7-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="f36c7-115">To polecenie pobiera krok o nazwie ContosoService1WaitStep w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f36c7-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f36c7-116">Przykład 2. Uzyskiwanie kroku za pomocą identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="f36c7-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="f36c7-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f36c7-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="f36c7-118">To polecenie pobiera krok o nazwie ContosoService1WaitStep w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f36c7-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f36c7-119">Przykład 3. Uzyskiwanie kroku przy użyciu obiektu zwróconego przez New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f36c7-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="f36c7-120">To polecenie pobiera etap, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $stepObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="f36c7-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="f36c7-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f36c7-121">PARAMETERS</span></span>

### <span data-ttu-id="f36c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36c7-122">-DefaultProfile</span></span>
<span data-ttu-id="f36c7-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f36c7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f36c7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f36c7-124">-InputObject</span></span>
<span data-ttu-id="f36c7-125">Obiekt zasobu kroku.</span><span class="sxs-lookup"><span data-stu-id="f36c7-125">The step resource object.</span></span>

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

### <span data-ttu-id="f36c7-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f36c7-126">-Name</span></span>
<span data-ttu-id="f36c7-127">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="f36c7-127">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36c7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36c7-128">-ResourceGroupName</span></span>
<span data-ttu-id="f36c7-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="f36c7-129">The resource group.</span></span>

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

### <span data-ttu-id="f36c7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f36c7-130">-ResourceId</span></span>
<span data-ttu-id="f36c7-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="f36c7-131">The resource identifier.</span></span>

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

### <span data-ttu-id="f36c7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36c7-132">CommonParameters</span></span>
<span data-ttu-id="f36c7-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f36c7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36c7-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f36c7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36c7-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f36c7-135">INPUTS</span></span>

### <span data-ttu-id="f36c7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f36c7-136">System.String</span></span>

### <span data-ttu-id="f36c7-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f36c7-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f36c7-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f36c7-138">OUTPUTS</span></span>

### <span data-ttu-id="f36c7-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f36c7-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f36c7-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f36c7-140">NOTES</span></span>

## <span data-ttu-id="f36c7-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f36c7-141">RELATED LINKS</span></span>
