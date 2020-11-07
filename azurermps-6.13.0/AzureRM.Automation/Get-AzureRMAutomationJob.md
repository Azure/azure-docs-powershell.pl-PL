---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 6e825e6d582117a919691aea4780868191e8e4a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718388"
---
# <span data-ttu-id="b2b15-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b2b15-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="b2b15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2b15-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b15-103">Pobiera zadania elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b2b15-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2b15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2b15-104">SYNTAX</span></span>

### <span data-ttu-id="b2b15-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2b15-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2b15-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="b2b15-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2b15-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="b2b15-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2b15-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b2b15-108">DESCRIPTION</span></span>
<span data-ttu-id="b2b15-109">Polecenie cmdlet **Get-AzureRmAutomationJob** pobiera zadania elementu Runbook w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b2b15-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="b2b15-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2b15-110">EXAMPLES</span></span>

### <span data-ttu-id="b2b15-111">Przykład 1: uzyskiwanie określonego zadania w usłudze Runbook</span><span class="sxs-lookup"><span data-stu-id="b2b15-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="b2b15-112">To polecenie uzyskuje zadanie o określonym identyfikatorze GUID.</span><span class="sxs-lookup"><span data-stu-id="b2b15-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="b2b15-113">Przykład 2: pobieranie wszystkich zadań elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="b2b15-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="b2b15-114">To polecenie pobiera wszystkie zadania skojarzone z elementem Runbook o nazwie Runbook02.</span><span class="sxs-lookup"><span data-stu-id="b2b15-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="b2b15-115">Przykład 3: uzyskiwanie wszystkich uruchomionych zadań</span><span class="sxs-lookup"><span data-stu-id="b2b15-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="b2b15-116">To polecenie pobiera wszystkie uruchomione zadania na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b2b15-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b2b15-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2b15-117">PARAMETERS</span></span>

### <span data-ttu-id="b2b15-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2b15-118">-AutomationAccountName</span></span>
<span data-ttu-id="b2b15-119">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="b2b15-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="b2b15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b15-120">-DefaultProfile</span></span>
<span data-ttu-id="b2b15-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b2b15-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2b15-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b2b15-122">-EndTime</span></span>
<span data-ttu-id="b2b15-123">Określa godzinę zakończenia zadania jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="b2b15-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b2b15-124">Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="b2b15-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="b2b15-125">To polecenie cmdlet umożliwia pobieranie zadań, których wartość w tym parametrze określa godzina zakończenia lub przed nią.</span><span class="sxs-lookup"><span data-stu-id="b2b15-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2b15-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b2b15-126">-Id</span></span>
<span data-ttu-id="b2b15-127">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2b15-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b2b15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b15-128">-ResourceGroupName</span></span>
<span data-ttu-id="b2b15-129">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="b2b15-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="b2b15-130">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="b2b15-130">-RunbookName</span></span>
<span data-ttu-id="b2b15-131">Określa nazwę elementu Runbook, dla którego to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="b2b15-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="b2b15-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b2b15-132">-StartTime</span></span>
<span data-ttu-id="b2b15-133">Określa godzinę rozpoczęcia zadania jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="b2b15-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b2b15-134">To polecenie cmdlet umożliwia pobieranie zadań o wartości od godziny rozpoczęcia przypadającej w tym parametrze lub po niej.</span><span class="sxs-lookup"><span data-stu-id="b2b15-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2b15-135">-Status</span><span class="sxs-lookup"><span data-stu-id="b2b15-135">-Status</span></span>
<span data-ttu-id="b2b15-136">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="b2b15-136">Specifies the status of a job.</span></span>
<span data-ttu-id="b2b15-137">To polecenie cmdlet umożliwia pobieranie zadań o stanie zgodnych z tym parametrem.</span><span class="sxs-lookup"><span data-stu-id="b2b15-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="b2b15-138">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b2b15-138">Valid values are:</span></span> 
- <span data-ttu-id="b2b15-139">Ponownego</span><span class="sxs-lookup"><span data-stu-id="b2b15-139">Activating</span></span>
- <span data-ttu-id="b2b15-140">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="b2b15-140">Completed</span></span>
- <span data-ttu-id="b2b15-141">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="b2b15-141">Failed</span></span>
- <span data-ttu-id="b2b15-142">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="b2b15-142">Queued</span></span>
- <span data-ttu-id="b2b15-143">Działanie</span><span class="sxs-lookup"><span data-stu-id="b2b15-143">Resuming</span></span>
- <span data-ttu-id="b2b15-144">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="b2b15-144">Running</span></span>
- <span data-ttu-id="b2b15-145">Czynając</span><span class="sxs-lookup"><span data-stu-id="b2b15-145">Starting</span></span>
- <span data-ttu-id="b2b15-146">Trzymywanie</span><span class="sxs-lookup"><span data-stu-id="b2b15-146">Stopped</span></span>
- <span data-ttu-id="b2b15-147">Trzymywany</span><span class="sxs-lookup"><span data-stu-id="b2b15-147">Stopping</span></span>
- <span data-ttu-id="b2b15-148">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="b2b15-148">Suspended</span></span>
- <span data-ttu-id="b2b15-149">Zawieszeniem</span><span class="sxs-lookup"><span data-stu-id="b2b15-149">Suspending</span></span>

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

### <span data-ttu-id="b2b15-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b15-150">CommonParameters</span></span>
<span data-ttu-id="b2b15-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b15-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b15-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2b15-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b15-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2b15-153">INPUTS</span></span>

### <span data-ttu-id="b2b15-154">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b2b15-154">System.Guid</span></span>

### <span data-ttu-id="b2b15-155">System. String</span><span class="sxs-lookup"><span data-stu-id="b2b15-155">System.String</span></span>

## <span data-ttu-id="b2b15-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2b15-156">OUTPUTS</span></span>

### <span data-ttu-id="b2b15-157">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="b2b15-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="b2b15-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2b15-158">NOTES</span></span>

## <span data-ttu-id="b2b15-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2b15-159">RELATED LINKS</span></span>

[<span data-ttu-id="b2b15-160">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b2b15-160">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="b2b15-161">Życiorys — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b2b15-161">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="b2b15-162">Zatrzymaj — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b2b15-162">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="b2b15-163">Suspend — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b2b15-163">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


