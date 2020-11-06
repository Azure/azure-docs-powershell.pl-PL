---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: ac63bbdb95551ff5ff08661a92f0924d5853ade5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549251"
---
# <span data-ttu-id="f191a-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="f191a-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="f191a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f191a-102">SYNOPSIS</span></span>
<span data-ttu-id="f191a-103">Zatrzymuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="f191a-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f191a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f191a-104">SYNTAX</span></span>

### <span data-ttu-id="f191a-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="f191a-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f191a-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f191a-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f191a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f191a-107">DESCRIPTION</span></span>
<span data-ttu-id="f191a-108">Polecenie cmdlet **stop-AzureBatchTask** zatrzymuje zadanie wsadowe usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="f191a-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="f191a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f191a-109">EXAMPLES</span></span>

### <span data-ttu-id="f191a-110">Przykład 1: usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="f191a-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="f191a-111">To polecenie zatrzymuje zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="f191a-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f191a-112">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f191a-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="f191a-113">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="f191a-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f191a-114">Przykład 2: zatrzymanie zadania wsadowego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="f191a-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="f191a-115">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task26 w zadaniu z identyfikatorem zadania ID-000001 przy użyciu polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="f191a-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="f191a-116">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="f191a-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f191a-117">Polecenie zatrzyma to zadanie.</span><span class="sxs-lookup"><span data-stu-id="f191a-117">The command stops that task.</span></span>

## <span data-ttu-id="f191a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f191a-118">PARAMETERS</span></span>

### <span data-ttu-id="f191a-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f191a-119">-BatchContext</span></span>
<span data-ttu-id="f191a-120">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f191a-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f191a-121">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f191a-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f191a-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f191a-122">-Id</span></span>
<span data-ttu-id="f191a-123">Określa identyfikator zadania, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f191a-123">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f191a-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="f191a-124">-JobId</span></span>
<span data-ttu-id="f191a-125">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="f191a-125">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f191a-126">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="f191a-126">-Task</span></span>
<span data-ttu-id="f191a-127">Określa zadanie, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f191a-127">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="f191a-128">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="f191a-128">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f191a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f191a-129">-DefaultProfile</span></span>
<span data-ttu-id="f191a-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f191a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f191a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f191a-131">CommonParameters</span></span>
<span data-ttu-id="f191a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f191a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f191a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f191a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f191a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f191a-134">INPUTS</span></span>

### <span data-ttu-id="f191a-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f191a-135">BatchAccountContext</span></span>
<span data-ttu-id="f191a-136">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="f191a-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="f191a-137">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="f191a-137">PSCloudTask</span></span>
<span data-ttu-id="f191a-138">Parametr "zadanie" akceptuje wartość typu "PSCloudTask" z potoku.</span><span class="sxs-lookup"><span data-stu-id="f191a-138">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="f191a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f191a-139">OUTPUTS</span></span>

## <span data-ttu-id="f191a-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f191a-140">NOTES</span></span>

## <span data-ttu-id="f191a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f191a-141">RELATED LINKS</span></span>

[<span data-ttu-id="f191a-142">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="f191a-142">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="f191a-143">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="f191a-143">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="f191a-144">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="f191a-144">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="f191a-145">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f191a-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


