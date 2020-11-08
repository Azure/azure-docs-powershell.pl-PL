---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055323"
---
# <span data-ttu-id="78918-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="78918-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="78918-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78918-102">SYNOPSIS</span></span>

<span data-ttu-id="78918-103">Pobiera elementy Runbook usługi Azure Automation i skojarzone harmonogramy.</span><span class="sxs-lookup"><span data-stu-id="78918-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="78918-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78918-104">SYNTAX</span></span>

### <span data-ttu-id="78918-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="78918-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="78918-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="78918-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="78918-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="78918-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="78918-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="78918-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="78918-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="78918-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="78918-110">Opis</span><span class="sxs-lookup"><span data-stu-id="78918-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="78918-111">Funkcja **Get-AzureAutomationScheduledRunbook** pobiera jeden lub więcej elementów Runbook usługi Azure Automation oraz skojarzonych z nimi harmonogramów.</span><span class="sxs-lookup"><span data-stu-id="78918-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="78918-112">Domyślnie zostaną zwrócone wszystkie zaplanowane elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="78918-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="78918-113">Aby uzyskać określony zaplanowany element Runbook, określ nazwę elementu Runbook i nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="78918-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="78918-114">Aby uzyskać wszystkie harmonogramy skojarzone z elementem Runbook, określ tylko nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="78918-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="78918-115">Aby uzyskać wszystkie elementy Runbook skojarzone z harmonogramem, określ tylko nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="78918-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="78918-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78918-116">EXAMPLES</span></span>

### <span data-ttu-id="78918-117">Przykład 1: pobieranie wszystkich zaplanowanych elementów Runbook</span><span class="sxs-lookup"><span data-stu-id="78918-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="78918-118">To polecenie pobiera wszystkie zaplanowane elementy Runbook z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="78918-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="78918-119">Przykład 2: pobieranie wszystkich harmonogramów skojarzonych z elementem Runbook</span><span class="sxs-lookup"><span data-stu-id="78918-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="78918-120">To polecenie pobiera wszystkie zaplanowane elementy Runbook dla elementu Runbook Runbk01 na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="78918-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="78918-121">Przykład 3: pobieranie wszystkich elementów Runbook skojarzonych z harmonogramem</span><span class="sxs-lookup"><span data-stu-id="78918-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="78918-122">To polecenie pobiera wszystkie zaplanowane elementy Runbook dla Schedule01 harmonogram na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="78918-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="78918-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78918-123">PARAMETERS</span></span>

### <span data-ttu-id="78918-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78918-124">-AutomationAccountName</span></span>
<span data-ttu-id="78918-125">Określa nazwę konta usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="78918-125">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="78918-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="78918-126">-JobScheduleId</span></span>
<span data-ttu-id="78918-127">Określa identyfikator zaplanowanego zadania.</span><span class="sxs-lookup"><span data-stu-id="78918-127">Specifies the ID of a scheduled job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78918-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="78918-128">-Profile</span></span>
<span data-ttu-id="78918-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78918-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78918-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="78918-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78918-131">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="78918-131">-RunbookName</span></span>
<span data-ttu-id="78918-132">Określa nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="78918-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78918-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="78918-133">-ScheduleName</span></span>
<span data-ttu-id="78918-134">Określa nazwę harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="78918-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78918-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78918-135">CommonParameters</span></span>
<span data-ttu-id="78918-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78918-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78918-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78918-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78918-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78918-138">INPUTS</span></span>

## <span data-ttu-id="78918-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78918-139">OUTPUTS</span></span>

### <span data-ttu-id="78918-140">Microsoft. Azure. Commands. Automation. model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="78918-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="78918-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78918-141">NOTES</span></span>

## <span data-ttu-id="78918-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78918-142">RELATED LINKS</span></span>

[<span data-ttu-id="78918-143">Rejestr — AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="78918-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="78918-144">Wyrejestrowanie — AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="78918-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


