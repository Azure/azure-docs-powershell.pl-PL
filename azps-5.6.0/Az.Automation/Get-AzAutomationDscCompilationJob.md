---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5157b4d4e1a291193f10fef22308002de210e748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993049"
---
# <span data-ttu-id="f653f-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f653f-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="f653f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f653f-102">SYNOPSIS</span></span>
<span data-ttu-id="f653f-103">Otrzymuje zadania kompilacji dsc w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f653f-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="f653f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f653f-104">SYNTAX</span></span>

### <span data-ttu-id="f653f-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f653f-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f653f-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="f653f-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f653f-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f653f-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f653f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f653f-108">DESCRIPTION</span></span>
<span data-ttu-id="f653f-109">Polecenie **cmdlet Get-AzAutomationDscCompilationJob** pobiera zadania kompilacji APS Desired State Configuration (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f653f-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="f653f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f653f-110">EXAMPLES</span></span>

### <span data-ttu-id="f653f-111">Przykład 1. Uzyskiwanie wszystkich zadań kompilacji dsc</span><span class="sxs-lookup"><span data-stu-id="f653f-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f653f-112">To polecenie pobiera wszystkie zadania kompilacji na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f653f-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f653f-113">Przykład 2. Uzyskiwanie zadań kompilacji dsc dla konfiguracji</span><span class="sxs-lookup"><span data-stu-id="f653f-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="f653f-114">To polecenie pobiera wszystkie zadania kompilacji dla konfiguracji DSC o nazwie ContosoConfiguration w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f653f-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f653f-115">Przykład 3. Uzyskiwanie określonego zadania kompilacji dsc</span><span class="sxs-lookup"><span data-stu-id="f653f-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="f653f-116">To polecenie pobiera zadanie kompilacji z określonym identyfikatorem na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f653f-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f653f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f653f-117">PARAMETERS</span></span>

### <span data-ttu-id="f653f-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f653f-118">-AutomationAccountName</span></span>
<span data-ttu-id="f653f-119">Określa nazwę konta automatyzacji zawierającego zadania kompilacji dsc, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f653f-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f653f-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f653f-120">-ConfigurationName</span></span>
<span data-ttu-id="f653f-121">Określa nazwę konfiguracji dsc, dla której to polecenie cmdlet otrzymuje zadania kompilacji.</span><span class="sxs-lookup"><span data-stu-id="f653f-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f653f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f653f-122">-DefaultProfile</span></span>
<span data-ttu-id="f653f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f653f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f653f-124">- EndTime</span><span class="sxs-lookup"><span data-stu-id="f653f-124">-EndTime</span></span>
<span data-ttu-id="f653f-125">Określa czas zakończenia.</span><span class="sxs-lookup"><span data-stu-id="f653f-125">Specifies an end time.</span></span>
<span data-ttu-id="f653f-126">To polecenie cmdlet pobiera zadania kompilacji, które rozpoczęły się do czasu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f653f-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f653f-127">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="f653f-127">-Id</span></span>
<span data-ttu-id="f653f-128">Określa unikatowy identyfikator zadania kompilacji dsc, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f653f-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f653f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f653f-129">-ResourceGroupName</span></span>
<span data-ttu-id="f653f-130">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera zadania kompilacji DSC.</span><span class="sxs-lookup"><span data-stu-id="f653f-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="f653f-131">— StartTime</span><span class="sxs-lookup"><span data-stu-id="f653f-131">-StartTime</span></span>
<span data-ttu-id="f653f-132">Określa czas rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="f653f-132">Specifies a start time.</span></span>
<span data-ttu-id="f653f-133">To polecenie cmdlet pobiera zadania, które rozpoczynają się od lub po upływie czasu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f653f-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f653f-134">— Status</span><span class="sxs-lookup"><span data-stu-id="f653f-134">-Status</span></span>
<span data-ttu-id="f653f-135">Określa stan zadań, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f653f-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f653f-136">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="f653f-136">Valid values are:</span></span> 
- <span data-ttu-id="f653f-137">Ukończono</span><span class="sxs-lookup"><span data-stu-id="f653f-137">Completed</span></span> 
- <span data-ttu-id="f653f-138">Niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="f653f-138">Failed</span></span> 
- <span data-ttu-id="f653f-139">W kolejce</span><span class="sxs-lookup"><span data-stu-id="f653f-139">Queued</span></span> 
- <span data-ttu-id="f653f-140">Rozpoczynanie</span><span class="sxs-lookup"><span data-stu-id="f653f-140">Starting</span></span> 
- <span data-ttu-id="f653f-141">Wznawianie</span><span class="sxs-lookup"><span data-stu-id="f653f-141">Resuming</span></span> 
- <span data-ttu-id="f653f-142">Uruchomione</span><span class="sxs-lookup"><span data-stu-id="f653f-142">Running</span></span> 
- <span data-ttu-id="f653f-143">Zatrzymano</span><span class="sxs-lookup"><span data-stu-id="f653f-143">Stopped</span></span> 
- <span data-ttu-id="f653f-144">Zatrzymywanie</span><span class="sxs-lookup"><span data-stu-id="f653f-144">Stopping</span></span> 
- <span data-ttu-id="f653f-145">Wstrzymane</span><span class="sxs-lookup"><span data-stu-id="f653f-145">Suspended</span></span> 
- <span data-ttu-id="f653f-146">Zawieszanie</span><span class="sxs-lookup"><span data-stu-id="f653f-146">Suspending</span></span> 
- <span data-ttu-id="f653f-147">Aktywacja</span><span class="sxs-lookup"><span data-stu-id="f653f-147">Activating</span></span>
- <span data-ttu-id="f653f-148">Nowy</span><span class="sxs-lookup"><span data-stu-id="f653f-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f653f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f653f-149">CommonParameters</span></span>
<span data-ttu-id="f653f-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f653f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f653f-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f653f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f653f-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f653f-152">INPUTS</span></span>

### <span data-ttu-id="f653f-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f653f-153">System.Guid</span></span>

### <span data-ttu-id="f653f-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f653f-154">System.String</span></span>

## <span data-ttu-id="f653f-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f653f-155">OUTPUTS</span></span>

### <span data-ttu-id="f653f-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="f653f-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="f653f-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f653f-157">NOTES</span></span>

## <span data-ttu-id="f653f-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f653f-158">RELATED LINKS</span></span>

[<span data-ttu-id="f653f-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="f653f-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="f653f-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f653f-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


