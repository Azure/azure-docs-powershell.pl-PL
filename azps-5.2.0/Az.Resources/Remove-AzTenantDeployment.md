---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354805"
---
# <span data-ttu-id="a5998-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a5998-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="a5998-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5998-102">SYNOPSIS</span></span>
<span data-ttu-id="a5998-103">Usuwa wdrożenie w zakresie dzierżawy i wszystkie skojarzone operacje</span><span class="sxs-lookup"><span data-stu-id="a5998-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="a5998-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5998-104">SYNTAX</span></span>

### <span data-ttu-id="a5998-105">RemoveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5998-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5998-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a5998-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5998-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5998-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5998-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a5998-108">DESCRIPTION</span></span>
<span data-ttu-id="a5998-109">Polecenie cmdlet **Remove-AzTenantDeployment** usuwa wdrożenie platformy Azure w bieżącym zakresie dzierżawy i wszystkich skojarzonych operacjach.</span><span class="sxs-lookup"><span data-stu-id="a5998-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="a5998-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5998-110">EXAMPLES</span></span>

### <span data-ttu-id="a5998-111">Przykład 1: usunięcie wdrożenia o danej nazwie</span><span class="sxs-lookup"><span data-stu-id="a5998-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="a5998-112">To polecenie powoduje usunięcie wdrożenia "RolesDeployment" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="a5998-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="a5998-113">Przykład 2: uzyskiwanie wdrożenia i usuwanie go</span><span class="sxs-lookup"><span data-stu-id="a5998-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="a5998-114">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie dzierżawy i usuwa je.</span><span class="sxs-lookup"><span data-stu-id="a5998-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="a5998-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5998-115">PARAMETERS</span></span>

### <span data-ttu-id="a5998-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5998-116">-AsJob</span></span>
<span data-ttu-id="a5998-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a5998-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5998-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5998-118">-DefaultProfile</span></span>
<span data-ttu-id="a5998-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5998-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5998-120">-ID</span><span class="sxs-lookup"><span data-stu-id="a5998-120">-Id</span></span>
<span data-ttu-id="a5998-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a5998-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a5998-122">przykład:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="a5998-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="a5998-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5998-123">-InputObject</span></span>
<span data-ttu-id="a5998-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a5998-124">The deployment object.</span></span>

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

### <span data-ttu-id="a5998-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5998-125">-Name</span></span>
<span data-ttu-id="a5998-126">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a5998-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="a5998-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5998-127">-PassThru</span></span>
<span data-ttu-id="a5998-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a5998-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a5998-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="a5998-129">-Pre</span></span>
<span data-ttu-id="a5998-130">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="a5998-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a5998-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5998-131">-Confirm</span></span>
<span data-ttu-id="a5998-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5998-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5998-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5998-133">-WhatIf</span></span>
<span data-ttu-id="a5998-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5998-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5998-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5998-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5998-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5998-136">CommonParameters</span></span>
<span data-ttu-id="a5998-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5998-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5998-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5998-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5998-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5998-139">INPUTS</span></span>

### <span data-ttu-id="a5998-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a5998-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a5998-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5998-141">OUTPUTS</span></span>

### <span data-ttu-id="a5998-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5998-142">System.Boolean</span></span>

## <span data-ttu-id="a5998-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5998-143">NOTES</span></span>

## <span data-ttu-id="a5998-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5998-144">RELATED LINKS</span></span>
