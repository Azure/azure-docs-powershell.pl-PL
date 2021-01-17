---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490266"
---
# <span data-ttu-id="de58c-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="de58c-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="de58c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de58c-102">SYNOPSIS</span></span>
<span data-ttu-id="de58c-103">Anulowanie uruchomionego wdrożenia w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="de58c-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="de58c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de58c-104">SYNTAX</span></span>

### <span data-ttu-id="de58c-105">StopByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de58c-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de58c-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="de58c-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de58c-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="de58c-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de58c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="de58c-108">DESCRIPTION</span></span>
<span data-ttu-id="de58c-109">Polecenie cmdlet **stop-AzTenantDeployment** powoduje anulowanie wdrożenia, które zostało uruchomione, ale nie zostało ukończone w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="de58c-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="de58c-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="de58c-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="de58c-111">Aby utworzyć wdrożenie w zakresie dzierżawy, użyj polecenia cmdlet New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="de58c-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="de58c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de58c-112">EXAMPLES</span></span>

### <span data-ttu-id="de58c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de58c-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="de58c-114">To polecenie powoduje anulowanie uruchomionego wdrożenia "deployment01" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="de58c-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="de58c-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="de58c-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="de58c-116">To polecenie pobiera wdrożenie "deployment01" w bieżącym zakresie dzierżawy i anuluje je.</span><span class="sxs-lookup"><span data-stu-id="de58c-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="de58c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de58c-117">PARAMETERS</span></span>

### <span data-ttu-id="de58c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de58c-118">-DefaultProfile</span></span>
<span data-ttu-id="de58c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de58c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de58c-120">-ID</span><span class="sxs-lookup"><span data-stu-id="de58c-120">-Id</span></span>
<span data-ttu-id="de58c-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="de58c-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="de58c-122">przykład:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="de58c-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="de58c-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="de58c-123">-InputObject</span></span>
<span data-ttu-id="de58c-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="de58c-124">The deployment object.</span></span>

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

### <span data-ttu-id="de58c-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de58c-125">-Name</span></span>
<span data-ttu-id="de58c-126">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="de58c-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="de58c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de58c-127">-PassThru</span></span>
<span data-ttu-id="de58c-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="de58c-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="de58c-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="de58c-129">-Pre</span></span>
<span data-ttu-id="de58c-130">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="de58c-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="de58c-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de58c-131">-Confirm</span></span>
<span data-ttu-id="de58c-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de58c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de58c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de58c-133">-WhatIf</span></span>
<span data-ttu-id="de58c-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de58c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de58c-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de58c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de58c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de58c-136">CommonParameters</span></span>
<span data-ttu-id="de58c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de58c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de58c-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de58c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de58c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de58c-139">INPUTS</span></span>

### <span data-ttu-id="de58c-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="de58c-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="de58c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de58c-141">OUTPUTS</span></span>

### <span data-ttu-id="de58c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de58c-142">System.Boolean</span></span>

## <span data-ttu-id="de58c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de58c-143">NOTES</span></span>

## <span data-ttu-id="de58c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de58c-144">RELATED LINKS</span></span>
