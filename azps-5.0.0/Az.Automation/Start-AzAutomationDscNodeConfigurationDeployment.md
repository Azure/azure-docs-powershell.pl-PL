---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308562"
---
# <span data-ttu-id="ae815-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ae815-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="ae815-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae815-102">SYNOPSIS</span></span>
<span data-ttu-id="ae815-103">Wdrażanie konfiguracji węzła DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="ae815-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="ae815-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae815-104">SYNTAX</span></span>

### <span data-ttu-id="ae815-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ae815-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae815-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ae815-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae815-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ae815-107">DESCRIPTION</span></span>
<span data-ttu-id="ae815-108">Polecenie cmdlet **Start-AzAutomationDscNodeConfigurationDeployment** wdraża konfigurację węzła konfiguracji stanu (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ae815-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="ae815-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae815-109">EXAMPLES</span></span>

### <span data-ttu-id="ae815-110">Przykład 1: wdrażanie konfiguracji węzła usługi Azure DSC w automatyzacji</span><span class="sxs-lookup"><span data-stu-id="ae815-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="ae815-111">Powyższe polecenie wdraża konfigurację węzła DSC o nazwie "Config01. Node1" na podstawie dwuwymiarowej tablicy nazw węzłów.</span><span class="sxs-lookup"><span data-stu-id="ae815-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="ae815-112">Wdrożenie przebiega w sposób stopniowy.</span><span class="sxs-lookup"><span data-stu-id="ae815-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="ae815-113">Przykład 2: Planowanie wdrożenia konfiguracji węzła platformy Azure DSC w automatyzacji</span><span class="sxs-lookup"><span data-stu-id="ae815-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="ae815-114">Powyższe polecenie planuje wdrożenie konfiguracji węzła DSC o nazwie "Config01. Node1" na podstawie dwuwymiarowej tablicy nazw węzłów.</span><span class="sxs-lookup"><span data-stu-id="ae815-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="ae815-115">Wdrożenie przebiega w sposób stopniowy i zostanie wykonany na podstawie harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="ae815-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="ae815-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae815-116">PARAMETERS</span></span>

### <span data-ttu-id="ae815-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ae815-117">-AutomationAccountName</span></span>
<span data-ttu-id="ae815-118">Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą jest kompilowany to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae815-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="ae815-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae815-119">-DefaultProfile</span></span>
<span data-ttu-id="ae815-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ae815-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae815-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ae815-121">-Force</span></span>
<span data-ttu-id="ae815-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="ae815-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae815-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ae815-123">-InputObject</span></span>
<span data-ttu-id="ae815-124">Obiekt wejściowy dla połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="ae815-124">Input object for Piping</span></span>

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

### <span data-ttu-id="ae815-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ae815-125">-NodeConfigurationName</span></span>
<span data-ttu-id="ae815-126">Określa nazwę konfiguracji węzła DSC, którą to polecenie cmdlet wdraża.</span><span class="sxs-lookup"><span data-stu-id="ae815-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae815-127">-Nodename</span><span class="sxs-lookup"><span data-stu-id="ae815-127">-NodeName</span></span>
<span data-ttu-id="ae815-128">Określa nazwy węzłów, na których ma zostać wdrożona konfiguracja węzła.</span><span class="sxs-lookup"><span data-stu-id="ae815-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae815-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae815-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae815-130">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="ae815-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="ae815-131">-Schedule</span><span class="sxs-lookup"><span data-stu-id="ae815-131">-Schedule</span></span>
<span data-ttu-id="ae815-132">Obiekt harmonogramu automatyzacji umożliwiający zaplanowanie zadania wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ae815-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae815-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae815-133">-Confirm</span></span>
<span data-ttu-id="ae815-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae815-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae815-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae815-135">-WhatIf</span></span>
<span data-ttu-id="ae815-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae815-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae815-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae815-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae815-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae815-138">CommonParameters</span></span>
<span data-ttu-id="ae815-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae815-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae815-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae815-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae815-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae815-141">INPUTS</span></span>

### <span data-ttu-id="ae815-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ae815-142">System.String</span></span>

### <span data-ttu-id="ae815-143">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ae815-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="ae815-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae815-144">OUTPUTS</span></span>

### <span data-ttu-id="ae815-145">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ae815-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="ae815-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae815-146">NOTES</span></span>

## <span data-ttu-id="ae815-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae815-147">RELATED LINKS</span></span>

[<span data-ttu-id="ae815-148">Start — AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ae815-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="ae815-149">Import — AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae815-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ae815-150">Zatrzymaj — AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ae815-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ae815-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ae815-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ae815-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="ae815-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="ae815-153">Nowe — AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ae815-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
