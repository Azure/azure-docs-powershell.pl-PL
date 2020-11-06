---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523182"
---
# <span data-ttu-id="87bfe-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="87bfe-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="87bfe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="87bfe-103">Pobiera krok wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="87bfe-103">Gets the deployment step.</span></span>

## <span data-ttu-id="87bfe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87bfe-104">SYNTAX</span></span>

### <span data-ttu-id="87bfe-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="87bfe-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87bfe-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="87bfe-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87bfe-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="87bfe-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87bfe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="87bfe-108">DESCRIPTION</span></span>
<span data-ttu-id="87bfe-109">Polecenie cmdlet **Get-AzureRmDeploymentManagerStep** Pobiera krok i zwraca obiekt reprezentujący ten krok.</span><span class="sxs-lookup"><span data-stu-id="87bfe-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="87bfe-110">Określ krok, podając jego nazwę i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87bfe-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="87bfe-111">Alternatywnie możesz podać obiekt Step lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="87bfe-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="87bfe-112">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w źródle artefaktów, korzystając z polecenia cmdlet Set-AzureRmDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="87bfe-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="87bfe-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87bfe-113">EXAMPLES</span></span>

### <span data-ttu-id="87bfe-114">Przykład 1: uzyskiwanie kroku</span><span class="sxs-lookup"><span data-stu-id="87bfe-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="87bfe-115">To polecenie pobiera krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="87bfe-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="87bfe-116">Przykład 2: uzyskiwanie kroku przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="87bfe-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="87bfe-117">To polecenie pobiera krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="87bfe-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="87bfe-118">Przykład 3: uzyskiwanie kroku przy użyciu obiektu zwróconego przez New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="87bfe-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="87bfe-119">To polecenie pobiera krok, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $stepObject.</span><span class="sxs-lookup"><span data-stu-id="87bfe-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="87bfe-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87bfe-120">PARAMETERS</span></span>

### <span data-ttu-id="87bfe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87bfe-121">-DefaultProfile</span></span>
<span data-ttu-id="87bfe-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87bfe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87bfe-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87bfe-123">-Name</span></span>
<span data-ttu-id="87bfe-124">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="87bfe-124">The name of the step.</span></span>

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

### <span data-ttu-id="87bfe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87bfe-125">-ResourceGroupName</span></span>
<span data-ttu-id="87bfe-126">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="87bfe-126">The resource group.</span></span>

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

### <span data-ttu-id="87bfe-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87bfe-127">-ResourceId</span></span>
<span data-ttu-id="87bfe-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="87bfe-128">The resource identifier.</span></span>

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

### <span data-ttu-id="87bfe-129">-Krok</span><span class="sxs-lookup"><span data-stu-id="87bfe-129">-Step</span></span>
<span data-ttu-id="87bfe-130">Obiekt zasobu kroku.</span><span class="sxs-lookup"><span data-stu-id="87bfe-130">The step resource object.</span></span>

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

### <span data-ttu-id="87bfe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87bfe-131">CommonParameters</span></span>
<span data-ttu-id="87bfe-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87bfe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="87bfe-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87bfe-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87bfe-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87bfe-134">INPUTS</span></span>

### <span data-ttu-id="87bfe-135">System. String</span><span class="sxs-lookup"><span data-stu-id="87bfe-135">System.String</span></span>

### <span data-ttu-id="87bfe-136">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="87bfe-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="87bfe-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87bfe-137">OUTPUTS</span></span>

### <span data-ttu-id="87bfe-138">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="87bfe-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="87bfe-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87bfe-139">NOTES</span></span>

## <span data-ttu-id="87bfe-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87bfe-140">RELATED LINKS</span></span>
