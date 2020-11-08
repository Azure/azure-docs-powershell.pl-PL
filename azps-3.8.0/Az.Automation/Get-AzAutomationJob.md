---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051645"
---
# <span data-ttu-id="be849-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="be849-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="be849-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be849-102">SYNOPSIS</span></span>
<span data-ttu-id="be849-103">Pobiera zadania elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="be849-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="be849-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be849-104">SYNTAX</span></span>

### <span data-ttu-id="be849-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be849-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be849-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="be849-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be849-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="be849-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be849-108">Opis</span><span class="sxs-lookup"><span data-stu-id="be849-108">DESCRIPTION</span></span>
<span data-ttu-id="be849-109">Polecenie cmdlet **Get-AzAutomationJob** pobiera zadania elementu Runbook w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="be849-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="be849-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be849-110">EXAMPLES</span></span>

### <span data-ttu-id="be849-111">Przykład 1: uzyskiwanie określonego zadania w usłudze Runbook</span><span class="sxs-lookup"><span data-stu-id="be849-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="be849-112">To polecenie uzyskuje zadanie o określonym identyfikatorze GUID.</span><span class="sxs-lookup"><span data-stu-id="be849-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="be849-113">Przykład 2: pobieranie wszystkich zadań elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="be849-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="be849-114">To polecenie pobiera wszystkie zadania skojarzone z elementem Runbook o nazwie Runbook02.</span><span class="sxs-lookup"><span data-stu-id="be849-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="be849-115">Przykład 3: uzyskiwanie wszystkich uruchomionych zadań</span><span class="sxs-lookup"><span data-stu-id="be849-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="be849-116">To polecenie pobiera wszystkie uruchomione zadania na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="be849-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="be849-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be849-117">PARAMETERS</span></span>

### <span data-ttu-id="be849-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="be849-118">-AutomationAccountName</span></span>
<span data-ttu-id="be849-119">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="be849-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="be849-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be849-120">-DefaultProfile</span></span>
<span data-ttu-id="be849-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="be849-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be849-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="be849-122">-EndTime</span></span>
<span data-ttu-id="be849-123">Określa godzinę zakończenia zadania jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="be849-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="be849-124">Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="be849-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="be849-125">To polecenie cmdlet umożliwia pobieranie zadań, których wartość w tym parametrze określa godzina zakończenia lub przed nią.</span><span class="sxs-lookup"><span data-stu-id="be849-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be849-126">-ID</span><span class="sxs-lookup"><span data-stu-id="be849-126">-Id</span></span>
<span data-ttu-id="be849-127">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be849-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="be849-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be849-128">-ResourceGroupName</span></span>
<span data-ttu-id="be849-129">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="be849-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="be849-130">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="be849-130">-RunbookName</span></span>
<span data-ttu-id="be849-131">Określa nazwę elementu Runbook, dla którego to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="be849-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be849-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="be849-132">-StartTime</span></span>
<span data-ttu-id="be849-133">Określa godzinę rozpoczęcia zadania jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="be849-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="be849-134">To polecenie cmdlet umożliwia pobieranie zadań o wartości od godziny rozpoczęcia przypadającej w tym parametrze lub po niej.</span><span class="sxs-lookup"><span data-stu-id="be849-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be849-135">-Status</span><span class="sxs-lookup"><span data-stu-id="be849-135">-Status</span></span>
<span data-ttu-id="be849-136">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="be849-136">Specifies the status of a job.</span></span>
<span data-ttu-id="be849-137">To polecenie cmdlet umożliwia pobieranie zadań o stanie zgodnych z tym parametrem.</span><span class="sxs-lookup"><span data-stu-id="be849-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="be849-138">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="be849-138">Valid values are:</span></span> 
- <span data-ttu-id="be849-139">Ponownego</span><span class="sxs-lookup"><span data-stu-id="be849-139">Activating</span></span>
- <span data-ttu-id="be849-140">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="be849-140">Completed</span></span>
- <span data-ttu-id="be849-141">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="be849-141">Failed</span></span>
- <span data-ttu-id="be849-142">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="be849-142">Queued</span></span>
- <span data-ttu-id="be849-143">Działanie</span><span class="sxs-lookup"><span data-stu-id="be849-143">Resuming</span></span>
- <span data-ttu-id="be849-144">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="be849-144">Running</span></span>
- <span data-ttu-id="be849-145">Czynając</span><span class="sxs-lookup"><span data-stu-id="be849-145">Starting</span></span>
- <span data-ttu-id="be849-146">Trzymywanie</span><span class="sxs-lookup"><span data-stu-id="be849-146">Stopped</span></span>
- <span data-ttu-id="be849-147">Trzymywany</span><span class="sxs-lookup"><span data-stu-id="be849-147">Stopping</span></span>
- <span data-ttu-id="be849-148">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="be849-148">Suspended</span></span>
- <span data-ttu-id="be849-149">Zawieszeniem</span><span class="sxs-lookup"><span data-stu-id="be849-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be849-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be849-150">CommonParameters</span></span>
<span data-ttu-id="be849-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be849-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be849-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be849-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be849-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be849-153">INPUTS</span></span>

### <span data-ttu-id="be849-154">System. GUID</span><span class="sxs-lookup"><span data-stu-id="be849-154">System.Guid</span></span>

### <span data-ttu-id="be849-155">System. String</span><span class="sxs-lookup"><span data-stu-id="be849-155">System.String</span></span>

## <span data-ttu-id="be849-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be849-156">OUTPUTS</span></span>

### <span data-ttu-id="be849-157">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="be849-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="be849-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be849-158">NOTES</span></span>

## <span data-ttu-id="be849-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be849-159">RELATED LINKS</span></span>

[<span data-ttu-id="be849-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="be849-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="be849-161">Życiorys — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="be849-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="be849-162">Zatrzymaj — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="be849-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="be849-163">Suspend — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="be849-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


