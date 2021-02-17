---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198018"
---
# <span data-ttu-id="ae9c2-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ae9c2-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="ae9c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae9c2-103">Pobiera rozmówienie.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-103">Gets the rollout.</span></span>

## <span data-ttu-id="ae9c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae9c2-104">SYNTAX</span></span>

### <span data-ttu-id="ae9c2-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ae9c2-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae9c2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae9c2-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae9c2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae9c2-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae9c2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae9c2-108">DESCRIPTION</span></span>
<span data-ttu-id="ae9c2-109">Polecenie **cmdlet Get-AzDeploymentManagerRollout** pobiera rzutowanie i zwraca obiekt reprezentujący to rzutowanie ze wszystkimi szczegółowymi informacjami o postępie tego rzutowania.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="ae9c2-110">Określ wycofanie według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ae9c2-111">Ewentualnie możesz podać obiekt Rollout lub Identyfikator Zasobu.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="ae9c2-112">Zwrócony obiekt wdrażania zawiera usługi, jednostki usługi i kroki, które zostały wdrożone, oraz te, które są w toku.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="ae9c2-113">Te, które jeszcze nie zostaną wdrożone, nie są w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="ae9c2-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae9c2-114">EXAMPLES</span></span>

### <span data-ttu-id="ae9c2-115">Przykład 1. Uzyskiwanie rozłożenia</span><span class="sxs-lookup"><span data-stu-id="ae9c2-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="ae9c2-116">To polecenie pobiera wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="ae9c2-117">Przykład 2. Uzyskiwanie i wyświetlanie szczegółów dotyczących rzutowania</span><span class="sxs-lookup"><span data-stu-id="ae9c2-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="ae9c2-118">To polecenie pobiera wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="ae9c2-119">Przełącznik -Verbose wyświetla wszystkie szczegóły dotyczące rzutowania hierarchicznie; wyświetlając usługi, jednostki ServiceUnits oraz kroki w ramach poszczególnych jednostek ServiceUnit oraz informacje kontekstowe dla każdego kroku w widoku infektowania.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="ae9c2-120">Przykład 3. Uzyskiwanie wycofywania przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="ae9c2-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ae9c2-121">To polecenie pobiera wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ae9c2-122">Przykład 4. Uzyskiwanie rzutowania przy użyciu obiektu rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="ae9c2-123">To polecenie pobiera rzutowanie, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $rolloutObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="ae9c2-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ae9c2-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae9c2-124">PARAMETERS</span></span>

### <span data-ttu-id="ae9c2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae9c2-125">-DefaultProfile</span></span>
<span data-ttu-id="ae9c2-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae9c2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae9c2-127">-InputObject</span></span>
<span data-ttu-id="ae9c2-128">Obiekt Rollout.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-128">Rollout object.</span></span>

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

### <span data-ttu-id="ae9c2-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae9c2-129">-Name</span></span>
<span data-ttu-id="ae9c2-130">Nazwa tego rozsyłania.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="ae9c2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae9c2-131">-ResourceGroupName</span></span>
<span data-ttu-id="ae9c2-132">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-132">The resource group.</span></span>

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

### <span data-ttu-id="ae9c2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae9c2-133">-ResourceId</span></span>
<span data-ttu-id="ae9c2-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-134">The resource identifier.</span></span>

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

### <span data-ttu-id="ae9c2-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="ae9c2-135">-RetryAttempt</span></span>
<span data-ttu-id="ae9c2-136">Ponowna próba wykonania.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="ae9c2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae9c2-137">CommonParameters</span></span>
<span data-ttu-id="ae9c2-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae9c2-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae9c2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae9c2-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae9c2-140">INPUTS</span></span>

### <span data-ttu-id="ae9c2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ae9c2-141">System.String</span></span>

### <span data-ttu-id="ae9c2-142">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ae9c2-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ae9c2-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="ae9c2-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ae9c2-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae9c2-144">OUTPUTS</span></span>

### <span data-ttu-id="ae9c2-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="ae9c2-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ae9c2-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae9c2-146">NOTES</span></span>

## <span data-ttu-id="ae9c2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae9c2-147">RELATED LINKS</span></span>
