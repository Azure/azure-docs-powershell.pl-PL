---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 794cc94ece2452f1fd5518d64d4071d7fa6ec326
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963754"
---
# <span data-ttu-id="0b130-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0b130-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="0b130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b130-102">SYNOPSIS</span></span>
<span data-ttu-id="0b130-103">Anulowanie uruchomionego wdrożenia</span><span class="sxs-lookup"><span data-stu-id="0b130-103">Cancel a running deployment</span></span>

## <span data-ttu-id="0b130-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b130-104">SYNTAX</span></span>

### <span data-ttu-id="0b130-105">StopByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0b130-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b130-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0b130-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b130-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b130-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b130-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b130-108">DESCRIPTION</span></span>
<span data-ttu-id="0b130-109">Polecenie **cmdlet Stop-AzDeployment** anuluje wdrożenie w zakresie subskrypcji, które zostało rozpoczęte, ale nie ukończone.</span><span class="sxs-lookup"><span data-stu-id="0b130-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="0b130-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niepełny stan inicjowania obsługi, taki jak inicjowanie obsługi administracyjnej, a nie stan ukończony, taki jak Inicjowanie obsługi administracyjnej lub Zakończone niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="0b130-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="0b130-111">Aby utworzyć wdrożenie w zakresie subskrypcji, użyj New-AzDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b130-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="0b130-112">To polecenie cmdlet zatrzymuje tylko jedno uruchomione wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="0b130-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="0b130-113">Użyj *parametru Name,* aby zatrzymać określone wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="0b130-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="0b130-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b130-114">EXAMPLES</span></span>

### <span data-ttu-id="0b130-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0b130-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="0b130-116">To polecenie anuluje uruchomione wdrożenie "deployment01" w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0b130-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="0b130-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0b130-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="0b130-118">To polecenie pobiera wdrożenie "deployment01" w bieżącym zakresie subskrypcji i anuluje je.</span><span class="sxs-lookup"><span data-stu-id="0b130-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="0b130-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b130-119">PARAMETERS</span></span>

### <span data-ttu-id="0b130-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b130-120">-DefaultProfile</span></span>
<span data-ttu-id="0b130-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b130-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b130-122">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="0b130-122">-Id</span></span>
<span data-ttu-id="0b130-123">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0b130-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0b130-124">przykład: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0b130-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="0b130-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b130-125">-InputObject</span></span>
<span data-ttu-id="0b130-126">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0b130-126">The deployment object.</span></span>

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

### <span data-ttu-id="0b130-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0b130-127">-Name</span></span>
<span data-ttu-id="0b130-128">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0b130-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="0b130-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b130-129">-PassThru</span></span>
<span data-ttu-id="0b130-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0b130-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0b130-131">— Przed</span><span class="sxs-lookup"><span data-stu-id="0b130-131">-Pre</span></span>
<span data-ttu-id="0b130-132">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0b130-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0b130-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b130-133">-Confirm</span></span>
<span data-ttu-id="0b130-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0b130-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b130-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b130-135">-WhatIf</span></span>
<span data-ttu-id="0b130-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b130-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b130-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0b130-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b130-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b130-138">CommonParameters</span></span>
<span data-ttu-id="0b130-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b130-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b130-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b130-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b130-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b130-141">INPUTS</span></span>

### <span data-ttu-id="0b130-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0b130-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0b130-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b130-143">OUTPUTS</span></span>

### <span data-ttu-id="0b130-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b130-144">System.Boolean</span></span>

## <span data-ttu-id="0b130-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b130-145">NOTES</span></span>

## <span data-ttu-id="0b130-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b130-146">RELATED LINKS</span></span>
