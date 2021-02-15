---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201867"
---
# <span data-ttu-id="6adcb-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6adcb-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="6adcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6adcb-102">SYNOPSIS</span></span>
<span data-ttu-id="6adcb-103">Usuwa wdrożenie w grupie zarządzania i wszystkie skojarzone operacje.</span><span class="sxs-lookup"><span data-stu-id="6adcb-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="6adcb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6adcb-104">SYNTAX</span></span>

### <span data-ttu-id="6adcb-105">RemoveByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="6adcb-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adcb-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6adcb-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adcb-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="6adcb-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6adcb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6adcb-108">DESCRIPTION</span></span>
<span data-ttu-id="6adcb-109">Polecenie **cmdlet Remove-AzManagementGroupDeployment** usuwa wdrożenie platformy Azure w grupie zarządzania i wszystkie skojarzone operacje.</span><span class="sxs-lookup"><span data-stu-id="6adcb-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="6adcb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6adcb-110">EXAMPLES</span></span>

### <span data-ttu-id="6adcb-111">Przykład 1. Usuwanie wdrożenia z podaną nazwą</span><span class="sxs-lookup"><span data-stu-id="6adcb-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="6adcb-112">To polecenie usuwa wdrożenie "RolesDeployment" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="6adcb-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="6adcb-113">Przykład 2. Uzyskaj wdrożenie i usuń je</span><span class="sxs-lookup"><span data-stu-id="6adcb-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="6adcb-114">To polecenie pobiera wdrożenie "RolesDeployment" w grupie zarządzania "myMG" i usuwa je.</span><span class="sxs-lookup"><span data-stu-id="6adcb-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="6adcb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6adcb-115">PARAMETERS</span></span>

### <span data-ttu-id="6adcb-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6adcb-116">-AsJob</span></span>
<span data-ttu-id="6adcb-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6adcb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6adcb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6adcb-118">-DefaultProfile</span></span>
<span data-ttu-id="6adcb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6adcb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6adcb-120">— Id</span><span class="sxs-lookup"><span data-stu-id="6adcb-120">-Id</span></span>
<span data-ttu-id="6adcb-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="6adcb-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="6adcb-122">przykład: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="6adcb-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6adcb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6adcb-123">-InputObject</span></span>
<span data-ttu-id="6adcb-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="6adcb-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6adcb-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="6adcb-125">-ManagementGroupId</span></span>
<span data-ttu-id="6adcb-126">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="6adcb-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6adcb-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6adcb-127">-Name</span></span>
<span data-ttu-id="6adcb-128">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="6adcb-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6adcb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6adcb-129">-PassThru</span></span>
<span data-ttu-id="6adcb-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="6adcb-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6adcb-131">— Przed</span><span class="sxs-lookup"><span data-stu-id="6adcb-131">-Pre</span></span>
<span data-ttu-id="6adcb-132">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="6adcb-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6adcb-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6adcb-133">-Confirm</span></span>
<span data-ttu-id="6adcb-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6adcb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6adcb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6adcb-135">-WhatIf</span></span>
<span data-ttu-id="6adcb-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6adcb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6adcb-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6adcb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6adcb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6adcb-138">CommonParameters</span></span>
<span data-ttu-id="6adcb-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6adcb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6adcb-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6adcb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6adcb-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6adcb-141">INPUTS</span></span>

### <span data-ttu-id="6adcb-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="6adcb-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="6adcb-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6adcb-143">OUTPUTS</span></span>

### <span data-ttu-id="6adcb-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6adcb-144">System.Boolean</span></span>

## <span data-ttu-id="6adcb-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6adcb-145">NOTES</span></span>

## <span data-ttu-id="6adcb-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6adcb-146">RELATED LINKS</span></span>
