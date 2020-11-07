---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 15dc9e6a24aa78523a020af541250c5c51b32994
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708266"
---
# <span data-ttu-id="23637-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="23637-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="23637-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23637-102">SYNOPSIS</span></span>
<span data-ttu-id="23637-103">Cancal uruchomione wdrożenie</span><span class="sxs-lookup"><span data-stu-id="23637-103">Cancal a running deployment</span></span>

## <span data-ttu-id="23637-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23637-104">SYNTAX</span></span>

### <span data-ttu-id="23637-105">StopByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23637-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23637-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="23637-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23637-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="23637-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23637-108">Opis</span><span class="sxs-lookup"><span data-stu-id="23637-108">DESCRIPTION</span></span>
<span data-ttu-id="23637-109">Polecenie cmdlet **stop-AzDeployment** anuluje wdrożenie w zakresie subskrypcji, który rozpoczął się, ale nie został ukończony.</span><span class="sxs-lookup"><span data-stu-id="23637-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="23637-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="23637-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="23637-111">Aby utworzyć wdrożenie w zakresie abonamentu, użyj polecenia cmdlet New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="23637-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="23637-112">To polecenie cmdlet powoduje zatrzymanie tylko jednego uruchomionego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="23637-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="23637-113">Użyj parametru *name* , aby zatrzymać określone wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="23637-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="23637-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23637-114">EXAMPLES</span></span>

### <span data-ttu-id="23637-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23637-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="23637-116">To polecenie powoduje anulowanie uruchomionego wdrożenia "deployment01" w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23637-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="23637-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="23637-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="23637-118">To polecenie pobiera wdrożenie "deployment01" w bieżącym zakresie subskrypcji i anuluje je.</span><span class="sxs-lookup"><span data-stu-id="23637-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="23637-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23637-119">PARAMETERS</span></span>

### <span data-ttu-id="23637-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23637-120">-ApiVersion</span></span>
<span data-ttu-id="23637-121">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="23637-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="23637-122">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="23637-122">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23637-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23637-123">-DefaultProfile</span></span>
<span data-ttu-id="23637-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23637-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23637-125">-ID</span><span class="sxs-lookup"><span data-stu-id="23637-125">-Id</span></span>
<span data-ttu-id="23637-126">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="23637-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="23637-127">przykład:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="23637-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="23637-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23637-128">-InputObject</span></span>
<span data-ttu-id="23637-129">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="23637-129">The deployment object.</span></span>

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

### <span data-ttu-id="23637-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23637-130">-Name</span></span>
<span data-ttu-id="23637-131">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="23637-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="23637-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23637-132">-PassThru</span></span>
<span data-ttu-id="23637-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="23637-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="23637-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="23637-134">-Pre</span></span>
<span data-ttu-id="23637-135">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="23637-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="23637-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23637-136">-Confirm</span></span>
<span data-ttu-id="23637-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23637-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23637-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23637-138">-WhatIf</span></span>
<span data-ttu-id="23637-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23637-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23637-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23637-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23637-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23637-141">CommonParameters</span></span>
<span data-ttu-id="23637-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23637-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23637-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23637-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23637-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23637-144">INPUTS</span></span>

### <span data-ttu-id="23637-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="23637-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="23637-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23637-146">OUTPUTS</span></span>

### <span data-ttu-id="23637-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23637-147">System.Boolean</span></span>

## <span data-ttu-id="23637-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23637-148">NOTES</span></span>

## <span data-ttu-id="23637-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23637-149">RELATED LINKS</span></span>
