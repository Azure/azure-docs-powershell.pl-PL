---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: 53458d53dd6d8b3f698dc51fc6b1463c9a9134e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966362"
---
# <span data-ttu-id="a1e58-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="a1e58-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="a1e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1e58-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e58-103">Pobiera rozmówienie.</span><span class="sxs-lookup"><span data-stu-id="a1e58-103">Gets the rollout.</span></span>

## <span data-ttu-id="a1e58-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1e58-104">SYNTAX</span></span>

### <span data-ttu-id="a1e58-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a1e58-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1e58-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e58-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1e58-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a1e58-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1e58-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1e58-108">DESCRIPTION</span></span>
<span data-ttu-id="a1e58-109">Polecenie **cmdlet Get-AzDeploymentManagerRollout** pobiera rzutowanie i zwraca obiekt reprezentujący to rzutowanie ze wszystkimi szczegółowymi informacjami o postępie tego rzutowania.</span><span class="sxs-lookup"><span data-stu-id="a1e58-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="a1e58-110">Określ wycofanie według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1e58-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="a1e58-111">Ewentualnie możesz podać obiekt Rollout lub Identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="a1e58-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="a1e58-112">Zwrócony obiekt wdrażania zawiera usługi, jednostki usługi i kroki, które zostały wdrożone, oraz te, które są w toku.</span><span class="sxs-lookup"><span data-stu-id="a1e58-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="a1e58-113">Te, które jeszcze nie zostaną wdrożone, nie są w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="a1e58-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="a1e58-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1e58-114">EXAMPLES</span></span>

### <span data-ttu-id="a1e58-115">Przykład 1. Uzyskiwanie tego rozsyłania</span><span class="sxs-lookup"><span data-stu-id="a1e58-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="a1e58-116">To polecenie pobiera wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a1e58-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="a1e58-117">Przykład 2. Uzyskiwanie i wyświetlanie szczegółów dotyczących wycofywania</span><span class="sxs-lookup"><span data-stu-id="a1e58-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="a1e58-118">To polecenie pobiera wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a1e58-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="a1e58-119">Przełącznik -Verbose wyświetla wszystkie szczegóły dotyczące rzutowania hierarchicznie; wyświetlając usługi, jednostki ServiceUnits oraz kroki w ramach poszczególnych jednostek ServiceUnit oraz informacje kontekstowe dla każdego kroku w widoku infektowania.</span><span class="sxs-lookup"><span data-stu-id="a1e58-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="a1e58-120">Przykład 3. Uzyskiwanie wycofywania przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="a1e58-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="a1e58-121">To polecenie pobiera wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a1e58-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a1e58-122">Przykład 4. Uzyskiwanie rzutowania przy użyciu obiektu rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="a1e58-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="a1e58-123">To polecenie pobiera rzutowanie, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $rolloutObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="a1e58-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="a1e58-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1e58-124">PARAMETERS</span></span>

### <span data-ttu-id="a1e58-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e58-125">-DefaultProfile</span></span>
<span data-ttu-id="a1e58-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e58-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1e58-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1e58-127">-InputObject</span></span>
<span data-ttu-id="a1e58-128">Obiekt Rollout.</span><span class="sxs-lookup"><span data-stu-id="a1e58-128">Rollout object.</span></span>

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

### <span data-ttu-id="a1e58-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a1e58-129">-Name</span></span>
<span data-ttu-id="a1e58-130">Nazwa tego rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="a1e58-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="a1e58-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e58-131">-ResourceGroupName</span></span>
<span data-ttu-id="a1e58-132">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1e58-132">The resource group.</span></span>

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

### <span data-ttu-id="a1e58-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e58-133">-ResourceId</span></span>
<span data-ttu-id="a1e58-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="a1e58-134">The resource identifier.</span></span>

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

### <span data-ttu-id="a1e58-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="a1e58-135">-RetryAttempt</span></span>
<span data-ttu-id="a1e58-136">Ponowna próba wykonania.</span><span class="sxs-lookup"><span data-stu-id="a1e58-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1e58-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e58-137">CommonParameters</span></span>
<span data-ttu-id="a1e58-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e58-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e58-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1e58-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e58-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1e58-140">INPUTS</span></span>

### <span data-ttu-id="a1e58-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a1e58-141">System.String</span></span>

### <span data-ttu-id="a1e58-142">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a1e58-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a1e58-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="a1e58-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="a1e58-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1e58-144">OUTPUTS</span></span>

### <span data-ttu-id="a1e58-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="a1e58-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="a1e58-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1e58-146">NOTES</span></span>

## <span data-ttu-id="a1e58-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1e58-147">RELATED LINKS</span></span>
