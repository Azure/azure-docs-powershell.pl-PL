---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368678"
---
# <span data-ttu-id="87e9e-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="87e9e-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="87e9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="87e9e-103">Pobierz wdrożenie w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="87e9e-103">Get deployment at a management group</span></span>

## <span data-ttu-id="87e9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87e9e-104">SYNTAX</span></span>

### <span data-ttu-id="87e9e-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="87e9e-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87e9e-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="87e9e-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87e9e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="87e9e-107">DESCRIPTION</span></span>
<span data-ttu-id="87e9e-108">Polecenie cmdlet **Get-AzManagementGroupDeployment** pobiera wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="87e9e-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="87e9e-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="87e9e-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="87e9e-110">Domyślnie polecenie **Get-AzManagementGroupDeployment** pobiera wszystkie wdrożenia w grupie Zarządzanie.</span><span class="sxs-lookup"><span data-stu-id="87e9e-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="87e9e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87e9e-111">EXAMPLES</span></span>

### <span data-ttu-id="87e9e-112">Przykład 1: pobieranie wszystkich wdrożeń w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="87e9e-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="87e9e-113">To polecenie pobiera wszystkie wdrożenia w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="87e9e-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="87e9e-114">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="87e9e-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="87e9e-115">To polecenie uzyskuje wdrożenie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="87e9e-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="87e9e-116">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="87e9e-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="87e9e-117">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="87e9e-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="87e9e-118">Przykład 3: uzyskiwanie wdrożenia według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="87e9e-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="87e9e-119">To polecenie uzyskuje wdrożenie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="87e9e-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="87e9e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87e9e-120">PARAMETERS</span></span>

### <span data-ttu-id="87e9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e9e-121">-DefaultProfile</span></span>
<span data-ttu-id="87e9e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87e9e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e9e-123">-ID</span><span class="sxs-lookup"><span data-stu-id="87e9e-123">-Id</span></span>
<span data-ttu-id="87e9e-124">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="87e9e-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="87e9e-125">przykład:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="87e9e-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="87e9e-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="87e9e-126">-ManagementGroupId</span></span>
<span data-ttu-id="87e9e-127">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="87e9e-127">The management group id.</span></span>

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

### <span data-ttu-id="87e9e-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87e9e-128">-Name</span></span>
<span data-ttu-id="87e9e-129">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="87e9e-129">The name of deployment.</span></span>

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

### <span data-ttu-id="87e9e-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="87e9e-130">-Pre</span></span>
<span data-ttu-id="87e9e-131">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="87e9e-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="87e9e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e9e-132">CommonParameters</span></span>
<span data-ttu-id="87e9e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e9e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e9e-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87e9e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e9e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87e9e-135">INPUTS</span></span>

### <span data-ttu-id="87e9e-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="87e9e-136">None</span></span>

## <span data-ttu-id="87e9e-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87e9e-137">OUTPUTS</span></span>

### <span data-ttu-id="87e9e-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="87e9e-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="87e9e-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87e9e-139">NOTES</span></span>

## <span data-ttu-id="87e9e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87e9e-140">RELATED LINKS</span></span>
