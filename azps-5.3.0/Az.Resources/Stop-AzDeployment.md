---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490273"
---
# <span data-ttu-id="5bf5a-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5bf5a-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="5bf5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5bf5a-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf5a-103">Anulowanie uruchomionego wdrożenia</span><span class="sxs-lookup"><span data-stu-id="5bf5a-103">Cancel a running deployment</span></span>

## <span data-ttu-id="5bf5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5bf5a-104">SYNTAX</span></span>

### <span data-ttu-id="5bf5a-105">StopByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5bf5a-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf5a-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5bf5a-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf5a-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="5bf5a-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf5a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5bf5a-108">DESCRIPTION</span></span>
<span data-ttu-id="5bf5a-109">Polecenie cmdlet **stop-AzDeployment** anuluje wdrożenie w zakresie subskrypcji, który rozpoczął się, ale nie został ukończony.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="5bf5a-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="5bf5a-111">Aby utworzyć wdrożenie w zakresie abonamentu, użyj polecenia cmdlet New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="5bf5a-112">To polecenie cmdlet powoduje zatrzymanie tylko jednego uruchomionego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="5bf5a-113">Użyj parametru *name* , aby zatrzymać określone wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="5bf5a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5bf5a-114">EXAMPLES</span></span>

### <span data-ttu-id="5bf5a-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5bf5a-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="5bf5a-116">To polecenie powoduje anulowanie uruchomionego wdrożenia "deployment01" w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="5bf5a-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5bf5a-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="5bf5a-118">To polecenie pobiera wdrożenie "deployment01" w bieżącym zakresie subskrypcji i anuluje je.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="5bf5a-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5bf5a-119">PARAMETERS</span></span>

### <span data-ttu-id="5bf5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf5a-120">-DefaultProfile</span></span>
<span data-ttu-id="5bf5a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bf5a-122">-ID</span><span class="sxs-lookup"><span data-stu-id="5bf5a-122">-Id</span></span>
<span data-ttu-id="5bf5a-123">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="5bf5a-124">przykład:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="5bf5a-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="5bf5a-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5bf5a-125">-InputObject</span></span>
<span data-ttu-id="5bf5a-126">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-126">The deployment object.</span></span>

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

### <span data-ttu-id="5bf5a-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5bf5a-127">-Name</span></span>
<span data-ttu-id="5bf5a-128">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="5bf5a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bf5a-129">-PassThru</span></span>
<span data-ttu-id="5bf5a-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5bf5a-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5bf5a-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="5bf5a-131">-Pre</span></span>
<span data-ttu-id="5bf5a-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5bf5a-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5bf5a-133">-Confirm</span></span>
<span data-ttu-id="5bf5a-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf5a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf5a-135">-WhatIf</span></span>
<span data-ttu-id="5bf5a-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf5a-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf5a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf5a-138">CommonParameters</span></span>
<span data-ttu-id="5bf5a-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf5a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf5a-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bf5a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf5a-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bf5a-141">INPUTS</span></span>

### <span data-ttu-id="5bf5a-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="5bf5a-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5bf5a-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5bf5a-143">OUTPUTS</span></span>

### <span data-ttu-id="5bf5a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf5a-144">System.Boolean</span></span>

## <span data-ttu-id="5bf5a-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5bf5a-145">NOTES</span></span>

## <span data-ttu-id="5bf5a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bf5a-146">RELATED LINKS</span></span>
