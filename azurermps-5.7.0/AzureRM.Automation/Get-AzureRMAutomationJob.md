---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 3183720cbafc9a8feae5c9687dfb92ab325f8b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525378"
---
# <span data-ttu-id="b5346-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b5346-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="b5346-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5346-102">SYNOPSIS</span></span>
<span data-ttu-id="b5346-103">Pobiera zadania elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b5346-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5346-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5346-104">SYNTAX</span></span>

### <span data-ttu-id="b5346-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5346-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5346-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="b5346-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5346-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="b5346-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5346-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b5346-108">DESCRIPTION</span></span>
<span data-ttu-id="b5346-109">Polecenie cmdlet **Get-AzureRmAutomationJob** pobiera zadania elementu Runbook w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b5346-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="b5346-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5346-110">EXAMPLES</span></span>

### <span data-ttu-id="b5346-111">Przykład 1: uzyskiwanie określonego zadania w usłudze Runbook</span><span class="sxs-lookup"><span data-stu-id="b5346-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="b5346-112">To polecenie uzyskuje zadanie o określonym identyfikatorze GUID.</span><span class="sxs-lookup"><span data-stu-id="b5346-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="b5346-113">Przykład 2: pobieranie wszystkich zadań elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="b5346-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="b5346-114">To polecenie pobiera wszystkie zadania skojarzone z elementem Runbook o nazwie Runbook02.</span><span class="sxs-lookup"><span data-stu-id="b5346-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="b5346-115">Przykład 3: uzyskiwanie wszystkich uruchomionych zadań</span><span class="sxs-lookup"><span data-stu-id="b5346-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="b5346-116">To polecenie pobiera wszystkie uruchomione zadania na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b5346-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b5346-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5346-117">PARAMETERS</span></span>

### <span data-ttu-id="b5346-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b5346-118">-AutomationAccountName</span></span>
<span data-ttu-id="b5346-119">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="b5346-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5346-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5346-120">-DefaultProfile</span></span>
<span data-ttu-id="b5346-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b5346-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5346-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b5346-122">-EndTime</span></span>
<span data-ttu-id="b5346-123">Określa godzinę zakończenia zadania jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="b5346-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b5346-124">Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="b5346-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="b5346-125">To polecenie cmdlet umożliwia pobieranie zadań, których wartość w tym parametrze określa godzina zakończenia lub przed nią.</span><span class="sxs-lookup"><span data-stu-id="b5346-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5346-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b5346-126">-Id</span></span>
<span data-ttu-id="b5346-127">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5346-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5346-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5346-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5346-129">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="b5346-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5346-130">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="b5346-130">-RunbookName</span></span>
<span data-ttu-id="b5346-131">Określa nazwę elementu Runbook, dla którego to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="b5346-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5346-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b5346-132">-StartTime</span></span>
<span data-ttu-id="b5346-133">Określa godzinę rozpoczęcia zadania jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="b5346-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b5346-134">To polecenie cmdlet umożliwia pobieranie zadań o wartości od godziny rozpoczęcia przypadającej w tym parametrze lub po niej.</span><span class="sxs-lookup"><span data-stu-id="b5346-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5346-135">-Status</span><span class="sxs-lookup"><span data-stu-id="b5346-135">-Status</span></span>
<span data-ttu-id="b5346-136">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="b5346-136">Specifies the status of a job.</span></span>
<span data-ttu-id="b5346-137">To polecenie cmdlet umożliwia pobieranie zadań o stanie zgodnych z tym parametrem.</span><span class="sxs-lookup"><span data-stu-id="b5346-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="b5346-138">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b5346-138">Valid values are:</span></span> 

- <span data-ttu-id="b5346-139">Ponownego</span><span class="sxs-lookup"><span data-stu-id="b5346-139">Activating</span></span>
- <span data-ttu-id="b5346-140">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="b5346-140">Completed</span></span>
- <span data-ttu-id="b5346-141">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="b5346-141">Failed</span></span>
- <span data-ttu-id="b5346-142">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="b5346-142">Queued</span></span>
- <span data-ttu-id="b5346-143">Działanie</span><span class="sxs-lookup"><span data-stu-id="b5346-143">Resuming</span></span>
- <span data-ttu-id="b5346-144">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="b5346-144">Running</span></span>
- <span data-ttu-id="b5346-145">Czynając</span><span class="sxs-lookup"><span data-stu-id="b5346-145">Starting</span></span>
- <span data-ttu-id="b5346-146">Trzymywanie</span><span class="sxs-lookup"><span data-stu-id="b5346-146">Stopped</span></span>
- <span data-ttu-id="b5346-147">Trzymywany</span><span class="sxs-lookup"><span data-stu-id="b5346-147">Stopping</span></span>
- <span data-ttu-id="b5346-148">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="b5346-148">Suspended</span></span>
- <span data-ttu-id="b5346-149">Zawieszeniem</span><span class="sxs-lookup"><span data-stu-id="b5346-149">Suspending</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5346-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5346-150">CommonParameters</span></span>
<span data-ttu-id="b5346-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5346-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5346-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5346-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5346-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5346-153">INPUTS</span></span>

### <span data-ttu-id="b5346-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b5346-154">None</span></span>
<span data-ttu-id="b5346-155">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b5346-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5346-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5346-156">OUTPUTS</span></span>

### <span data-ttu-id="b5346-157">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="b5346-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="b5346-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5346-158">NOTES</span></span>

## <span data-ttu-id="b5346-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5346-159">RELATED LINKS</span></span>

[<span data-ttu-id="b5346-160">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b5346-160">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="b5346-161">Życiorys — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b5346-161">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="b5346-162">Zatrzymaj — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b5346-162">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="b5346-163">Suspend — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b5346-163">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


