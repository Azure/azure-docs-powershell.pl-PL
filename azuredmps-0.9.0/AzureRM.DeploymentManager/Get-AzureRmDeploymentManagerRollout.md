---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522929"
---
# <span data-ttu-id="c0457-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c0457-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="c0457-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0457-102">SYNOPSIS</span></span>
<span data-ttu-id="c0457-103">Umożliwia rozmieszczenie.</span><span class="sxs-lookup"><span data-stu-id="c0457-103">Gets a rollout.</span></span>

## <span data-ttu-id="c0457-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0457-104">SYNTAX</span></span>

### <span data-ttu-id="c0457-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c0457-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0457-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c0457-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0457-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="c0457-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0457-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c0457-108">DESCRIPTION</span></span>
<span data-ttu-id="c0457-109">Polecenie cmdlet **Get-AzureRmDeploymentManagerRollout** pobiera i zwraca obiekt reprezentujący to rozmieszczenie wraz ze wszystkimi szczegółowymi informacjami na temat postępu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c0457-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="c0457-110">Określanie rozmieszczenia według nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0457-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="c0457-111">Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c0457-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="c0457-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0457-112">EXAMPLES</span></span>

### <span data-ttu-id="c0457-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0457-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="c0457-114">To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c0457-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c0457-115">Przykład 2: uzyskiwanie rozmieszczenia przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="c0457-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="c0457-116">To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c0457-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c0457-117">Przykład 3: uzyskiwanie rozmieszczenia przy użyciu obiektu do rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="c0457-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="c0457-118">To polecenie pobiera rozmieszczenie, których nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="c0457-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="c0457-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0457-119">PARAMETERS</span></span>

### <span data-ttu-id="c0457-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0457-120">-DefaultProfile</span></span>
<span data-ttu-id="c0457-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0457-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0457-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0457-122">-Name</span></span>
<span data-ttu-id="c0457-123">Nazwa rozmieszczenia.</span><span class="sxs-lookup"><span data-stu-id="c0457-123">The name of the rollout.</span></span>

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

### <span data-ttu-id="c0457-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0457-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0457-125">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="c0457-125">The resource group.</span></span>

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

### <span data-ttu-id="c0457-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0457-126">-ResourceId</span></span>
<span data-ttu-id="c0457-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c0457-127">The resource identifier.</span></span>

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

### <span data-ttu-id="c0457-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="c0457-128">-RetryAttempt</span></span>
<span data-ttu-id="c0457-129">Próba ponowienia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c0457-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0457-130">— Wprowadzanie</span><span class="sxs-lookup"><span data-stu-id="c0457-130">-Rollout</span></span>
<span data-ttu-id="c0457-131">Rozmieszczanie obiektu.</span><span class="sxs-lookup"><span data-stu-id="c0457-131">Rollout object.</span></span>

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

### <span data-ttu-id="c0457-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0457-132">CommonParameters</span></span>
<span data-ttu-id="c0457-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0457-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0457-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0457-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0457-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0457-135">INPUTS</span></span>

### <span data-ttu-id="c0457-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c0457-136">None</span></span>

## <span data-ttu-id="c0457-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0457-137">OUTPUTS</span></span>

### <span data-ttu-id="c0457-138">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout</span><span class="sxs-lookup"><span data-stu-id="c0457-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="c0457-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0457-139">NOTES</span></span>

## <span data-ttu-id="c0457-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0457-140">RELATED LINKS</span></span>

[<span data-ttu-id="c0457-141">Zatrzymaj — AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c0457-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="c0457-142">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c0457-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="c0457-143">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c0457-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)