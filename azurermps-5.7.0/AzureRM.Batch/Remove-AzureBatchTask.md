---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 775425b0da46ef6c2b22e1c28725b323b3071974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552228"
---
# <span data-ttu-id="6e9c5-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e9c5-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="6e9c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e9c5-103">Umożliwia usunięcie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e9c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e9c5-104">SYNTAX</span></span>

### <span data-ttu-id="6e9c5-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="6e9c5-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e9c5-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e9c5-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e9c5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6e9c5-107">DESCRIPTION</span></span>
<span data-ttu-id="6e9c5-108">Polecenie cmdlet **Remove-AzureBatchTask** usuwa zadanie wsadowe usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="6e9c5-109">To polecenie cmdlet monituje o potwierdzenie, chyba że parametr *Force* zostanie określony.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="6e9c5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e9c5-110">EXAMPLES</span></span>

### <span data-ttu-id="6e9c5-111">Przykład 1: usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="6e9c5-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="6e9c5-112">To polecenie usuwa zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="6e9c5-113">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="6e9c5-114">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6e9c5-115">Przykład 2: usuwanie zadania wsadowego przy użyciu rurociągu bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="6e9c5-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="6e9c5-116">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task26 w zadaniu z identyfikatorem zadania ID-000001 przy użyciu polecenia cmdlet **Get-AzureBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="6e9c5-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="6e9c5-117">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6e9c5-118">Polecenie usunie to zadanie.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-118">The command deletes that task.</span></span>
<span data-ttu-id="6e9c5-119">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="6e9c5-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6e9c5-120">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6e9c5-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e9c5-121">PARAMETERS</span></span>

### <span data-ttu-id="6e9c5-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6e9c5-122">-BatchContext</span></span>
<span data-ttu-id="6e9c5-123">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6e9c5-124">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6e9c5-125">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6e9c5-126">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6e9c5-127">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e9c5-128">-DefaultProfile</span></span>
<span data-ttu-id="6e9c5-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c5-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6e9c5-130">-Force</span></span>
<span data-ttu-id="6e9c5-131">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c5-132">-ID</span><span class="sxs-lookup"><span data-stu-id="6e9c5-132">-Id</span></span>
<span data-ttu-id="6e9c5-133">Określa identyfikator zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="6e9c5-134">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c5-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e9c5-135">-InputObject</span></span>
<span data-ttu-id="6e9c5-136">Określa zadanie, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="6e9c5-137">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c5-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="6e9c5-138">-JobId</span></span>
<span data-ttu-id="6e9c5-139">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-139">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c5-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e9c5-140">-Confirm</span></span>
<span data-ttu-id="6e9c5-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e9c5-142">-WhatIf</span></span>
<span data-ttu-id="6e9c5-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e9c5-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e9c5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e9c5-145">CommonParameters</span></span>
<span data-ttu-id="6e9c5-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e9c5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e9c5-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e9c5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e9c5-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e9c5-148">INPUTS</span></span>

### <span data-ttu-id="6e9c5-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6e9c5-149">BatchAccountContext</span></span>
<span data-ttu-id="6e9c5-150">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6e9c5-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6e9c5-151">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="6e9c5-151">PSCloudTask</span></span>
<span data-ttu-id="6e9c5-152">Parametr "Inputobject" przyjmuje wartość typu "PSCloudTask" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6e9c5-152">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="6e9c5-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e9c5-153">OUTPUTS</span></span>

## <span data-ttu-id="6e9c5-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e9c5-154">NOTES</span></span>

## <span data-ttu-id="6e9c5-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e9c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="6e9c5-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6e9c5-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6e9c5-157">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e9c5-157">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="6e9c5-158">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e9c5-158">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="6e9c5-159">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e9c5-159">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="6e9c5-160">Zatrzymaj — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e9c5-160">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="6e9c5-161">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="6e9c5-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


