---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6a18c886ddddc30c82746ebe76d83d9477399755
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895937"
---
# <span data-ttu-id="23cfe-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23cfe-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="23cfe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="23cfe-103">Pobierz wdrożenie w grupie Zarządzanie</span><span class="sxs-lookup"><span data-stu-id="23cfe-103">Get deployment at a mangement group</span></span>

## <span data-ttu-id="23cfe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23cfe-104">SYNTAX</span></span>

### <span data-ttu-id="23cfe-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23cfe-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23cfe-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="23cfe-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23cfe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="23cfe-107">DESCRIPTION</span></span>
<span data-ttu-id="23cfe-108">Polecenie cmdlet **Get-AzManagementGroupDeployment** pobiera wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="23cfe-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="23cfe-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="23cfe-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="23cfe-110">Domyślnie polecenie **Get-AzManagementGroupDeployment** pobiera wszystkie wdrożenia w grupie Zarządzanie.</span><span class="sxs-lookup"><span data-stu-id="23cfe-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="23cfe-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23cfe-111">EXAMPLES</span></span>

### <span data-ttu-id="23cfe-112">Przykład 1: pobieranie wszystkich wdrożeń w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="23cfe-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="23cfe-113">To polecenie pobiera wszystkie wdrożenia w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="23cfe-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="23cfe-114">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="23cfe-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="23cfe-115">To polecenie uzyskuje wdrożenie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="23cfe-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="23cfe-116">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="23cfe-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="23cfe-117">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="23cfe-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="23cfe-118">Przykład 3: uzyskiwanie wdrożenia według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="23cfe-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="23cfe-119">To polecenie uzyskuje wdrożenie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="23cfe-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="23cfe-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23cfe-120">PARAMETERS</span></span>

### <span data-ttu-id="23cfe-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23cfe-121">-ApiVersion</span></span>
<span data-ttu-id="23cfe-122">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="23cfe-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="23cfe-123">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="23cfe-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="23cfe-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cfe-124">-DefaultProfile</span></span>
<span data-ttu-id="23cfe-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23cfe-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cfe-126">-ID</span><span class="sxs-lookup"><span data-stu-id="23cfe-126">-Id</span></span>
<span data-ttu-id="23cfe-127">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="23cfe-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="23cfe-128">przykład:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="23cfe-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="23cfe-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="23cfe-129">-ManagementGroupId</span></span>
<span data-ttu-id="23cfe-130">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="23cfe-130">The management group id.</span></span>

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

### <span data-ttu-id="23cfe-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23cfe-131">-Name</span></span>
<span data-ttu-id="23cfe-132">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="23cfe-132">The name of deployment.</span></span>

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

### <span data-ttu-id="23cfe-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="23cfe-133">-Pre</span></span>
<span data-ttu-id="23cfe-134">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="23cfe-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="23cfe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cfe-135">CommonParameters</span></span>
<span data-ttu-id="23cfe-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cfe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cfe-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23cfe-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cfe-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cfe-138">INPUTS</span></span>

### <span data-ttu-id="23cfe-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="23cfe-139">None</span></span>

## <span data-ttu-id="23cfe-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23cfe-140">OUTPUTS</span></span>

### <span data-ttu-id="23cfe-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="23cfe-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="23cfe-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23cfe-142">NOTES</span></span>

## <span data-ttu-id="23cfe-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23cfe-143">RELATED LINKS</span></span>
