---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055335"
---
# <span data-ttu-id="33f4e-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="33f4e-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="33f4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33f4e-102">SYNOPSIS</span></span>

<span data-ttu-id="33f4e-103">Pobiera co najmniej jedno zadanie elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="33f4e-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="33f4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33f4e-104">SYNTAX</span></span>

### <span data-ttu-id="33f4e-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33f4e-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="33f4e-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="33f4e-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="33f4e-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="33f4e-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="33f4e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="33f4e-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="33f4e-109">Polecenie cmdlet **Get-AzureAutomationJob** pobiera co najmniej jedno zadanie Runbook w usłudze Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="33f4e-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="33f4e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33f4e-110">EXAMPLES</span></span>

### <span data-ttu-id="33f4e-111">Przykład 1: uzyskiwanie określonego zadania w usłudze Runbook</span><span class="sxs-lookup"><span data-stu-id="33f4e-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="33f4e-112">To polecenie uzyskuje zadanie o określonym identyfikatorze GUID.</span><span class="sxs-lookup"><span data-stu-id="33f4e-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="33f4e-113">Przykład 2: pobieranie wszystkich zadań elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="33f4e-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="33f4e-114">To polecenie pobiera wszystkie zadania skojarzone z elementem Runbook o nazwie webrunbook.</span><span class="sxs-lookup"><span data-stu-id="33f4e-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="33f4e-115">Przykład 2: uzyskiwanie wszystkich uruchomionych zadań</span><span class="sxs-lookup"><span data-stu-id="33f4e-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="33f4e-116">To polecenie pobiera wszystkie uruchomione zadania na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="33f4e-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="33f4e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33f4e-117">PARAMETERS</span></span>

### <span data-ttu-id="33f4e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="33f4e-118">-AutomationAccountName</span></span>
<span data-ttu-id="33f4e-119">Określa nazwę konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="33f4e-119">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33f4e-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="33f4e-120">-EndTime</span></span>
<span data-ttu-id="33f4e-121">Określa godzinę zakończenia zadania.</span><span class="sxs-lookup"><span data-stu-id="33f4e-121">Specifies the end time for a job.</span></span>

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

### <span data-ttu-id="33f4e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="33f4e-122">-Id</span></span>
<span data-ttu-id="33f4e-123">Określa identyfikator zadania.</span><span class="sxs-lookup"><span data-stu-id="33f4e-123">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="33f4e-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="33f4e-124">-Profile</span></span>
<span data-ttu-id="33f4e-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33f4e-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33f4e-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="33f4e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f4e-127">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="33f4e-127">-RunbookName</span></span>
<span data-ttu-id="33f4e-128">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="33f4e-128">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="33f4e-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="33f4e-129">-StartTime</span></span>
<span data-ttu-id="33f4e-130">Określa godzinę rozpoczęcia zadania.</span><span class="sxs-lookup"><span data-stu-id="33f4e-130">Specifies the start time of a job.</span></span>

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

### <span data-ttu-id="33f4e-131">-Status</span><span class="sxs-lookup"><span data-stu-id="33f4e-131">-Status</span></span>
<span data-ttu-id="33f4e-132">Określa stan zadania.</span><span class="sxs-lookup"><span data-stu-id="33f4e-132">Specifies the status of a job.</span></span>
<span data-ttu-id="33f4e-133">To polecenie cmdlet umożliwia pobieranie zadań o stanie zgodnych z tym parametrem.</span><span class="sxs-lookup"><span data-stu-id="33f4e-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="33f4e-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="33f4e-134">Valid values are:</span></span> 

- <span data-ttu-id="33f4e-135">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="33f4e-135">Completed</span></span>
- <span data-ttu-id="33f4e-136">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="33f4e-136">Failed</span></span>
- <span data-ttu-id="33f4e-137">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="33f4e-137">Queued</span></span>
- <span data-ttu-id="33f4e-138">Czynając</span><span class="sxs-lookup"><span data-stu-id="33f4e-138">Starting</span></span>
- <span data-ttu-id="33f4e-139">Działanie</span><span class="sxs-lookup"><span data-stu-id="33f4e-139">Resuming</span></span>
- <span data-ttu-id="33f4e-140">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="33f4e-140">Running</span></span>
- <span data-ttu-id="33f4e-141">Trzymywanie</span><span class="sxs-lookup"><span data-stu-id="33f4e-141">Stopped</span></span>
- <span data-ttu-id="33f4e-142">Trzymywany</span><span class="sxs-lookup"><span data-stu-id="33f4e-142">Stopping</span></span>
- <span data-ttu-id="33f4e-143">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="33f4e-143">Suspended</span></span>
- <span data-ttu-id="33f4e-144">Zawieszeniem</span><span class="sxs-lookup"><span data-stu-id="33f4e-144">Suspending</span></span>
- <span data-ttu-id="33f4e-145">Ponownego</span><span class="sxs-lookup"><span data-stu-id="33f4e-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f4e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f4e-146">CommonParameters</span></span>
<span data-ttu-id="33f4e-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f4e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f4e-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33f4e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f4e-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33f4e-149">INPUTS</span></span>

## <span data-ttu-id="33f4e-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33f4e-150">OUTPUTS</span></span>

### <span data-ttu-id="33f4e-151">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="33f4e-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="33f4e-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33f4e-152">NOTES</span></span>

## <span data-ttu-id="33f4e-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33f4e-153">RELATED LINKS</span></span>

[<span data-ttu-id="33f4e-154">Życiorys — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="33f4e-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="33f4e-155">Zatrzymaj — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="33f4e-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="33f4e-156">Suspend — AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="33f4e-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


