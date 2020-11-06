---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 58bed6fda4040c1af48469f4aa85f717c26c898c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554219"
---
# <span data-ttu-id="da233-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="da233-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="da233-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da233-102">SYNOPSIS</span></span>
<span data-ttu-id="da233-103">Pobiera informacje podzadania określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="da233-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da233-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da233-104">SYNTAX</span></span>

### <span data-ttu-id="da233-105">ODataFilter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="da233-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da233-106">Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="da233-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da233-107">Opis</span><span class="sxs-lookup"><span data-stu-id="da233-107">DESCRIPTION</span></span>
<span data-ttu-id="da233-108">Polecenie cmdlet **Get-AzureBatchSubtask** pobiera informacje podzadania określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="da233-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="da233-109">Podzadania zapewniają równoległą obróbkę poszczególnych zadań i umożliwiają precyzyjne monitorowanie wykonywania i postępu zadań.</span><span class="sxs-lookup"><span data-stu-id="da233-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="da233-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da233-110">EXAMPLES</span></span>

### <span data-ttu-id="da233-111">Przykład 1. zwraca wszystkie podzadania dla określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="da233-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="da233-112">Te polecenia zwracają wszystkie podzadania zadania z IDENTYFIKATORem moje zadanie.</span><span class="sxs-lookup"><span data-stu-id="da233-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="da233-113">W tym celu pierwszym poleceniem w przykładzie jest tworzenie odwołania do obiektu dla kluczy konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="da233-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="da233-114">Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="da233-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="da233-115">Drugie polecenie korzysta z tego odwołania do obiektu i polecenia cmdlet **Get-AzureBatchSubtask** , aby zwrócić wszystkie podzadania zadania podzadania, zadanie uruchamiane w ramach zadania zlecenia-01.</span><span class="sxs-lookup"><span data-stu-id="da233-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="da233-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da233-116">PARAMETERS</span></span>

### <span data-ttu-id="da233-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="da233-117">-BatchContext</span></span>
<span data-ttu-id="da233-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="da233-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="da233-119">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="da233-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="da233-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="da233-120">-JobId</span></span>
<span data-ttu-id="da233-121">Określa identyfikator zadania zawierającego zadanie, którego podzadania są dostępne.</span><span class="sxs-lookup"><span data-stu-id="da233-121">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="da233-122">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="da233-122">-MaxCount</span></span>
<span data-ttu-id="da233-123">Określa maksymalną liczbę podzadań, które należy zwrócić.</span><span class="sxs-lookup"><span data-stu-id="da233-123">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="da233-124">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie używa górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="da233-124">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="da233-125">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="da233-125">The default value is 1000.</span></span>

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

### <span data-ttu-id="da233-126">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="da233-126">-Task</span></span>
<span data-ttu-id="da233-127">Określa odwołanie do obiektu zadania, które zawiera podzadania zwrócone przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da233-127">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="da233-128">Odwołanie do obiektu jest tworzone przy użyciu polecenia cmdlet Get-AzureBatchTask i przechowywania zwróconego obiektu w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="da233-128">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="da233-129">-TaskId</span><span class="sxs-lookup"><span data-stu-id="da233-129">-TaskId</span></span>
<span data-ttu-id="da233-130">Określa identyfikator zadania, którego podzadania są zwracane przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="da233-130">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="da233-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da233-131">-DefaultProfile</span></span>
<span data-ttu-id="da233-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da233-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da233-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da233-133">CommonParameters</span></span>
<span data-ttu-id="da233-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da233-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da233-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da233-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da233-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da233-136">INPUTS</span></span>

### <span data-ttu-id="da233-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="da233-137">BatchAccountContext</span></span>
<span data-ttu-id="da233-138">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="da233-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="da233-139">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="da233-139">PSCloudTask</span></span>
<span data-ttu-id="da233-140">Parametr "zadanie" akceptuje wartość typu "PSCloudTask" z potoku.</span><span class="sxs-lookup"><span data-stu-id="da233-140">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="da233-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da233-141">OUTPUTS</span></span>

###  
<span data-ttu-id="da233-142">To polecenie cmdlet zwraca wystąpienia obiektu **PSSubtaskInformation** .</span><span class="sxs-lookup"><span data-stu-id="da233-142">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="da233-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da233-143">NOTES</span></span>

## <span data-ttu-id="da233-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da233-144">RELATED LINKS</span></span>

[<span data-ttu-id="da233-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="da233-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


