---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: eb0c7db4706aacfba4010632422869f0dca54694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705629"
---
# <span data-ttu-id="b2700-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b2700-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="b2700-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2700-102">SYNOPSIS</span></span>
<span data-ttu-id="b2700-103">Pobiera krok.</span><span class="sxs-lookup"><span data-stu-id="b2700-103">Gets the step.</span></span>

## <span data-ttu-id="b2700-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2700-104">SYNTAX</span></span>

### <span data-ttu-id="b2700-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b2700-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2700-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="b2700-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2700-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="b2700-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2700-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b2700-108">DESCRIPTION</span></span>
<span data-ttu-id="b2700-109">Polecenie cmdlet **Get-AzDeploymentManagerStep** Pobiera krok i zwraca obiekt reprezentujący ten krok.</span><span class="sxs-lookup"><span data-stu-id="b2700-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="b2700-110">Określ krok, podając jego nazwę i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2700-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="b2700-111">Alternatywnie możesz podać obiekt Step lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b2700-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="b2700-112">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w źródle artefaktów, korzystając z polecenia cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="b2700-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="b2700-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2700-113">EXAMPLES</span></span>

### <span data-ttu-id="b2700-114">Przykład 1: uzyskiwanie kroku</span><span class="sxs-lookup"><span data-stu-id="b2700-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="b2700-115">To polecenie pobiera krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b2700-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b2700-116">Przykład 2: uzyskiwanie kroku przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="b2700-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="b2700-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2700-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="b2700-118">To polecenie pobiera krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b2700-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b2700-119">Przykład 3: uzyskiwanie kroku przy użyciu obiektu zwróconego przez New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b2700-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="b2700-120">To polecenie pobiera krok, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $stepObject.</span><span class="sxs-lookup"><span data-stu-id="b2700-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="b2700-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2700-121">PARAMETERS</span></span>

### <span data-ttu-id="b2700-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2700-122">-DefaultProfile</span></span>
<span data-ttu-id="b2700-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2700-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2700-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b2700-124">-InputObject</span></span>
<span data-ttu-id="b2700-125">Obiekt zasobu kroku.</span><span class="sxs-lookup"><span data-stu-id="b2700-125">The step resource object.</span></span>

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

### <span data-ttu-id="b2700-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2700-126">-Name</span></span>
<span data-ttu-id="b2700-127">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="b2700-127">The name of the step.</span></span>

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

### <span data-ttu-id="b2700-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2700-128">-ResourceGroupName</span></span>
<span data-ttu-id="b2700-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2700-129">The resource group.</span></span>

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

### <span data-ttu-id="b2700-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2700-130">-ResourceId</span></span>
<span data-ttu-id="b2700-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b2700-131">The resource identifier.</span></span>

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

### <span data-ttu-id="b2700-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2700-132">CommonParameters</span></span>
<span data-ttu-id="b2700-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2700-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2700-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2700-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2700-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2700-135">INPUTS</span></span>

### <span data-ttu-id="b2700-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b2700-136">System.String</span></span>

### <span data-ttu-id="b2700-137">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b2700-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b2700-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2700-138">OUTPUTS</span></span>

### <span data-ttu-id="b2700-139">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b2700-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b2700-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2700-140">NOTES</span></span>

## <span data-ttu-id="b2700-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2700-141">RELATED LINKS</span></span>
