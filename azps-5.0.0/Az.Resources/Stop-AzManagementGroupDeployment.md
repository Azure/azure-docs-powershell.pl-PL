---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231498"
---
# <span data-ttu-id="fdb07-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fdb07-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="fdb07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fdb07-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb07-103">Anulowanie uruchomionego wdrożenia w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="fdb07-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="fdb07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fdb07-104">SYNTAX</span></span>

### <span data-ttu-id="fdb07-105">StopByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fdb07-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb07-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="fdb07-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb07-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="fdb07-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb07-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fdb07-108">DESCRIPTION</span></span>
<span data-ttu-id="fdb07-109">Polecenie cmdlet **stop-AzManagementGroupDeployment** powoduje anulowanie wdrożenia, które zostało uruchomione, ale nie zostało ukończone w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="fdb07-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="fdb07-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="fdb07-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="fdb07-111">Aby utworzyć wdrożenie w grupie zarządzania, użyj polecenia cmdlet New-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="fdb07-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="fdb07-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fdb07-112">EXAMPLES</span></span>

### <span data-ttu-id="fdb07-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fdb07-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="fdb07-114">To polecenie powoduje anulowanie uruchomionego wdrożenia "deployment01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="fdb07-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="fdb07-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fdb07-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="fdb07-116">To polecenie pobiera wdrożenie "deployment01" w grupie zarządzania "myMG" i anuluje je.</span><span class="sxs-lookup"><span data-stu-id="fdb07-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="fdb07-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fdb07-117">PARAMETERS</span></span>

### <span data-ttu-id="fdb07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb07-118">-DefaultProfile</span></span>
<span data-ttu-id="fdb07-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb07-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb07-120">-ID</span><span class="sxs-lookup"><span data-stu-id="fdb07-120">-Id</span></span>
<span data-ttu-id="fdb07-121">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="fdb07-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="fdb07-122">przykład:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="fdb07-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="fdb07-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fdb07-123">-InputObject</span></span>
<span data-ttu-id="fdb07-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="fdb07-124">The deployment object.</span></span>

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

### <span data-ttu-id="fdb07-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="fdb07-125">-ManagementGroupId</span></span>
<span data-ttu-id="fdb07-126">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="fdb07-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb07-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fdb07-127">-Name</span></span>
<span data-ttu-id="fdb07-128">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="fdb07-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb07-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdb07-129">-PassThru</span></span>
<span data-ttu-id="fdb07-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fdb07-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="fdb07-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="fdb07-131">-Pre</span></span>
<span data-ttu-id="fdb07-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="fdb07-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fdb07-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fdb07-133">-Confirm</span></span>
<span data-ttu-id="fdb07-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb07-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb07-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb07-135">-WhatIf</span></span>
<span data-ttu-id="fdb07-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdb07-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdb07-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fdb07-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb07-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb07-138">CommonParameters</span></span>
<span data-ttu-id="fdb07-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb07-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb07-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdb07-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb07-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fdb07-141">INPUTS</span></span>

### <span data-ttu-id="fdb07-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="fdb07-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="fdb07-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fdb07-143">OUTPUTS</span></span>

### <span data-ttu-id="fdb07-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fdb07-144">System.Boolean</span></span>

## <span data-ttu-id="fdb07-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fdb07-145">NOTES</span></span>

## <span data-ttu-id="fdb07-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fdb07-146">RELATED LINKS</span></span>
