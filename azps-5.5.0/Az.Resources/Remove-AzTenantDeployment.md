---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189211"
---
# <span data-ttu-id="0fe5b-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0fe5b-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="0fe5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe5b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe5b-103">Usuwa wdrożenie w zakresie dzierżawy i wszelkie skojarzone operacje.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="0fe5b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0fe5b-104">SYNTAX</span></span>

### <span data-ttu-id="0fe5b-105">RemoveByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0fe5b-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe5b-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0fe5b-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fe5b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="0fe5b-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe5b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0fe5b-108">DESCRIPTION</span></span>
<span data-ttu-id="0fe5b-109">Polecenie **cmdlet Remove-AzTenantDeployment** usuwa wdrożenie platformy Azure w bieżącym zakresie dzierżawy i wszystkie skojarzone operacje.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="0fe5b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0fe5b-110">EXAMPLES</span></span>

### <span data-ttu-id="0fe5b-111">Przykład 1. Usuwanie wdrożenia z podaną nazwą</span><span class="sxs-lookup"><span data-stu-id="0fe5b-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="0fe5b-112">To polecenie usuwa wdrożenie "RolesDeployment" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="0fe5b-113">Przykład 2. Uzyskaj wdrożenie i usuń je</span><span class="sxs-lookup"><span data-stu-id="0fe5b-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="0fe5b-114">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie dzierżawy i usuwa je.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="0fe5b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fe5b-115">PARAMETERS</span></span>

### <span data-ttu-id="0fe5b-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0fe5b-116">-AsJob</span></span>
<span data-ttu-id="0fe5b-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0fe5b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fe5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe5b-118">-DefaultProfile</span></span>
<span data-ttu-id="0fe5b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fe5b-120">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="0fe5b-120">-Id</span></span>
<span data-ttu-id="0fe5b-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0fe5b-122">przykład: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0fe5b-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="0fe5b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fe5b-123">-InputObject</span></span>
<span data-ttu-id="0fe5b-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-124">The deployment object.</span></span>

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

### <span data-ttu-id="0fe5b-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0fe5b-125">-Name</span></span>
<span data-ttu-id="0fe5b-126">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="0fe5b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fe5b-127">-PassThru</span></span>
<span data-ttu-id="0fe5b-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="0fe5b-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0fe5b-129">— Przed</span><span class="sxs-lookup"><span data-stu-id="0fe5b-129">-Pre</span></span>
<span data-ttu-id="0fe5b-130">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0fe5b-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0fe5b-131">-Confirm</span></span>
<span data-ttu-id="0fe5b-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe5b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe5b-133">-WhatIf</span></span>
<span data-ttu-id="0fe5b-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe5b-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe5b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe5b-136">CommonParameters</span></span>
<span data-ttu-id="0fe5b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe5b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe5b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fe5b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe5b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fe5b-139">INPUTS</span></span>

### <span data-ttu-id="0fe5b-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0fe5b-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0fe5b-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fe5b-141">OUTPUTS</span></span>

### <span data-ttu-id="0fe5b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0fe5b-142">System.Boolean</span></span>

## <span data-ttu-id="0fe5b-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0fe5b-143">NOTES</span></span>

## <span data-ttu-id="0fe5b-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fe5b-144">RELATED LINKS</span></span>
