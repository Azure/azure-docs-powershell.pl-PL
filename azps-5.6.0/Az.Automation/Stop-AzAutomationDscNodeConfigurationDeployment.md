---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 726423dfcfef07142002cd40b29b6e4d26f91137
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978913"
---
# <span data-ttu-id="bad57-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bad57-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="bad57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bad57-102">SYNOPSIS</span></span>
<span data-ttu-id="bad57-103">Zatrzymuje wdrożenie konfiguracji węzła dsc w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="bad57-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="bad57-104">Powoduje jedynie zatrzymanie bieżącego zadania wdrażania, ale nie powoduje nieprzypisu już przypisanych konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="bad57-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="bad57-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bad57-105">SYNTAX</span></span>

### <span data-ttu-id="bad57-106">ByJobId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="bad57-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bad57-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bad57-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bad57-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bad57-108">DESCRIPTION</span></span>
<span data-ttu-id="bad57-109">Polecenie cmdlet **Stop-AzAutomationDscNodeConfigurationDeployment** zatrzymuje wdrożenie konfiguracji węzła żądanej konfiguracji województwa (DSC) w automatyzacji azure.</span><span class="sxs-lookup"><span data-stu-id="bad57-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="bad57-110">Wstrzymuje przypisywanie konfiguracji węzła do grup węzłów( jeśli są pozostałe do przypisania, ale nie powoduje przypisania już przypisanych węzłów).</span><span class="sxs-lookup"><span data-stu-id="bad57-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="bad57-111">Aby wyrejestrować zaplanowane zadanie, użyj funkcji [Wyrejestrowanie-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) z zadaniem JobScheduleId w celu przypisania istniejącego zaplanowanego zadania.</span><span class="sxs-lookup"><span data-stu-id="bad57-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="bad57-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bad57-112">EXAMPLES</span></span>

### <span data-ttu-id="bad57-113">Przykład 1. Wdrażanie konfiguracji węzła usługi Azure DSC w automatyzacji</span><span class="sxs-lookup"><span data-stu-id="bad57-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="bad57-114">Powyższe polecenie zatrzymuje zadanie wdrażania konfiguracji węzła DSC z przekazanym polem jobId.</span><span class="sxs-lookup"><span data-stu-id="bad57-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="bad57-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bad57-115">PARAMETERS</span></span>

### <span data-ttu-id="bad57-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bad57-116">-AutomationAccountName</span></span>
<span data-ttu-id="bad57-117">Określa nazwę konta automatyzacji zawierającego konfigurację dsc, która kompiluje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bad57-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bad57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bad57-118">-DefaultProfile</span></span>
<span data-ttu-id="bad57-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="bad57-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bad57-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="bad57-120">-Force</span></span>
<span data-ttu-id="bad57-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="bad57-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad57-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bad57-122">-InputObject</span></span>
<span data-ttu-id="bad57-123">Obiekt wejściowy dla funkcji Piping</span><span class="sxs-lookup"><span data-stu-id="bad57-123">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bad57-124">- JobId</span><span class="sxs-lookup"><span data-stu-id="bad57-124">-JobId</span></span>
<span data-ttu-id="bad57-125">Określa identyfikator zadania istniejącego zadania wdrażania.</span><span class="sxs-lookup"><span data-stu-id="bad57-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bad57-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bad57-126">-PassThru</span></span>
<span data-ttu-id="bad57-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="bad57-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bad57-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bad57-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bad57-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bad57-129">-ResourceGroupName</span></span>
<span data-ttu-id="bad57-130">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="bad57-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bad57-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bad57-131">-Confirm</span></span>
<span data-ttu-id="bad57-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bad57-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad57-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bad57-133">-WhatIf</span></span>
<span data-ttu-id="bad57-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bad57-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bad57-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bad57-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad57-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad57-136">CommonParameters</span></span>
<span data-ttu-id="bad57-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bad57-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad57-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad57-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad57-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bad57-139">INPUTS</span></span>

### <span data-ttu-id="bad57-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bad57-140">System.Guid</span></span>

### <span data-ttu-id="bad57-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bad57-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="bad57-142">System.String</span><span class="sxs-lookup"><span data-stu-id="bad57-142">System.String</span></span>

## <span data-ttu-id="bad57-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bad57-143">OUTPUTS</span></span>

### <span data-ttu-id="bad57-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bad57-144">System.Boolean</span></span>

## <span data-ttu-id="bad57-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bad57-145">NOTES</span></span>

## <span data-ttu-id="bad57-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bad57-146">RELATED LINKS</span></span>

[<span data-ttu-id="bad57-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="bad57-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="bad57-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="bad57-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="bad57-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bad57-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="bad57-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bad57-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="bad57-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="bad57-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
