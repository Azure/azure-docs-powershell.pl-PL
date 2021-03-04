---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 2af89bac9e748fca0719abf34bd672d2b09c3af5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967633"
---
# <span data-ttu-id="ca120-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ca120-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ca120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca120-102">SYNOPSIS</span></span>
<span data-ttu-id="ca120-103">Anulowanie uruchomionego wdrożenia w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="ca120-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="ca120-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca120-104">SYNTAX</span></span>

### <span data-ttu-id="ca120-105">StopByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="ca120-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca120-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ca120-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca120-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="ca120-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca120-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca120-108">DESCRIPTION</span></span>
<span data-ttu-id="ca120-109">Polecenie cmdlet **Stop-AzManagementGroupDeployment** anuluje wdrożenie rozpoczęte, ale nie ukończone w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="ca120-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="ca120-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niepełny stan inicjowania obsługi, taki jak inicjowanie obsługi administracyjnej, a nie stan ukończony, taki jak Inicjowanie obsługi administracyjnej lub Zakończone niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ca120-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="ca120-111">Aby utworzyć wdrożenie w grupie zarządzania, użyj New-AzManagementGroupDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca120-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="ca120-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca120-112">EXAMPLES</span></span>

### <span data-ttu-id="ca120-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca120-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="ca120-114">To polecenie anuluje uruchomione wdrożenie "deployment01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="ca120-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="ca120-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ca120-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="ca120-116">To polecenie pobiera wdrożenie "deployment01" w grupie zarządzania "myMG" i anuluje je.</span><span class="sxs-lookup"><span data-stu-id="ca120-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="ca120-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca120-117">PARAMETERS</span></span>

### <span data-ttu-id="ca120-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca120-118">-DefaultProfile</span></span>
<span data-ttu-id="ca120-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca120-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca120-120">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="ca120-120">-Id</span></span>
<span data-ttu-id="ca120-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ca120-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ca120-122">przykład: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ca120-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca120-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca120-123">-InputObject</span></span>
<span data-ttu-id="ca120-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ca120-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca120-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ca120-125">-ManagementGroupId</span></span>
<span data-ttu-id="ca120-126">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="ca120-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca120-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ca120-127">-Name</span></span>
<span data-ttu-id="ca120-128">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ca120-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca120-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca120-129">-PassThru</span></span>
<span data-ttu-id="ca120-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="ca120-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ca120-131">— Przed</span><span class="sxs-lookup"><span data-stu-id="ca120-131">-Pre</span></span>
<span data-ttu-id="ca120-132">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ca120-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ca120-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca120-133">-Confirm</span></span>
<span data-ttu-id="ca120-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ca120-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca120-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca120-135">-WhatIf</span></span>
<span data-ttu-id="ca120-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca120-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca120-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ca120-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca120-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca120-138">CommonParameters</span></span>
<span data-ttu-id="ca120-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca120-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca120-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca120-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca120-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca120-141">INPUTS</span></span>

### <span data-ttu-id="ca120-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ca120-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ca120-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca120-143">OUTPUTS</span></span>

### <span data-ttu-id="ca120-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca120-144">System.Boolean</span></span>

## <span data-ttu-id="ca120-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca120-145">NOTES</span></span>

## <span data-ttu-id="ca120-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca120-146">RELATED LINKS</span></span>
