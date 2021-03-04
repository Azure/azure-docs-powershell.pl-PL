---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: e6948bf1868865bb53bd3e1bfabc68aded44cd4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967601"
---
# <span data-ttu-id="02b98-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="02b98-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="02b98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02b98-102">SYNOPSIS</span></span>
<span data-ttu-id="02b98-103">Anulowanie uruchomionego wdrożenia w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="02b98-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="02b98-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="02b98-104">SYNTAX</span></span>

### <span data-ttu-id="02b98-105">StopByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="02b98-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b98-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="02b98-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02b98-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="02b98-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02b98-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="02b98-108">DESCRIPTION</span></span>
<span data-ttu-id="02b98-109">Polecenie **cmdlet Stop-AzTenantDeployment** anuluje wdrożenie, które rozpoczęło się, ale nie zakończyło się w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="02b98-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="02b98-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niepełny stan inicjowania obsługi, taki jak inicjowanie obsługi administracyjnej, a nie stan ukończony, taki jak Inicjowanie obsługi administracyjnej lub Zakończone niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="02b98-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="02b98-111">Aby utworzyć wdrożenie w zakresie dzierżawy, użyj New-AzTenantDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02b98-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="02b98-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="02b98-112">EXAMPLES</span></span>

### <span data-ttu-id="02b98-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02b98-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="02b98-114">To polecenie anuluje uruchomione wdrożenie "wdrożenie01" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="02b98-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="02b98-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="02b98-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="02b98-116">To polecenie pobiera wdrożenie "deployment01" w bieżącym zakresie dzierżawy i anuluje je.</span><span class="sxs-lookup"><span data-stu-id="02b98-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="02b98-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02b98-117">PARAMETERS</span></span>

### <span data-ttu-id="02b98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b98-118">-DefaultProfile</span></span>
<span data-ttu-id="02b98-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="02b98-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02b98-120">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="02b98-120">-Id</span></span>
<span data-ttu-id="02b98-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="02b98-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="02b98-122">przykład: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="02b98-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="02b98-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02b98-123">-InputObject</span></span>
<span data-ttu-id="02b98-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="02b98-124">The deployment object.</span></span>

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

### <span data-ttu-id="02b98-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="02b98-125">-Name</span></span>
<span data-ttu-id="02b98-126">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="02b98-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b98-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02b98-127">-PassThru</span></span>
<span data-ttu-id="02b98-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="02b98-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="02b98-129">— Przed</span><span class="sxs-lookup"><span data-stu-id="02b98-129">-Pre</span></span>
<span data-ttu-id="02b98-130">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="02b98-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="02b98-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02b98-131">-Confirm</span></span>
<span data-ttu-id="02b98-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02b98-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02b98-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b98-133">-WhatIf</span></span>
<span data-ttu-id="02b98-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02b98-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02b98-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="02b98-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02b98-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b98-136">CommonParameters</span></span>
<span data-ttu-id="02b98-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02b98-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b98-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02b98-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b98-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02b98-139">INPUTS</span></span>

### <span data-ttu-id="02b98-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="02b98-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="02b98-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02b98-141">OUTPUTS</span></span>

### <span data-ttu-id="02b98-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02b98-142">System.Boolean</span></span>

## <span data-ttu-id="02b98-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="02b98-143">NOTES</span></span>

## <span data-ttu-id="02b98-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02b98-144">RELATED LINKS</span></span>
