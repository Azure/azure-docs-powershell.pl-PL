---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: f995050e86189c1b84652895ad0434403c4e86d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979402"
---
# <span data-ttu-id="34df3-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="34df3-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="34df3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34df3-102">SYNOPSIS</span></span>
<span data-ttu-id="34df3-103">Usuwa wdrożenie w zakresie dzierżawy i wszelkie skojarzone operacje.</span><span class="sxs-lookup"><span data-stu-id="34df3-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="34df3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="34df3-104">SYNTAX</span></span>

### <span data-ttu-id="34df3-105">RemoveByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="34df3-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34df3-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="34df3-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34df3-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="34df3-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34df3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="34df3-108">DESCRIPTION</span></span>
<span data-ttu-id="34df3-109">Polecenie **cmdlet Remove-AzTenantDeployment** usuwa wdrożenie platformy Azure w bieżącym zakresie dzierżawy i wszystkie skojarzone operacje.</span><span class="sxs-lookup"><span data-stu-id="34df3-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="34df3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="34df3-110">EXAMPLES</span></span>

### <span data-ttu-id="34df3-111">Przykład 1. Usuwanie wdrożenia z podaną nazwą</span><span class="sxs-lookup"><span data-stu-id="34df3-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="34df3-112">To polecenie usuwa wdrożenie "RolesDeployment" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="34df3-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="34df3-113">Przykład 2. Uzyskaj wdrożenie i usuń je</span><span class="sxs-lookup"><span data-stu-id="34df3-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="34df3-114">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie dzierżawy i usuwa je.</span><span class="sxs-lookup"><span data-stu-id="34df3-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="34df3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34df3-115">PARAMETERS</span></span>

### <span data-ttu-id="34df3-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="34df3-116">-AsJob</span></span>
<span data-ttu-id="34df3-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="34df3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34df3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34df3-118">-DefaultProfile</span></span>
<span data-ttu-id="34df3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="34df3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34df3-120">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="34df3-120">-Id</span></span>
<span data-ttu-id="34df3-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="34df3-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="34df3-122">przykład: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="34df3-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="34df3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34df3-123">-InputObject</span></span>
<span data-ttu-id="34df3-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="34df3-124">The deployment object.</span></span>

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

### <span data-ttu-id="34df3-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="34df3-125">-Name</span></span>
<span data-ttu-id="34df3-126">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="34df3-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34df3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34df3-127">-PassThru</span></span>
<span data-ttu-id="34df3-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="34df3-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="34df3-129">— Przed</span><span class="sxs-lookup"><span data-stu-id="34df3-129">-Pre</span></span>
<span data-ttu-id="34df3-130">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="34df3-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="34df3-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34df3-131">-Confirm</span></span>
<span data-ttu-id="34df3-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34df3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34df3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34df3-133">-WhatIf</span></span>
<span data-ttu-id="34df3-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34df3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34df3-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="34df3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34df3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34df3-136">CommonParameters</span></span>
<span data-ttu-id="34df3-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34df3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34df3-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34df3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34df3-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34df3-139">INPUTS</span></span>

### <span data-ttu-id="34df3-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="34df3-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="34df3-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34df3-141">OUTPUTS</span></span>

### <span data-ttu-id="34df3-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="34df3-142">System.Boolean</span></span>

## <span data-ttu-id="34df3-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="34df3-143">NOTES</span></span>

## <span data-ttu-id="34df3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34df3-144">RELATED LINKS</span></span>
