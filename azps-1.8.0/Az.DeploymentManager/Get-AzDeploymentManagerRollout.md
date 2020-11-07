---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: fbcb93ec75dc0e136c1c18743a8686f7642ef02f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709974"
---
# <span data-ttu-id="083cb-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="083cb-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="083cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="083cb-102">SYNOPSIS</span></span>
<span data-ttu-id="083cb-103">Pobiera rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="083cb-103">Gets the rollout.</span></span>

## <span data-ttu-id="083cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="083cb-104">SYNTAX</span></span>

### <span data-ttu-id="083cb-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="083cb-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="083cb-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="083cb-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="083cb-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="083cb-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="083cb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="083cb-108">DESCRIPTION</span></span>
<span data-ttu-id="083cb-109">Polecenie cmdlet **Get-AzDeploymentManagerRollout** pobiera i zwraca obiekt reprezentujący to rozmieszczenie wraz ze wszystkimi szczegółowymi informacjami na temat postępu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="083cb-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="083cb-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="083cb-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="083cb-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="083cb-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="083cb-112">Zwrócony obiekt rozmieszczenia zawiera usługi, jednostki usług i kroki, które zostały wdrożone, i te, które są w toku.</span><span class="sxs-lookup"><span data-stu-id="083cb-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="083cb-113">Te, które nie zostały jeszcze wdrożone, nie znajdują się w odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="083cb-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="083cb-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="083cb-114">EXAMPLES</span></span>

### <span data-ttu-id="083cb-115">Przykład 1 pobieranie rozmieszczenia</span><span class="sxs-lookup"><span data-stu-id="083cb-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="083cb-116">To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="083cb-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="083cb-117">Przykład 2 pobieranie i wyświetlanie szczegółów rozmieszczenia</span><span class="sxs-lookup"><span data-stu-id="083cb-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="083cb-118">To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="083cb-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="083cb-119">Przełącznik-verbose umożliwia wyświetlanie wszystkich szczegółów dotyczących rozmieszczenia hierarchicznie; Pokazywanie usług, jednostek oraz kroków w poszczególnych jednostkach oraz informacje kontekstowe dla każdego kroku w celu uzyskania całościowego widoku rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="083cb-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="083cb-120">Przykład 3: uzyskiwanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="083cb-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="083cb-121">To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="083cb-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="083cb-122">Przykład 4: uzyskiwanie rozmieszczenia przy użyciu obiektu do rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="083cb-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="083cb-123">To polecenie pobiera rozmieszczenie, których nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="083cb-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="083cb-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="083cb-124">PARAMETERS</span></span>

### <span data-ttu-id="083cb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083cb-125">-DefaultProfile</span></span>
<span data-ttu-id="083cb-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="083cb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="083cb-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="083cb-127">-InputObject</span></span>
<span data-ttu-id="083cb-128">Rozmieszczanie obiektu.</span><span class="sxs-lookup"><span data-stu-id="083cb-128">Rollout object.</span></span>

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

### <span data-ttu-id="083cb-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="083cb-129">-Name</span></span>
<span data-ttu-id="083cb-130">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="083cb-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="083cb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="083cb-131">-ResourceGroupName</span></span>
<span data-ttu-id="083cb-132">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="083cb-132">The resource group.</span></span>

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

### <span data-ttu-id="083cb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="083cb-133">-ResourceId</span></span>
<span data-ttu-id="083cb-134">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="083cb-134">The resource identifier.</span></span>

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

### <span data-ttu-id="083cb-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="083cb-135">-RetryAttempt</span></span>
<span data-ttu-id="083cb-136">Próba ponowienia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="083cb-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="083cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083cb-137">CommonParameters</span></span>
<span data-ttu-id="083cb-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083cb-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083cb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083cb-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="083cb-140">INPUTS</span></span>

### <span data-ttu-id="083cb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="083cb-141">System.String</span></span>

### <span data-ttu-id="083cb-142">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="083cb-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="083cb-143">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="083cb-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="083cb-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="083cb-144">OUTPUTS</span></span>

### <span data-ttu-id="083cb-145">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="083cb-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="083cb-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="083cb-146">NOTES</span></span>

## <span data-ttu-id="083cb-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="083cb-147">RELATED LINKS</span></span>
