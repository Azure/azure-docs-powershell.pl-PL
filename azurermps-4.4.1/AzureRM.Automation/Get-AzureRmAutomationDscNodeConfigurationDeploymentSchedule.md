---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: 993de4da39f27a54be97de9fb7befe065fdd70f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547159"
---
# <span data-ttu-id="9b6f7-101">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="9b6f7-101">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="9b6f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b6f7-102">SYNOPSIS</span></span>
<span data-ttu-id="9b6f7-103">Pobiera harmonogram zadań wdrożenia konfiguracji węzła DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9b6f7-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b6f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b6f7-104">SYNTAX</span></span>

### <span data-ttu-id="9b6f7-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9b6f7-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b6f7-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="9b6f7-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b6f7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9b6f7-107">DESCRIPTION</span></span>
<span data-ttu-id="9b6f7-108">Polecenie cmdlet **Get-AzureRmAutomationDscNodeConfigurationDeployment** umożliwia wdrożenie konfiguracji węzła APS (Konfiguracja stanu żądanego) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9b6f7-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="9b6f7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b6f7-109">EXAMPLES</span></span>

### <span data-ttu-id="9b6f7-110">Przykład 1. Pobierz wszystkie harmonogramy wdrażania</span><span class="sxs-lookup"><span data-stu-id="9b6f7-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule `
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

### <span data-ttu-id="9b6f7-111">Przykład 2: pobieranie harmonogramu wdrażania</span><span class="sxs-lookup"><span data-stu-id="9b6f7-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule `
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

<span data-ttu-id="9b6f7-112">Powyższe polecenie wdraża konfigurację węzła DSC o nazwie "Config01. Node1" na podstawie dwuwymiarowej tablicy nazw węzłów.</span><span class="sxs-lookup"><span data-stu-id="9b6f7-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="9b6f7-113">Wdrożenie przebiega w sposób stopniowy.</span><span class="sxs-lookup"><span data-stu-id="9b6f7-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="9b6f7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b6f7-114">PARAMETERS</span></span>

### <span data-ttu-id="9b6f7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b6f7-115">-ResourceGroupName</span></span>
<span data-ttu-id="9b6f7-116">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="9b6f7-116">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="9b6f7-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9b6f7-117">-AutomationAccountName</span></span>
<span data-ttu-id="9b6f7-118">Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą jest kompilowany to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b6f7-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="9b6f7-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="9b6f7-119">-JobScheduleId</span></span>
<span data-ttu-id="9b6f7-120">Określa identyfikator harmonogramu zadań istniejącego zaplanowanego zadania wdrażania.</span><span class="sxs-lookup"><span data-stu-id="9b6f7-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

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

### <span data-ttu-id="9b6f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6f7-121">-DefaultProfile</span></span>
<span data-ttu-id="9b6f7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b6f7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b6f7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b6f7-123">CommonParameters</span></span>
<span data-ttu-id="9b6f7-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b6f7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b6f7-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b6f7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b6f7-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b6f7-126">INPUTS</span></span>

## <span data-ttu-id="9b6f7-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b6f7-127">OUTPUTS</span></span>

### <span data-ttu-id="9b6f7-128">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="9b6f7-128">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="9b6f7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b6f7-129">NOTES</span></span>

## <span data-ttu-id="9b6f7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b6f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="9b6f7-131">Start — AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9b6f7-131">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="9b6f7-132">Import — AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b6f7-132">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="9b6f7-133">Start — AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9b6f7-133">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="9b6f7-134">Zatrzymaj — AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9b6f7-134">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="9b6f7-135">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9b6f7-135">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)
