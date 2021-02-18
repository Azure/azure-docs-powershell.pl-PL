---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: bc98d8ed8773e49eab594a4d715bef3f93862e83
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239635"
---
# <span data-ttu-id="367d4-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="367d4-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="367d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="367d4-102">SYNOPSIS</span></span>
<span data-ttu-id="367d4-103">Pobiera harmonogram zadania wdrożenia węzła dsc w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="367d4-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="367d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="367d4-104">SYNTAX</span></span>

### <span data-ttu-id="367d4-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="367d4-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="367d4-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="367d4-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="367d4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="367d4-107">DESCRIPTION</span></span>
<span data-ttu-id="367d4-108">Polecenie **cmdlet Get-AzAutomationDscNodeConfigurationDeployment** wdraża konfigurację węzła APS Desired State Configuration (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="367d4-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="367d4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="367d4-109">EXAMPLES</span></span>

### <span data-ttu-id="367d4-110">Przykład 1. Pobierz wszystkie harmonogramy wdrażania</span><span class="sxs-lookup"><span data-stu-id="367d4-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="367d4-111">Przykład 2. Uzyskiwanie harmonogramu wdrożenia</span><span class="sxs-lookup"><span data-stu-id="367d4-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="367d4-112">Powyższe polecenie wdraża konfigurację węzła DSC o nazwie "Config01.Node1" w podanej dwuwymiarowej tablicy nazw węzła.</span><span class="sxs-lookup"><span data-stu-id="367d4-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="367d4-113">Wdrożenie jest etapowe.</span><span class="sxs-lookup"><span data-stu-id="367d4-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="367d4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="367d4-114">PARAMETERS</span></span>

### <span data-ttu-id="367d4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="367d4-115">-AutomationAccountName</span></span>
<span data-ttu-id="367d4-116">Określa nazwę konta automatyzacji zawierającego konfigurację DSC kompilacyjną przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="367d4-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="367d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367d4-117">-DefaultProfile</span></span>
<span data-ttu-id="367d4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="367d4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="367d4-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="367d4-119">-JobScheduleId</span></span>
<span data-ttu-id="367d4-120">Określa identyfikator harmonogramu zadania dla istniejącego zaplanowanego zadania wdrażania.</span><span class="sxs-lookup"><span data-stu-id="367d4-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="367d4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="367d4-121">-ResourceGroupName</span></span>
<span data-ttu-id="367d4-122">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="367d4-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="367d4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367d4-123">CommonParameters</span></span>
<span data-ttu-id="367d4-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367d4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367d4-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367d4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367d4-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="367d4-126">INPUTS</span></span>

### <span data-ttu-id="367d4-127">System.Guid</span><span class="sxs-lookup"><span data-stu-id="367d4-127">System.Guid</span></span>

### <span data-ttu-id="367d4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="367d4-128">System.String</span></span>

## <span data-ttu-id="367d4-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="367d4-129">OUTPUTS</span></span>

### <span data-ttu-id="367d4-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="367d4-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="367d4-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="367d4-131">NOTES</span></span>

## <span data-ttu-id="367d4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="367d4-132">RELATED LINKS</span></span>

[<span data-ttu-id="367d4-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="367d4-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="367d4-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="367d4-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="367d4-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="367d4-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="367d4-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="367d4-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="367d4-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="367d4-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
