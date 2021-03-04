---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 622b25a4cd84fcdd6ffb8179b3990ac786733e06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990480"
---
# <span data-ttu-id="c8850-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="c8850-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="c8850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8850-102">SYNOPSIS</span></span>
<span data-ttu-id="c8850-103">Pobiera informacje o podzadaniu określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="c8850-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="c8850-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c8850-104">SYNTAX</span></span>

### <span data-ttu-id="c8850-105">FiltrDanych OData (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c8850-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8850-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="c8850-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8850-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c8850-107">DESCRIPTION</span></span>
<span data-ttu-id="c8850-108">Polecenie **cmdlet Get-AzBatchSubtask** pobiera informacje podzadania dotyczące określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="c8850-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="c8850-109">Podzadawki zapewniają przetwarzanie równoległe poszczególnych zadań i umożliwiają precyzyjne monitorowanie wykonywania zadań i postępu.</span><span class="sxs-lookup"><span data-stu-id="c8850-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="c8850-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c8850-110">EXAMPLES</span></span>

### <span data-ttu-id="c8850-111">Przykład 1. Zwracanie wszystkich podzadań dla określonego zadania</span><span class="sxs-lookup"><span data-stu-id="c8850-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="c8850-112">Te polecenia zwracają wszystkie podzadaty dla zadania o identyfikatorze myTask.</span><span class="sxs-lookup"><span data-stu-id="c8850-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="c8850-113">W tym celu pierwsze polecenie w tym przykładzie tworzy odwołanie obiektu do kluczy konta dla konta wsadowego contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="c8850-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="c8850-114">To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $context.</span><span class="sxs-lookup"><span data-stu-id="c8850-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="c8850-115">Drugie polecenie używa następnie tego odwołania do obiektu i polecenia cmdlet **Get-AzBatchSubtask** w celu zwrócenia wszystkich podzadań dla zadania myTask— zadania uruchamianego w ramach zadania Zadania-01.</span><span class="sxs-lookup"><span data-stu-id="c8850-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="c8850-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8850-116">PARAMETERS</span></span>

### <span data-ttu-id="c8850-117">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="c8850-117">-BatchContext</span></span>
<span data-ttu-id="c8850-118">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="c8850-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c8850-119">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c8850-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c8850-120">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="c8850-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c8850-121">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="c8850-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c8850-122">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c8850-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c8850-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8850-123">-DefaultProfile</span></span>
<span data-ttu-id="c8850-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8850-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8850-125">- JobId</span><span class="sxs-lookup"><span data-stu-id="c8850-125">-JobId</span></span>
<span data-ttu-id="c8850-126">Określa identyfikator zadania zawierającego zadanie, którego podzadania pobiera to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8850-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="c8850-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c8850-127">-MaxCount</span></span>
<span data-ttu-id="c8850-128">Określa maksymalną liczbę zwracanych podzadań.</span><span class="sxs-lookup"><span data-stu-id="c8850-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="c8850-129">Jeśli określisz wartość zero (0) lub mniejszą, polecenie cmdlet nie użyje górnego limitu.</span><span class="sxs-lookup"><span data-stu-id="c8850-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="c8850-130">Wartość domyślna to 1000.</span><span class="sxs-lookup"><span data-stu-id="c8850-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="c8850-131">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="c8850-131">-Task</span></span>
<span data-ttu-id="c8850-132">Określa odwołanie do obiektu do zadania zawierającego podzadanie zwracane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8850-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="c8850-133">To odwołanie do obiektu jest tworzone przy użyciu Get-AzBatchTask cmdlet i przechowywania zwróconego obiektu w zmiennej.</span><span class="sxs-lookup"><span data-stu-id="c8850-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="c8850-134">- TaskId</span><span class="sxs-lookup"><span data-stu-id="c8850-134">-TaskId</span></span>
<span data-ttu-id="c8850-135">Określa identyfikator zadania, którego podzadanie zwraca to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8850-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="c8850-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8850-136">CommonParameters</span></span>
<span data-ttu-id="c8850-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8850-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8850-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8850-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8850-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8850-139">INPUTS</span></span>

### <span data-ttu-id="c8850-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c8850-140">System.String</span></span>

### <span data-ttu-id="c8850-141">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="c8850-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="c8850-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c8850-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c8850-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8850-143">OUTPUTS</span></span>

### <span data-ttu-id="c8850-144">Microsoft.Azure.Commands.Batch. Models.PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="c8850-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="c8850-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c8850-145">NOTES</span></span>

## <span data-ttu-id="c8850-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8850-146">RELATED LINKS</span></span>

[<span data-ttu-id="c8850-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c8850-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


