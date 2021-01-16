---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355537"
---
# <span data-ttu-id="74465-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="74465-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="74465-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74465-102">SYNOPSIS</span></span>
<span data-ttu-id="74465-103">Usunięcie wdrożenia w grupie zarządzania i wszelkich skojarzonych operacjach</span><span class="sxs-lookup"><span data-stu-id="74465-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="74465-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74465-104">SYNTAX</span></span>

### <span data-ttu-id="74465-105">RemoveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="74465-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74465-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="74465-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74465-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="74465-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74465-108">Opis</span><span class="sxs-lookup"><span data-stu-id="74465-108">DESCRIPTION</span></span>
<span data-ttu-id="74465-109">Polecenie cmdlet **Remove-AzManagementGroupDeployment** powoduje usunięcie wdrożenia platformy Azure w grupie zarządzania i wszelkich skojarzonych operacjach.</span><span class="sxs-lookup"><span data-stu-id="74465-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="74465-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74465-110">EXAMPLES</span></span>

### <span data-ttu-id="74465-111">Przykład 1: usunięcie wdrożenia o danej nazwie</span><span class="sxs-lookup"><span data-stu-id="74465-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="74465-112">To polecenie powoduje usunięcie wdrożenia "RolesDeployment" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="74465-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="74465-113">Przykład 2: uzyskiwanie wdrożenia i usuwanie go</span><span class="sxs-lookup"><span data-stu-id="74465-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="74465-114">To polecenie pobiera wdrożenie "RolesDeployment" w grupie zarządzania "myMG" i usuwa je.</span><span class="sxs-lookup"><span data-stu-id="74465-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="74465-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74465-115">PARAMETERS</span></span>

### <span data-ttu-id="74465-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74465-116">-AsJob</span></span>
<span data-ttu-id="74465-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="74465-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74465-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74465-118">-DefaultProfile</span></span>
<span data-ttu-id="74465-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74465-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74465-120">-ID</span><span class="sxs-lookup"><span data-stu-id="74465-120">-Id</span></span>
<span data-ttu-id="74465-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="74465-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="74465-122">przykład:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="74465-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="74465-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74465-123">-InputObject</span></span>
<span data-ttu-id="74465-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="74465-124">The deployment object.</span></span>

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

### <span data-ttu-id="74465-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="74465-125">-ManagementGroupId</span></span>
<span data-ttu-id="74465-126">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="74465-126">The management group id.</span></span>

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

### <span data-ttu-id="74465-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74465-127">-Name</span></span>
<span data-ttu-id="74465-128">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="74465-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="74465-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74465-129">-PassThru</span></span>
<span data-ttu-id="74465-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="74465-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="74465-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="74465-131">-Pre</span></span>
<span data-ttu-id="74465-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="74465-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="74465-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74465-133">-Confirm</span></span>
<span data-ttu-id="74465-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74465-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74465-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74465-135">-WhatIf</span></span>
<span data-ttu-id="74465-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74465-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74465-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74465-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74465-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74465-138">CommonParameters</span></span>
<span data-ttu-id="74465-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74465-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74465-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74465-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74465-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74465-141">INPUTS</span></span>

### <span data-ttu-id="74465-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="74465-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="74465-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74465-143">OUTPUTS</span></span>

### <span data-ttu-id="74465-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74465-144">System.Boolean</span></span>

## <span data-ttu-id="74465-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74465-145">NOTES</span></span>

## <span data-ttu-id="74465-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74465-146">RELATED LINKS</span></span>
