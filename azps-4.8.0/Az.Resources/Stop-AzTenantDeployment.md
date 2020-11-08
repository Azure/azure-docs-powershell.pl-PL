---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219889"
---
# <span data-ttu-id="304e4-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="304e4-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="304e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="304e4-102">SYNOPSIS</span></span>
<span data-ttu-id="304e4-103">Anulowanie uruchomionego wdrożenia w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="304e4-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="304e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="304e4-104">SYNTAX</span></span>

### <span data-ttu-id="304e4-105">StopByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="304e4-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="304e4-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="304e4-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="304e4-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="304e4-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="304e4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="304e4-108">DESCRIPTION</span></span>
<span data-ttu-id="304e4-109">Polecenie cmdlet **stop-AzTenantDeployment** powoduje anulowanie wdrożenia, które zostało uruchomione, ale nie zostało ukończone w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="304e4-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="304e4-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="304e4-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="304e4-111">Aby utworzyć wdrożenie w zakresie dzierżawy, użyj polecenia cmdlet New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="304e4-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="304e4-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="304e4-112">EXAMPLES</span></span>

### <span data-ttu-id="304e4-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="304e4-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="304e4-114">To polecenie powoduje anulowanie uruchomionego wdrożenia "deployment01" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="304e4-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="304e4-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="304e4-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="304e4-116">To polecenie pobiera wdrożenie "deployment01" w bieżącym zakresie dzierżawy i anuluje je.</span><span class="sxs-lookup"><span data-stu-id="304e4-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="304e4-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="304e4-117">PARAMETERS</span></span>

### <span data-ttu-id="304e4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="304e4-118">-ApiVersion</span></span>
<span data-ttu-id="304e4-119">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="304e4-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="304e4-120">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="304e4-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="304e4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304e4-121">-DefaultProfile</span></span>
<span data-ttu-id="304e4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="304e4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="304e4-123">-ID</span><span class="sxs-lookup"><span data-stu-id="304e4-123">-Id</span></span>
<span data-ttu-id="304e4-124">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="304e4-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="304e4-125">przykład:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="304e4-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="304e4-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="304e4-126">-InputObject</span></span>
<span data-ttu-id="304e4-127">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="304e4-127">The deployment object.</span></span>

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

### <span data-ttu-id="304e4-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="304e4-128">-Name</span></span>
<span data-ttu-id="304e4-129">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="304e4-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304e4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="304e4-130">-PassThru</span></span>
<span data-ttu-id="304e4-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="304e4-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="304e4-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="304e4-132">-Pre</span></span>
<span data-ttu-id="304e4-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="304e4-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="304e4-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="304e4-134">-Confirm</span></span>
<span data-ttu-id="304e4-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="304e4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="304e4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="304e4-136">-WhatIf</span></span>
<span data-ttu-id="304e4-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="304e4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="304e4-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="304e4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="304e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304e4-139">CommonParameters</span></span>
<span data-ttu-id="304e4-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="304e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304e4-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="304e4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304e4-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="304e4-142">INPUTS</span></span>

### <span data-ttu-id="304e4-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="304e4-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="304e4-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="304e4-144">OUTPUTS</span></span>

### <span data-ttu-id="304e4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="304e4-145">System.Boolean</span></span>

## <span data-ttu-id="304e4-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="304e4-146">NOTES</span></span>

## <span data-ttu-id="304e4-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="304e4-147">RELATED LINKS</span></span>
