---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 73a124070dd329daff52ec5c0de16fb55ef74354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973569"
---
# <span data-ttu-id="d3a5b-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d3a5b-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="d3a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a5b-103">Wdrażanie w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="d3a5b-103">Get deployment at a management group</span></span>

## <span data-ttu-id="d3a5b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3a5b-104">SYNTAX</span></span>

### <span data-ttu-id="d3a5b-105">GetByDeploymentName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d3a5b-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3a5b-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d3a5b-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3a5b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3a5b-107">DESCRIPTION</span></span>
<span data-ttu-id="d3a5b-108">Polecenie **cmdlet Get-AzManagementGroupDeployment** pobiera wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="d3a5b-109">Określ parametr *Name (Nazwa)* *lub Id (Identyfikator),* aby filtrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="d3a5b-110">Domyślnie **get-azManagementGroupDeployment** otrzymuje wszystkie wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="d3a5b-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3a5b-111">EXAMPLES</span></span>

### <span data-ttu-id="d3a5b-112">Przykład 1. Uzyskiwanie wszystkich wdrożeń w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="d3a5b-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="d3a5b-113">To polecenie pobiera wszystkie wdrożenia w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="d3a5b-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="d3a5b-114">Przykład 2. Uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="d3a5b-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="d3a5b-115">To polecenie pobiera wdrożenie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="d3a5b-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="d3a5b-116">Możesz przypisać nazwę do wdrożenia podczas jego tworzenia przy użyciu polecenia cmdlet **New-AzManagementGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="d3a5b-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="d3a5b-117">Jeśli nie przypiszesz nazwy, polecenia cmdlet będą mieć nazwę domyślną opartą na szablonie używanym do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="d3a5b-118">Przykład 3. Uzyskiwanie wdrożenia według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="d3a5b-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="d3a5b-119">To polecenie pobiera wdrożenie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="d3a5b-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="d3a5b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a5b-120">PARAMETERS</span></span>

### <span data-ttu-id="d3a5b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a5b-121">-DefaultProfile</span></span>
<span data-ttu-id="d3a5b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a5b-123">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="d3a5b-123">-Id</span></span>
<span data-ttu-id="d3a5b-124">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d3a5b-125">przykład: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d3a5b-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a5b-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d3a5b-126">-ManagementGroupId</span></span>
<span data-ttu-id="d3a5b-127">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-127">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a5b-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d3a5b-128">-Name</span></span>
<span data-ttu-id="d3a5b-129">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-129">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a5b-130">— Przed</span><span class="sxs-lookup"><span data-stu-id="d3a5b-130">-Pre</span></span>
<span data-ttu-id="d3a5b-131">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d3a5b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a5b-132">CommonParameters</span></span>
<span data-ttu-id="d3a5b-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a5b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a5b-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3a5b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a5b-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3a5b-135">INPUTS</span></span>

### <span data-ttu-id="d3a5b-136">Brak</span><span class="sxs-lookup"><span data-stu-id="d3a5b-136">None</span></span>

## <span data-ttu-id="d3a5b-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3a5b-137">OUTPUTS</span></span>

### <span data-ttu-id="d3a5b-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d3a5b-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d3a5b-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3a5b-139">NOTES</span></span>

## <span data-ttu-id="d3a5b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3a5b-140">RELATED LINKS</span></span>
