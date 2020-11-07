---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 463f19b5ed459f0c2b2f4a4fdeff40bf69db2682
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706662"
---
# <span data-ttu-id="2003d-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="2003d-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="2003d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2003d-102">SYNOPSIS</span></span>
<span data-ttu-id="2003d-103">Pobiera informacje podzadania określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="2003d-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="2003d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2003d-104">SYNTAX</span></span>

### <span data-ttu-id="2003d-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2003d-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2003d-106">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="2003d-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2003d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2003d-107">DESCRIPTION</span></span>
<span data-ttu-id="2003d-108">Polecenie cmdlet **Get-AzBatchSubtask** pobiera informacje podzadania określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="2003d-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="2003d-109">Podzadania zapewniają równoległą obróbkę poszczególnych zadań i umożliwiają precyzyjne monitorowanie wykonywania i postępu zadań.</span><span class="sxs-lookup"><span data-stu-id="2003d-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="2003d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2003d-110">EXAMPLES</span></span>

### <span data-ttu-id="2003d-111">Przykład 1. zwraca wszystkie podzadania dla określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="2003d-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="2003d-112">Te polecenia zwracają wszystkie podzadania zadania z IDENTYFIKATORem moje zadanie.</span><span class="sxs-lookup"><span data-stu-id="2003d-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="2003d-113">W tym celu pierwszym poleceniem w przykładzie jest tworzenie odwołania do obiektu dla kluczy konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="2003d-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="2003d-114">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="2003d-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="2003d-115">Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **Get-AzBatchSubtask** , aby zwrócić wszystkie podzadania zadania podzadania, zadanie uruchamiane w ramach zadania zlecenia-01.</span><span class="sxs-lookup"><span data-stu-id="2003d-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="2003d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2003d-116">PARAMETERS</span></span>

### <span data-ttu-id="2003d-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2003d-117">-BatchContext</span></span>
<span data-ttu-id="2003d-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="2003d-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2003d-119">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="2003d-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2003d-120">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="2003d-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2003d-121">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="2003d-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2003d-122">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2003d-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2003d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2003d-123">-DefaultProfile</span></span>
<span data-ttu-id="2003d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2003d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2003d-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="2003d-125">-JobId</span></span>
<span data-ttu-id="2003d-126">Określa identyfikator zadania zawierającego zadanie, którego podzadania są dostępne.</span><span class="sxs-lookup"><span data-stu-id="2003d-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2003d-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2003d-127">-MaxCount</span></span>
<span data-ttu-id="2003d-128">Określa maksymalną liczbę podzadań, które należy zwrócić.</span><span class="sxs-lookup"><span data-stu-id="2003d-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="2003d-129">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="2003d-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="2003d-130">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="2003d-130">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2003d-131">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="2003d-131">-Task</span></span>
<span data-ttu-id="2003d-132">Określa odwołanie do obiektu zadania, które zawiera podzadania zwrócone przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2003d-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="2003d-133">Odwołanie do obiektu jest tworzone przy użyciu polecenia cmdlet Get-AzBatchTask i przechowywania zwróconego obiektu w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="2003d-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2003d-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="2003d-134">-TaskId</span></span>
<span data-ttu-id="2003d-135">Określa identyfikator zadania, którego podzadania są zwracane przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="2003d-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2003d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2003d-136">CommonParameters</span></span>
<span data-ttu-id="2003d-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2003d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2003d-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2003d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2003d-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2003d-139">INPUTS</span></span>

### <span data-ttu-id="2003d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2003d-140">System.String</span></span>

### <span data-ttu-id="2003d-141">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="2003d-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="2003d-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2003d-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2003d-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2003d-143">OUTPUTS</span></span>

### <span data-ttu-id="2003d-144">Microsoft.Azure.Commands.Batch. Modele. PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="2003d-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="2003d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2003d-145">NOTES</span></span>

## <span data-ttu-id="2003d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2003d-146">RELATED LINKS</span></span>

[<span data-ttu-id="2003d-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="2003d-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

