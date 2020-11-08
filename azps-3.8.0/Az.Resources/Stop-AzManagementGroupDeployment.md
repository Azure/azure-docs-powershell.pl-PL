---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 8604aa58efff7b6fe7ef6dc931fdcb54b313d634
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050679"
---
# <span data-ttu-id="84b39-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84b39-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="84b39-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84b39-102">SYNOPSIS</span></span>
<span data-ttu-id="84b39-103">Anulowanie uruchomionego wdrożenia w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="84b39-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="84b39-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84b39-104">SYNTAX</span></span>

### <span data-ttu-id="84b39-105">StopByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="84b39-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84b39-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="84b39-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b39-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="84b39-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b39-108">Opis</span><span class="sxs-lookup"><span data-stu-id="84b39-108">DESCRIPTION</span></span>
<span data-ttu-id="84b39-109">Polecenie cmdlet **stop-AzManagementGroupDeployment** powoduje anulowanie wdrożenia, które zostało uruchomione, ale nie zostało ukończone w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="84b39-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="84b39-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="84b39-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="84b39-111">Aby utworzyć wdrożenie w grupie zarządzania, użyj polecenia cmdlet New-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="84b39-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="84b39-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84b39-112">EXAMPLES</span></span>

### <span data-ttu-id="84b39-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="84b39-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="84b39-114">To polecenie powoduje anulowanie uruchomionego wdrożenia "deployment01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="84b39-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="84b39-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="84b39-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="84b39-116">To polecenie pobiera wdrożenie "deployment01" w grupie zarządzania "myMG" i anuluje je.</span><span class="sxs-lookup"><span data-stu-id="84b39-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="84b39-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84b39-117">PARAMETERS</span></span>

### <span data-ttu-id="84b39-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="84b39-118">-ApiVersion</span></span>
<span data-ttu-id="84b39-119">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="84b39-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="84b39-120">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="84b39-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="84b39-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b39-121">-DefaultProfile</span></span>
<span data-ttu-id="84b39-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="84b39-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84b39-123">-ID</span><span class="sxs-lookup"><span data-stu-id="84b39-123">-Id</span></span>
<span data-ttu-id="84b39-124">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="84b39-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="84b39-125">przykład:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="84b39-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b39-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="84b39-126">-InputObject</span></span>
<span data-ttu-id="84b39-127">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="84b39-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84b39-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="84b39-128">-ManagementGroupId</span></span>
<span data-ttu-id="84b39-129">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="84b39-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b39-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84b39-130">-Name</span></span>
<span data-ttu-id="84b39-131">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="84b39-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b39-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84b39-132">-PassThru</span></span>
<span data-ttu-id="84b39-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="84b39-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="84b39-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="84b39-134">-Pre</span></span>
<span data-ttu-id="84b39-135">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="84b39-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="84b39-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84b39-136">-Confirm</span></span>
<span data-ttu-id="84b39-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b39-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b39-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b39-138">-WhatIf</span></span>
<span data-ttu-id="84b39-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b39-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b39-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84b39-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b39-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b39-141">CommonParameters</span></span>
<span data-ttu-id="84b39-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b39-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b39-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84b39-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b39-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84b39-144">INPUTS</span></span>

### <span data-ttu-id="84b39-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="84b39-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="84b39-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84b39-146">OUTPUTS</span></span>

### <span data-ttu-id="84b39-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84b39-147">System.Boolean</span></span>

## <span data-ttu-id="84b39-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84b39-148">NOTES</span></span>

## <span data-ttu-id="84b39-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84b39-149">RELATED LINKS</span></span>
