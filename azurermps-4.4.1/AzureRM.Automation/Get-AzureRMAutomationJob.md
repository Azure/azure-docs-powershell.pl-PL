---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 4509190a8417379c9d5bc9eae9d6d12609def4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554235"
---
# <span data-ttu-id="6de44-101">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6de44-101">Get-AzureRmAutomationJob</span></span>

## <span data-ttu-id="6de44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6de44-102">SYNOPSIS</span></span>
<span data-ttu-id="6de44-103">Pobiera zadania elementu Runbook automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="6de44-103">Gets Automation runbook jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6de44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6de44-104">SYNTAX</span></span>

### <span data-ttu-id="6de44-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6de44-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6de44-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="6de44-106">ByJobId</span></span>
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6de44-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="6de44-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6de44-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6de44-108">DESCRIPTION</span></span>
<span data-ttu-id="6de44-109">Polecenie cmdlet **Get-AzureRmAutomationJob** pobiera zadania elementu Runbook w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6de44-109">The **Get-AzureRmAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="6de44-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6de44-110">EXAMPLES</span></span>

### <span data-ttu-id="6de44-111">Przykład 1: uzyskiwanie określonego zadania w usłudze Runbook</span><span class="sxs-lookup"><span data-stu-id="6de44-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="6de44-112">To polecenie uzyskuje zadanie o określonym identyfikatorze GUID.</span><span class="sxs-lookup"><span data-stu-id="6de44-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="6de44-113">Przykład 2: pobieranie wszystkich zadań elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="6de44-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="6de44-114">To polecenie pobiera wszystkie zadania skojarzone z elementem Runbook o nazwie Runbook02.</span><span class="sxs-lookup"><span data-stu-id="6de44-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="6de44-115">Przykład 3: uzyskiwanie wszystkich uruchomionych zadań</span><span class="sxs-lookup"><span data-stu-id="6de44-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="6de44-116">To polecenie pobiera wszystkie uruchomione zadania na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6de44-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6de44-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6de44-117">PARAMETERS</span></span>

### <span data-ttu-id="6de44-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6de44-118">-AutomationAccountName</span></span>
<span data-ttu-id="6de44-119">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="6de44-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="6de44-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6de44-120">-EndTime</span></span>
<span data-ttu-id="6de44-121">Określa godzinę zakończenia zadania jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="6de44-121">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="6de44-122">Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="6de44-122">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="6de44-123">To polecenie cmdlet umożliwia pobieranie zadań, których wartość w tym parametrze określa godzina zakończenia lub przed nią.</span><span class="sxs-lookup"><span data-stu-id="6de44-123">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="6de44-124">-ID</span><span class="sxs-lookup"><span data-stu-id="6de44-124">-Id</span></span>
<span data-ttu-id="6de44-125">Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6de44-125">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6de44-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de44-126">-ResourceGroupName</span></span>
<span data-ttu-id="6de44-127">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="6de44-127">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="6de44-128">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="6de44-128">-RunbookName</span></span>
<span data-ttu-id="6de44-129">Określa nazwę elementu Runbook, dla którego to polecenie cmdlet pobiera zadania.</span><span class="sxs-lookup"><span data-stu-id="6de44-129">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="6de44-130">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6de44-130">-StartTime</span></span>
<span data-ttu-id="6de44-131">Określa godzinę rozpoczęcia zadania jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="6de44-131">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="6de44-132">To polecenie cmdlet umożliwia pobieranie zadań o wartości od godziny rozpoczęcia przypadającej w tym parametrze lub po niej.</span><span class="sxs-lookup"><span data-stu-id="6de44-132">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="6de44-133">-Status</span><span class="sxs-lookup"><span data-stu-id="6de44-133">-Status</span></span>
<span data-ttu-id="6de44-134">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="6de44-134">Specifies the status of a job.</span></span>
<span data-ttu-id="6de44-135">To polecenie cmdlet umożliwia pobieranie zadań o stanie zgodnych z tym parametrem.</span><span class="sxs-lookup"><span data-stu-id="6de44-135">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="6de44-136">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="6de44-136">Valid values are:</span></span> 

- <span data-ttu-id="6de44-137">Ponownego</span><span class="sxs-lookup"><span data-stu-id="6de44-137">Activating</span></span>
- <span data-ttu-id="6de44-138">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="6de44-138">Completed</span></span>
- <span data-ttu-id="6de44-139">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="6de44-139">Failed</span></span>
- <span data-ttu-id="6de44-140">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="6de44-140">Queued</span></span>
- <span data-ttu-id="6de44-141">Działanie</span><span class="sxs-lookup"><span data-stu-id="6de44-141">Resuming</span></span>
- <span data-ttu-id="6de44-142">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="6de44-142">Running</span></span>
- <span data-ttu-id="6de44-143">Czynając</span><span class="sxs-lookup"><span data-stu-id="6de44-143">Starting</span></span>
- <span data-ttu-id="6de44-144">Trzymywanie</span><span class="sxs-lookup"><span data-stu-id="6de44-144">Stopped</span></span>
- <span data-ttu-id="6de44-145">Trzymywany</span><span class="sxs-lookup"><span data-stu-id="6de44-145">Stopping</span></span>
- <span data-ttu-id="6de44-146">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="6de44-146">Suspended</span></span>
- <span data-ttu-id="6de44-147">Zawieszeniem</span><span class="sxs-lookup"><span data-stu-id="6de44-147">Suspending</span></span>

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

### <span data-ttu-id="6de44-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de44-148">-DefaultProfile</span></span>
<span data-ttu-id="6de44-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6de44-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de44-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de44-150">CommonParameters</span></span>
<span data-ttu-id="6de44-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de44-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de44-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de44-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de44-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6de44-153">INPUTS</span></span>

## <span data-ttu-id="6de44-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6de44-154">OUTPUTS</span></span>

### <span data-ttu-id="6de44-155">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="6de44-155">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="6de44-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6de44-156">NOTES</span></span>

## <span data-ttu-id="6de44-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6de44-157">RELATED LINKS</span></span>

[<span data-ttu-id="6de44-158">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="6de44-158">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="6de44-159">Życiorys — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6de44-159">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="6de44-160">Zatrzymaj — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6de44-160">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="6de44-161">Suspend — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6de44-161">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


