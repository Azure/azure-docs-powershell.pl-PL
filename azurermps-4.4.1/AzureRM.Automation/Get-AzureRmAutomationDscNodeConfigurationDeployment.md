---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 889318c911ae6f34b3655583ea2e9693da3bf80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547167"
---
# <span data-ttu-id="3f1d3-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3f1d3-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="3f1d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1d3-103">Umożliwia pobieranie wdrożeń konfiguracji węzłów DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f1d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f1d3-104">SYNTAX</span></span>

### <span data-ttu-id="3f1d3-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3f1d3-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [[-Status] <String>] [[-StartTime] <DateTimeOffset>]
 [[-EndTime] <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f1d3-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="3f1d3-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f1d3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3f1d3-107">DESCRIPTION</span></span>
<span data-ttu-id="3f1d3-108">Polecenie cmdlet **Get-AzureRmAutomationDscNodeConfigurationDeployment** umożliwia wdrożenie konfiguracji węzła APS (Konfiguracja stanu żądanego) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="3f1d3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f1d3-109">EXAMPLES</span></span>

### <span data-ttu-id="3f1d3-110">Przykład 1: pobieranie wdrożenia konfiguracji węzła</span><span class="sxs-lookup"><span data-stu-id="3f1d3-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="3f1d3-111">Powyższe polecenie wdraża konfigurację węzła DSC o nazwie "Config01. Node1" na podstawie dwuwymiarowej tablicy nazw węzłów.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="3f1d3-112">Wdrożenie przebiega w sposób stopniowy.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="3f1d3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f1d3-113">PARAMETERS</span></span>

### <span data-ttu-id="3f1d3-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="3f1d3-114">-JobId</span></span>
<span data-ttu-id="3f1d3-115">Określa identyfikator zadania istniejącego zadania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-115">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="3f1d3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1d3-116">-ResourceGroupName</span></span>
<span data-ttu-id="3f1d3-117">Określa nazwę grupy zasobów, w której to polecenie cmdlet kompiluje konfigurację.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-117">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="3f1d3-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3f1d3-118">-AutomationAccountName</span></span>
<span data-ttu-id="3f1d3-119">Określa nazwę konta automatyzacji zawierającego konfigurację DSC, którą jest kompilowany to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-119">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="3f1d3-120">-Status</span><span class="sxs-lookup"><span data-stu-id="3f1d3-120">-Status</span></span>
<span data-ttu-id="3f1d3-121">Stan filtru zadania.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-121">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1d3-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3f1d3-122">-StartTime</span></span>
<span data-ttu-id="3f1d3-123">Filtr czasu rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-123">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1d3-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3f1d3-124">-EndTime</span></span>
<span data-ttu-id="3f1d3-125">Filtr czasu zakończenia.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-125">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1d3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1d3-126">-DefaultProfile</span></span>
<span data-ttu-id="3f1d3-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f1d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1d3-128">CommonParameters</span></span>
<span data-ttu-id="3f1d3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f1d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1d3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f1d3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1d3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f1d3-131">INPUTS</span></span>

## <span data-ttu-id="3f1d3-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f1d3-132">OUTPUTS</span></span>

### <span data-ttu-id="3f1d3-133">Microsoft. Azure. Commands. Automation. model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3f1d3-133">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="3f1d3-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f1d3-134">NOTES</span></span>

## <span data-ttu-id="3f1d3-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f1d3-135">RELATED LINKS</span></span>

[<span data-ttu-id="3f1d3-136">Start — AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="3f1d3-136">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="3f1d3-137">Import — AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f1d3-137">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="3f1d3-138">Start — AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3f1d3-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="3f1d3-139">Zatrzymaj — AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="3f1d3-139">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="3f1d3-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="3f1d3-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
