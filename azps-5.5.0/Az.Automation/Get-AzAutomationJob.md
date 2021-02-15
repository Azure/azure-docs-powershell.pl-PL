---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244290"
---
# <span data-ttu-id="cb46c-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="cb46c-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="cb46c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb46c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb46c-103">Otrzymuje zadania podręcznika automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="cb46c-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="cb46c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cb46c-104">SYNTAX</span></span>

### <span data-ttu-id="cb46c-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="cb46c-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb46c-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="cb46c-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb46c-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="cb46c-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb46c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cb46c-108">DESCRIPTION</span></span>
<span data-ttu-id="cb46c-109">Polecenie **cmdlet Get-AzAutomationJob** otrzymuje zadania podręcznika w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cb46c-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="cb46c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cb46c-110">EXAMPLES</span></span>

### <span data-ttu-id="cb46c-111">Przykład 1. Uzyskiwanie określonego zadania podręcznika</span><span class="sxs-lookup"><span data-stu-id="cb46c-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="cb46c-112">To polecenie otrzymuje zadanie o określonym identyfikatorze GUID.</span><span class="sxs-lookup"><span data-stu-id="cb46c-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="cb46c-113">Przykład 2. Uzyskiwanie wszystkich zadań dla podręcznika uruchamiania</span><span class="sxs-lookup"><span data-stu-id="cb46c-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="cb46c-114">To polecenie pobiera wszystkie zadania skojarzone z podręcznikiem runbook o nazwie Runbook02.</span><span class="sxs-lookup"><span data-stu-id="cb46c-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="cb46c-115">Przykład 3. Uzyskiwanie wszystkich uruchomionych zadań</span><span class="sxs-lookup"><span data-stu-id="cb46c-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="cb46c-116">To polecenie pobiera wszystkie uruchomione zadania na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cb46c-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cb46c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb46c-117">PARAMETERS</span></span>

### <span data-ttu-id="cb46c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cb46c-118">-AutomationAccountName</span></span>
<span data-ttu-id="cb46c-119">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet otrzymuje zadania.</span><span class="sxs-lookup"><span data-stu-id="cb46c-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="cb46c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb46c-120">-DefaultProfile</span></span>
<span data-ttu-id="cb46c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cb46c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb46c-122">- EndTime</span><span class="sxs-lookup"><span data-stu-id="cb46c-122">-EndTime</span></span>
<span data-ttu-id="cb46c-123">Określa czas zakończenia zadania jako obiekt **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="cb46c-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="cb46c-124">Możesz określić ciąg, który może zostać przekonwertowany na prawidłowy **dateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="cb46c-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="cb46c-125">To polecenie cmdlet pobiera zadania, które mają czas zakończenia na lub przed wartością, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cb46c-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb46c-126">— Id</span><span class="sxs-lookup"><span data-stu-id="cb46c-126">-Id</span></span>
<span data-ttu-id="cb46c-127">Określa identyfikator zadania, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb46c-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cb46c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb46c-128">-ResourceGroupName</span></span>
<span data-ttu-id="cb46c-129">Określa nazwę grupy zasobów, w której to polecenie cmdlet otrzymuje zadania.</span><span class="sxs-lookup"><span data-stu-id="cb46c-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="cb46c-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="cb46c-130">-RunbookName</span></span>
<span data-ttu-id="cb46c-131">Określa nazwę podręcznika, dla którego to polecenie cmdlet otrzymuje zadania.</span><span class="sxs-lookup"><span data-stu-id="cb46c-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="cb46c-132">— StartTime</span><span class="sxs-lookup"><span data-stu-id="cb46c-132">-StartTime</span></span>
<span data-ttu-id="cb46c-133">Określa czas rozpoczęcia zadania jako obiekt **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="cb46c-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="cb46c-134">To polecenie cmdlet pobiera zadania, których godzina rozpoczęcia jest określana jako wartość określana przez ten parametr lub po tej wartości.</span><span class="sxs-lookup"><span data-stu-id="cb46c-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb46c-135">— Status</span><span class="sxs-lookup"><span data-stu-id="cb46c-135">-Status</span></span>
<span data-ttu-id="cb46c-136">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="cb46c-136">Specifies the status of a job.</span></span>
<span data-ttu-id="cb46c-137">To polecenie cmdlet pobiera zadania, które mają stan zgodny z tym parametrem.</span><span class="sxs-lookup"><span data-stu-id="cb46c-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="cb46c-138">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="cb46c-138">Valid values are:</span></span> 
- <span data-ttu-id="cb46c-139">Aktywacja</span><span class="sxs-lookup"><span data-stu-id="cb46c-139">Activating</span></span>
- <span data-ttu-id="cb46c-140">Ukończono</span><span class="sxs-lookup"><span data-stu-id="cb46c-140">Completed</span></span>
- <span data-ttu-id="cb46c-141">Niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="cb46c-141">Failed</span></span>
- <span data-ttu-id="cb46c-142">W kolejce</span><span class="sxs-lookup"><span data-stu-id="cb46c-142">Queued</span></span>
- <span data-ttu-id="cb46c-143">Wznawianie</span><span class="sxs-lookup"><span data-stu-id="cb46c-143">Resuming</span></span>
- <span data-ttu-id="cb46c-144">Uruchomione</span><span class="sxs-lookup"><span data-stu-id="cb46c-144">Running</span></span>
- <span data-ttu-id="cb46c-145">Rozpoczynanie</span><span class="sxs-lookup"><span data-stu-id="cb46c-145">Starting</span></span>
- <span data-ttu-id="cb46c-146">Zatrzymano</span><span class="sxs-lookup"><span data-stu-id="cb46c-146">Stopped</span></span>
- <span data-ttu-id="cb46c-147">Zatrzymywanie</span><span class="sxs-lookup"><span data-stu-id="cb46c-147">Stopping</span></span>
- <span data-ttu-id="cb46c-148">Wstrzymane</span><span class="sxs-lookup"><span data-stu-id="cb46c-148">Suspended</span></span>
- <span data-ttu-id="cb46c-149">Zawieszanie</span><span class="sxs-lookup"><span data-stu-id="cb46c-149">Suspending</span></span>

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

### <span data-ttu-id="cb46c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb46c-150">CommonParameters</span></span>
<span data-ttu-id="cb46c-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb46c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb46c-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb46c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb46c-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb46c-153">INPUTS</span></span>

### <span data-ttu-id="cb46c-154">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cb46c-154">System.Guid</span></span>

### <span data-ttu-id="cb46c-155">System.String</span><span class="sxs-lookup"><span data-stu-id="cb46c-155">System.String</span></span>

## <span data-ttu-id="cb46c-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb46c-156">OUTPUTS</span></span>

### <span data-ttu-id="cb46c-157">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="cb46c-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="cb46c-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cb46c-158">NOTES</span></span>

## <span data-ttu-id="cb46c-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb46c-159">RELATED LINKS</span></span>

[<span data-ttu-id="cb46c-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="cb46c-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="cb46c-161">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="cb46c-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="cb46c-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="cb46c-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="cb46c-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="cb46c-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


