---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 18a96a72cc965f5e93a035ba6ed7b91ba5419edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549420"
---
# <span data-ttu-id="72f26-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="72f26-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="72f26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72f26-102">SYNOPSIS</span></span>
<span data-ttu-id="72f26-103">Zatrzymuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="72f26-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72f26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72f26-104">SYNTAX</span></span>

### <span data-ttu-id="72f26-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="72f26-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72f26-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="72f26-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72f26-107">Opis</span><span class="sxs-lookup"><span data-stu-id="72f26-107">DESCRIPTION</span></span>
<span data-ttu-id="72f26-108">Polecenie cmdlet **stop-AzureBatchTask** zatrzymuje zadanie wsadowe usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="72f26-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="72f26-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72f26-109">EXAMPLES</span></span>

### <span data-ttu-id="72f26-110">Przykład 1: usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="72f26-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="72f26-111">To polecenie zatrzymuje zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="72f26-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="72f26-112">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72f26-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="72f26-113">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="72f26-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="72f26-114">Przykład 2: zatrzymanie zadania wsadowego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="72f26-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="72f26-115">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task26 w zadaniu z identyfikatorem zadania ID-000001 przy użyciu polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="72f26-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="72f26-116">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="72f26-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="72f26-117">Polecenie zatrzyma to zadanie.</span><span class="sxs-lookup"><span data-stu-id="72f26-117">The command stops that task.</span></span>

## <span data-ttu-id="72f26-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72f26-118">PARAMETERS</span></span>

### <span data-ttu-id="72f26-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="72f26-119">-BatchContext</span></span>
<span data-ttu-id="72f26-120">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="72f26-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="72f26-121">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="72f26-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="72f26-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="72f26-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="72f26-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="72f26-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="72f26-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="72f26-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="72f26-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f26-125">-DefaultProfile</span></span>
<span data-ttu-id="72f26-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72f26-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72f26-127">-ID</span><span class="sxs-lookup"><span data-stu-id="72f26-127">-Id</span></span>
<span data-ttu-id="72f26-128">Określa identyfikator zadania, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72f26-128">Specifies the ID of the task that this cmdlet stops.</span></span>

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

### <span data-ttu-id="72f26-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="72f26-129">-JobId</span></span>
<span data-ttu-id="72f26-130">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="72f26-130">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="72f26-131">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="72f26-131">-Task</span></span>
<span data-ttu-id="72f26-132">Określa zadanie, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72f26-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="72f26-133">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="72f26-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="72f26-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f26-134">CommonParameters</span></span>
<span data-ttu-id="72f26-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f26-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f26-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f26-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f26-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72f26-137">INPUTS</span></span>

### <span data-ttu-id="72f26-138">System. String</span><span class="sxs-lookup"><span data-stu-id="72f26-138">System.String</span></span>

### <span data-ttu-id="72f26-139">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="72f26-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="72f26-140">Parametry: zadanie (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72f26-140">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="72f26-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="72f26-141">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="72f26-142">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72f26-142">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="72f26-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72f26-143">OUTPUTS</span></span>

### <span data-ttu-id="72f26-144">System. void</span><span class="sxs-lookup"><span data-stu-id="72f26-144">System.Void</span></span>

## <span data-ttu-id="72f26-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72f26-145">NOTES</span></span>

## <span data-ttu-id="72f26-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72f26-146">RELATED LINKS</span></span>

[<span data-ttu-id="72f26-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="72f26-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="72f26-148">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="72f26-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="72f26-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="72f26-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="72f26-150">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="72f26-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


