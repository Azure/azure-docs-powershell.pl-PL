---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: b572a7aefc3076671e78895f5fea531929858873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552411"
---
# <span data-ttu-id="1fc80-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="1fc80-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="1fc80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fc80-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc80-103">Aktualizuje właściwości zadania.</span><span class="sxs-lookup"><span data-stu-id="1fc80-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fc80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fc80-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fc80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1fc80-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc80-106">Polecenie cmdlet **Set-AzureBatchTask** aktualizuje właściwości zadania w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="1fc80-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="1fc80-107">Użyj polecenia cmdlet Get-AzureBatchTask, aby uzyskać obiekt **PSCloudTask** .</span><span class="sxs-lookup"><span data-stu-id="1fc80-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="1fc80-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet, aby zatwierdzić zmiany w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="1fc80-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="1fc80-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fc80-109">EXAMPLES</span></span>

### <span data-ttu-id="1fc80-110">Przykład 1: aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="1fc80-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="1fc80-111">Pierwsze polecenie pobiera zadanie przy użyciu polecenia **Get-AzureBatchTask** , a następnie zapisuje je w zmiennej $Task.</span><span class="sxs-lookup"><span data-stu-id="1fc80-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="1fc80-112">Następne dwa polecenia modyfikują ograniczenia zadania w $Task.</span><span class="sxs-lookup"><span data-stu-id="1fc80-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="1fc80-113">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $Task.</span><span class="sxs-lookup"><span data-stu-id="1fc80-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="1fc80-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fc80-114">PARAMETERS</span></span>

### <span data-ttu-id="1fc80-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1fc80-115">-BatchContext</span></span>
<span data-ttu-id="1fc80-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="1fc80-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1fc80-117">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="1fc80-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="1fc80-118">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="1fc80-118">-Task</span></span>
<span data-ttu-id="1fc80-119">Określa **PSCloudTask** , do którego to polecenie cmdlet aktualizuje usługę wsadową.</span><span class="sxs-lookup"><span data-stu-id="1fc80-119">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc80-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc80-120">-DefaultProfile</span></span>
<span data-ttu-id="1fc80-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fc80-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fc80-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc80-122">CommonParameters</span></span>
<span data-ttu-id="1fc80-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc80-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc80-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc80-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc80-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fc80-125">INPUTS</span></span>

### <span data-ttu-id="1fc80-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1fc80-126">BatchAccountContext</span></span>
<span data-ttu-id="1fc80-127">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="1fc80-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="1fc80-128">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="1fc80-128">PSCloudTask</span></span>
<span data-ttu-id="1fc80-129">Parametr "zadanie" akceptuje wartość typu "PSCloudTask" z potoku.</span><span class="sxs-lookup"><span data-stu-id="1fc80-129">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="1fc80-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fc80-130">OUTPUTS</span></span>

## <span data-ttu-id="1fc80-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fc80-131">NOTES</span></span>

## <span data-ttu-id="1fc80-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fc80-132">RELATED LINKS</span></span>

[<span data-ttu-id="1fc80-133">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="1fc80-133">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="1fc80-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1fc80-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="1fc80-135">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="1fc80-135">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="1fc80-136">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="1fc80-136">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="1fc80-137">Zatrzymaj — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="1fc80-137">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="1fc80-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="1fc80-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


