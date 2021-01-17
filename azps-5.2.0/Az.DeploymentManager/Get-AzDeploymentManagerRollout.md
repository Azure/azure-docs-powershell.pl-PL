---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324245"
---
# <span data-ttu-id="ca337-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ca337-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="ca337-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca337-102">SYNOPSIS</span></span>
<span data-ttu-id="ca337-103">Pobiera rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="ca337-103">Gets the rollout.</span></span>

## <span data-ttu-id="ca337-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca337-104">SYNTAX</span></span>

### <span data-ttu-id="ca337-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ca337-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca337-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="ca337-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca337-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca337-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca337-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ca337-108">DESCRIPTION</span></span>
<span data-ttu-id="ca337-109">Polecenie cmdlet **Get-AzDeploymentManagerRollout** pobiera i zwraca obiekt reprezentujący to rozmieszczenie wraz ze wszystkimi szczegółowymi informacjami na temat postępu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ca337-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="ca337-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca337-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ca337-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ca337-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="ca337-112">Zwrócony obiekt rozmieszczenia zawiera usługi, jednostki usług i kroki, które zostały wdrożone, i te, które są w toku.</span><span class="sxs-lookup"><span data-stu-id="ca337-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="ca337-113">Te, które nie zostały jeszcze wdrożone, nie znajdują się w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="ca337-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="ca337-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca337-114">EXAMPLES</span></span>

### <span data-ttu-id="ca337-115">Przykład 1 pobieranie rozmieszczenia</span><span class="sxs-lookup"><span data-stu-id="ca337-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="ca337-116">To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ca337-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="ca337-117">Przykład 2 pobieranie i wyświetlanie szczegółów rozmieszczenia</span><span class="sxs-lookup"><span data-stu-id="ca337-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="ca337-118">To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ca337-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="ca337-119">Przełącznik-verbose umożliwia wyświetlanie wszystkich szczegółów dotyczących rozmieszczenia hierarchicznie; Pokazywanie usług, jednostek oraz kroków w poszczególnych jednostkach oraz informacje kontekstowe dla każdego kroku w celu uzyskania całościowego widoku rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="ca337-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="ca337-120">Przykład 3: uzyskiwanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="ca337-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ca337-121">To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ca337-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ca337-122">Przykład 4: uzyskiwanie rozmieszczenia przy użyciu obiektu do rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="ca337-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="ca337-123">To polecenie pobiera rozmieszczenie, których nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="ca337-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ca337-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca337-124">PARAMETERS</span></span>

### <span data-ttu-id="ca337-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca337-125">-DefaultProfile</span></span>
<span data-ttu-id="ca337-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca337-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca337-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca337-127">-InputObject</span></span>
<span data-ttu-id="ca337-128">Rozmieszczanie obiektu.</span><span class="sxs-lookup"><span data-stu-id="ca337-128">Rollout object.</span></span>

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

### <span data-ttu-id="ca337-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca337-129">-Name</span></span>
<span data-ttu-id="ca337-130">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="ca337-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="ca337-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca337-131">-ResourceGroupName</span></span>
<span data-ttu-id="ca337-132">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca337-132">The resource group.</span></span>

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

### <span data-ttu-id="ca337-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca337-133">-ResourceId</span></span>
<span data-ttu-id="ca337-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ca337-134">The resource identifier.</span></span>

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

### <span data-ttu-id="ca337-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="ca337-135">-RetryAttempt</span></span>
<span data-ttu-id="ca337-136">Próba ponowienia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ca337-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="ca337-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca337-137">CommonParameters</span></span>
<span data-ttu-id="ca337-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca337-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca337-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca337-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca337-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca337-140">INPUTS</span></span>

### <span data-ttu-id="ca337-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ca337-141">System.String</span></span>

### <span data-ttu-id="ca337-142">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ca337-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ca337-143">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ca337-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ca337-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca337-144">OUTPUTS</span></span>

### <span data-ttu-id="ca337-145">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ca337-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ca337-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca337-146">NOTES</span></span>

## <span data-ttu-id="ca337-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca337-147">RELATED LINKS</span></span>
