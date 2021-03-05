---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: f5cbb59ffbd5b79087e9f338788dde9d1176f4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995730"
---
# <span data-ttu-id="99234-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="99234-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="99234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99234-102">SYNOPSIS</span></span>
<span data-ttu-id="99234-103">Pobiera wdrożenia konfiguracji węzła dsc w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="99234-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="99234-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99234-104">SYNTAX</span></span>

### <span data-ttu-id="99234-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="99234-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99234-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="99234-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99234-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="99234-107">DESCRIPTION</span></span>
<span data-ttu-id="99234-108">Polecenie **cmdlet Get-AzAutomationDscNodeConfigurationDeployment** wdraża konfigurację węzła APS Desired State Configuration (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="99234-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="99234-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99234-109">EXAMPLES</span></span>

### <span data-ttu-id="99234-110">Przykład 1. Uzyskiwanie wdrożenia konfiguracji węzła</span><span class="sxs-lookup"><span data-stu-id="99234-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="99234-111">Powyższe polecenie wdraża konfigurację węzła DSC o nazwie "Config01.Node1" w podanej dwuwymiarowej tablicy nazw węzła.</span><span class="sxs-lookup"><span data-stu-id="99234-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="99234-112">Wdrożenie jest etapowe.</span><span class="sxs-lookup"><span data-stu-id="99234-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="99234-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99234-113">PARAMETERS</span></span>

### <span data-ttu-id="99234-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="99234-114">-AutomationAccountName</span></span>
<span data-ttu-id="99234-115">Określa nazwę konta automatyzacji zawierającego konfigurację DSC kompilacyjną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99234-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="99234-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99234-116">-DefaultProfile</span></span>
<span data-ttu-id="99234-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="99234-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99234-118">- EndTime</span><span class="sxs-lookup"><span data-stu-id="99234-118">-EndTime</span></span>
<span data-ttu-id="99234-119">Filtr czasu zakończenia.</span><span class="sxs-lookup"><span data-stu-id="99234-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99234-120">- JobId</span><span class="sxs-lookup"><span data-stu-id="99234-120">-JobId</span></span>
<span data-ttu-id="99234-121">Określa identyfikator zadania istniejącego zadania wdrażania.</span><span class="sxs-lookup"><span data-stu-id="99234-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="99234-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99234-122">-ResourceGroupName</span></span>
<span data-ttu-id="99234-123">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="99234-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="99234-124">— StartTime</span><span class="sxs-lookup"><span data-stu-id="99234-124">-StartTime</span></span>
<span data-ttu-id="99234-125">Filtr czasu rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="99234-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99234-126">— Status</span><span class="sxs-lookup"><span data-stu-id="99234-126">-Status</span></span>
<span data-ttu-id="99234-127">Stan filtru Zadanie.</span><span class="sxs-lookup"><span data-stu-id="99234-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99234-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99234-128">CommonParameters</span></span>
<span data-ttu-id="99234-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99234-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99234-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99234-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99234-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99234-131">INPUTS</span></span>

### <span data-ttu-id="99234-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="99234-132">System.Guid</span></span>

### <span data-ttu-id="99234-133">System.String</span><span class="sxs-lookup"><span data-stu-id="99234-133">System.String</span></span>

## <span data-ttu-id="99234-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99234-134">OUTPUTS</span></span>

### <span data-ttu-id="99234-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="99234-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="99234-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99234-136">NOTES</span></span>

## <span data-ttu-id="99234-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99234-137">RELATED LINKS</span></span>

[<span data-ttu-id="99234-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="99234-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="99234-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="99234-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="99234-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="99234-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="99234-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="99234-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="99234-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="99234-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
