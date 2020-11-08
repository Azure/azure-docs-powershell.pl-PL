---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223193"
---
# <span data-ttu-id="67956-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="67956-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="67956-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67956-102">SYNOPSIS</span></span>
<span data-ttu-id="67956-103">Pobierz wdrożenie w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="67956-103">Get deployment at a management group</span></span>

## <span data-ttu-id="67956-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67956-104">SYNTAX</span></span>

### <span data-ttu-id="67956-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67956-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67956-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="67956-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67956-107">Opis</span><span class="sxs-lookup"><span data-stu-id="67956-107">DESCRIPTION</span></span>
<span data-ttu-id="67956-108">Polecenie cmdlet **Get-AzManagementGroupDeployment** pobiera wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="67956-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="67956-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="67956-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="67956-110">Domyślnie polecenie **Get-AzManagementGroupDeployment** pobiera wszystkie wdrożenia w grupie Zarządzanie.</span><span class="sxs-lookup"><span data-stu-id="67956-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="67956-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67956-111">EXAMPLES</span></span>

### <span data-ttu-id="67956-112">Przykład 1: pobieranie wszystkich wdrożeń w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="67956-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="67956-113">To polecenie pobiera wszystkie wdrożenia w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="67956-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="67956-114">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="67956-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="67956-115">To polecenie uzyskuje wdrożenie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="67956-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="67956-116">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="67956-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="67956-117">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="67956-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="67956-118">Przykład 3: uzyskiwanie wdrożenia według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="67956-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="67956-119">To polecenie uzyskuje wdrożenie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="67956-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="67956-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67956-120">PARAMETERS</span></span>

### <span data-ttu-id="67956-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="67956-121">-ApiVersion</span></span>
<span data-ttu-id="67956-122">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="67956-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="67956-123">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="67956-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67956-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67956-124">-DefaultProfile</span></span>
<span data-ttu-id="67956-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67956-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67956-126">-ID</span><span class="sxs-lookup"><span data-stu-id="67956-126">-Id</span></span>
<span data-ttu-id="67956-127">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="67956-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="67956-128">przykład:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="67956-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67956-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="67956-129">-ManagementGroupId</span></span>
<span data-ttu-id="67956-130">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="67956-130">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67956-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="67956-131">-Name</span></span>
<span data-ttu-id="67956-132">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="67956-132">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67956-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="67956-133">-Pre</span></span>
<span data-ttu-id="67956-134">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="67956-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67956-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67956-135">CommonParameters</span></span>
<span data-ttu-id="67956-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67956-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67956-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67956-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67956-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67956-138">INPUTS</span></span>

### <span data-ttu-id="67956-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="67956-139">None</span></span>

## <span data-ttu-id="67956-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67956-140">OUTPUTS</span></span>

### <span data-ttu-id="67956-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="67956-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="67956-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67956-142">NOTES</span></span>

## <span data-ttu-id="67956-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67956-143">RELATED LINKS</span></span>
