---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062120"
---
# <span data-ttu-id="02dd7-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="02dd7-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="02dd7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="02dd7-103">Usunięcie wdrożenia w grupie zarządzania i wszelkich skojarzonych operacjach</span><span class="sxs-lookup"><span data-stu-id="02dd7-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="02dd7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02dd7-104">SYNTAX</span></span>

### <span data-ttu-id="02dd7-105">RemoveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02dd7-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02dd7-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="02dd7-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02dd7-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="02dd7-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02dd7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="02dd7-108">DESCRIPTION</span></span>
<span data-ttu-id="02dd7-109">Polecenie cmdlet **Remove-AzManagementGroupDeployment** powoduje usunięcie wdrożenia platformy Azure w grupie zarządzania i wszelkich skojarzonych operacjach.</span><span class="sxs-lookup"><span data-stu-id="02dd7-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="02dd7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02dd7-110">EXAMPLES</span></span>

### <span data-ttu-id="02dd7-111">Przykład 1: usunięcie wdrożenia o danej nazwie</span><span class="sxs-lookup"><span data-stu-id="02dd7-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="02dd7-112">To polecenie powoduje usunięcie wdrożenia "RolesDeployment" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="02dd7-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="02dd7-113">Przykład 2: uzyskiwanie wdrożenia i usuwanie go</span><span class="sxs-lookup"><span data-stu-id="02dd7-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="02dd7-114">To polecenie pobiera wdrożenie "RolesDeployment" w grupie zarządzania "myMG" i usuwa je.</span><span class="sxs-lookup"><span data-stu-id="02dd7-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="02dd7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02dd7-115">PARAMETERS</span></span>

### <span data-ttu-id="02dd7-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="02dd7-116">-ApiVersion</span></span>
<span data-ttu-id="02dd7-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="02dd7-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="02dd7-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="02dd7-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="02dd7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02dd7-119">-AsJob</span></span>
<span data-ttu-id="02dd7-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="02dd7-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02dd7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02dd7-121">-DefaultProfile</span></span>
<span data-ttu-id="02dd7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02dd7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02dd7-123">-ID</span><span class="sxs-lookup"><span data-stu-id="02dd7-123">-Id</span></span>
<span data-ttu-id="02dd7-124">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="02dd7-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="02dd7-125">przykład:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="02dd7-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dd7-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="02dd7-126">-InputObject</span></span>
<span data-ttu-id="02dd7-127">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="02dd7-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02dd7-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="02dd7-128">-ManagementGroupId</span></span>
<span data-ttu-id="02dd7-129">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="02dd7-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dd7-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02dd7-130">-Name</span></span>
<span data-ttu-id="02dd7-131">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="02dd7-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02dd7-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02dd7-132">-PassThru</span></span>
<span data-ttu-id="02dd7-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="02dd7-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="02dd7-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="02dd7-134">-Pre</span></span>
<span data-ttu-id="02dd7-135">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="02dd7-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="02dd7-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02dd7-136">-Confirm</span></span>
<span data-ttu-id="02dd7-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02dd7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02dd7-138">-WhatIf</span></span>
<span data-ttu-id="02dd7-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02dd7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02dd7-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02dd7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02dd7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02dd7-141">CommonParameters</span></span>
<span data-ttu-id="02dd7-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02dd7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02dd7-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02dd7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02dd7-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02dd7-144">INPUTS</span></span>

### <span data-ttu-id="02dd7-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="02dd7-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="02dd7-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02dd7-146">OUTPUTS</span></span>

### <span data-ttu-id="02dd7-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02dd7-147">System.Boolean</span></span>

## <span data-ttu-id="02dd7-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02dd7-148">NOTES</span></span>

## <span data-ttu-id="02dd7-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02dd7-149">RELATED LINKS</span></span>
