---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 449d539b767883bb075bcf333695b3285e047a9c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502379"
---
# <span data-ttu-id="5d5bb-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5d5bb-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="5d5bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5bb-103">Umożliwia pobieranie wdrożeń konfiguracji węzłów DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="5d5bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d5bb-104">SYNTAX</span></span>

### <span data-ttu-id="5d5bb-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d5bb-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d5bb-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="5d5bb-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d5bb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5d5bb-107">DESCRIPTION</span></span>
<span data-ttu-id="5d5bb-108">Polecenie cmdlet **Get-AzAutomationDscNodeConfigurationDeployment** powoduje wdrożenie konfiguracji węzła APS (Konfiguracja stanu żądanego) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="5d5bb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d5bb-109">EXAMPLES</span></span>

### <span data-ttu-id="5d5bb-110">Przykład 1: pobieranie wdrożenia konfiguracji węzła</span><span class="sxs-lookup"><span data-stu-id="5d5bb-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="5d5bb-111">Powyższe polecenie wdraża konfigurację węzła DSC o nazwie "Config01. Node1" na podstawie dwuwymiarowej tablicy nazw węzłów.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="5d5bb-112">Wdrożenie przebiega w sposób stopniowy.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="5d5bb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d5bb-113">PARAMETERS</span></span>

### <span data-ttu-id="5d5bb-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5d5bb-114">-AutomationAccountName</span></span>
<span data-ttu-id="5d5bb-115">Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą jest kompilowany to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="5d5bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5bb-116">-DefaultProfile</span></span>
<span data-ttu-id="5d5bb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5d5bb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d5bb-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5d5bb-118">-EndTime</span></span>
<span data-ttu-id="5d5bb-119">Filtr czasu zakończenia.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-119">End time filter.</span></span>

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

### <span data-ttu-id="5d5bb-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="5d5bb-120">-JobId</span></span>
<span data-ttu-id="5d5bb-121">Określa identyfikator zadania istniejącego zadania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="5d5bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="5d5bb-123">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="5d5bb-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5d5bb-124">-StartTime</span></span>
<span data-ttu-id="5d5bb-125">Filtr czasu rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-125">Start time filter.</span></span>

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

### <span data-ttu-id="5d5bb-126">-Status</span><span class="sxs-lookup"><span data-stu-id="5d5bb-126">-Status</span></span>
<span data-ttu-id="5d5bb-127">Stan filtru zadania.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="5d5bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5bb-128">CommonParameters</span></span>
<span data-ttu-id="5d5bb-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5bb-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d5bb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5bb-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d5bb-131">INPUTS</span></span>

### <span data-ttu-id="5d5bb-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5d5bb-132">System.Guid</span></span>

### <span data-ttu-id="5d5bb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5d5bb-133">System.String</span></span>

## <span data-ttu-id="5d5bb-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d5bb-134">OUTPUTS</span></span>

### <span data-ttu-id="5d5bb-135">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5d5bb-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="5d5bb-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d5bb-136">NOTES</span></span>

## <span data-ttu-id="5d5bb-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d5bb-137">RELATED LINKS</span></span>

[<span data-ttu-id="5d5bb-138">Start — AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5d5bb-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="5d5bb-139">Import — AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d5bb-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="5d5bb-140">Start — AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5d5bb-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5d5bb-141">Zatrzymaj — AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5d5bb-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5d5bb-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="5d5bb-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
