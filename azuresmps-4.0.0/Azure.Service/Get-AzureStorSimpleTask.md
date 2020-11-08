---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054518"
---
# <span data-ttu-id="bfa5a-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="bfa5a-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="bfa5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfa5a-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa5a-103">Pobiera stan zadania na urządzeniu StorSimple.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="bfa5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfa5a-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bfa5a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bfa5a-105">DESCRIPTION</span></span>
<span data-ttu-id="bfa5a-106">Polecenie cmdlet **Get-AzureStorSimpleTask** Pobiera stan zadania, które jest uruchamiane asynchronicznie na urządzeniu usługi Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="bfa5a-107">Gdy zarządzasz urządzeniem StorSimple, większość akcji tworzenia, czytania, aktualizowania i usuwania może być wykonywany asynchronicznie.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="bfa5a-108">Program Windows PowerShell zwraca wartość **TaskID**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="bfa5a-109">Użyj identyfikatora, aby uzyskać bieżący stan zadania.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="bfa5a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfa5a-110">EXAMPLES</span></span>

### <span data-ttu-id="bfa5a-111">Przykład 1. Pobieranie stanu zadania</span><span class="sxs-lookup"><span data-stu-id="bfa5a-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="bfa5a-112">To polecenie uzyskuje stan zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="bfa5a-113">Wyniki wskazują, że zadanie ma stan ukończone i wynik pozytywny.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="bfa5a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfa5a-114">PARAMETERS</span></span>

### <span data-ttu-id="bfa5a-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="bfa5a-115">-InstanceId</span></span>
<span data-ttu-id="bfa5a-116">Określa identyfikator zadania, dla którego ten aplet polecenia śledzi stan.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa5a-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="bfa5a-117">-Profile</span></span>
<span data-ttu-id="bfa5a-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bfa5a-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bfa5a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa5a-120">CommonParameters</span></span>
<span data-ttu-id="bfa5a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa5a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfa5a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa5a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfa5a-123">INPUTS</span></span>

### <span data-ttu-id="bfa5a-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bfa5a-124">None</span></span>

## <span data-ttu-id="bfa5a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfa5a-125">OUTPUTS</span></span>

### <span data-ttu-id="bfa5a-126">JobStatusInfo</span><span class="sxs-lookup"><span data-stu-id="bfa5a-126">JobStatusInfo</span></span>
<span data-ttu-id="bfa5a-127">To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , który zawiera następujące pola:</span><span class="sxs-lookup"><span data-stu-id="bfa5a-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="bfa5a-128">**Błąd**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-128">**Error**.</span></span>
<span data-ttu-id="bfa5a-129">**ErrorDetails** , który zawiera **kod** i **wiadomość**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="bfa5a-130">**TaskID**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-130">**TaskId**.</span></span>
<span data-ttu-id="bfa5a-131">**String**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-131">**String**.</span></span>
<span data-ttu-id="bfa5a-132">Identyfikator zadania, dla którego jest zwracany stan.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="bfa5a-133">**TaskSteps**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-133">**TaskSteps**.</span></span>
<span data-ttu-id="bfa5a-134">**IList \<TaskStep\>**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="bfa5a-135">Każdy obiekt **TaskStep** zawiera **Informacje o szczegółach** , **kodzie błędu** , **komunikacie** , **wyniku** i **stanie**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="bfa5a-136">**Wynik**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-136">**Result**.</span></span>
<span data-ttu-id="bfa5a-137">**TaskResult** , który zawiera ogólny wynik zadania.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="bfa5a-138">Prawidłowe wartości to: niepowodzenie, udane, PartialSuccess, anulowane i nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="bfa5a-139">**Status**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-139">**Status**.</span></span>
<span data-ttu-id="bfa5a-140">**TaskStatus** , który zawiera całkowity stan uruchomienia zadania.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="bfa5a-141">Prawidłowe wartości to: w trakcie, nieprawidłowe i wykonane.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="bfa5a-142">**TaskResult**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-142">**TaskResult**.</span></span>
<span data-ttu-id="bfa5a-143">**TaskResult** wartość obliczona na podstawie **wyniku** i **stanu**.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="bfa5a-144">Prawidłowe wartości to: niepowodzenie, powiodło się, stan, PartialSuccess, anulowane i nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="bfa5a-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="bfa5a-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfa5a-145">NOTES</span></span>

## <span data-ttu-id="bfa5a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfa5a-146">RELATED LINKS</span></span>

