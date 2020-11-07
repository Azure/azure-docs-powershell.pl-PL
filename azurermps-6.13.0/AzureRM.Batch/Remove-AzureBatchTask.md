---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 3012abfca2ca257ad7b72fb974a8c062bfe196d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716594"
---
# <span data-ttu-id="7bfa9-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7bfa9-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="7bfa9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7bfa9-102">SYNOPSIS</span></span>
<span data-ttu-id="7bfa9-103">Umożliwia usunięcie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bfa9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7bfa9-104">SYNTAX</span></span>

### <span data-ttu-id="7bfa9-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="7bfa9-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bfa9-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="7bfa9-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bfa9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7bfa9-107">DESCRIPTION</span></span>
<span data-ttu-id="7bfa9-108">Polecenie cmdlet **Remove-AzureBatchTask** usuwa zadanie wsadowe usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="7bfa9-109">To polecenie cmdlet monituje o potwierdzenie, chyba że parametr *Force* zostanie określony.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="7bfa9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7bfa9-110">EXAMPLES</span></span>

### <span data-ttu-id="7bfa9-111">Przykład 1: usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="7bfa9-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="7bfa9-112">To polecenie usuwa zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="7bfa9-113">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="7bfa9-114">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7bfa9-115">Przykład 2: usuwanie zadania wsadowego przy użyciu rurociągu bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="7bfa9-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="7bfa9-116">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task26 w zadaniu z identyfikatorem zadania ID-000001 przy użyciu polecenia cmdlet **Get-AzureBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="7bfa9-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="7bfa9-117">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7bfa9-118">Polecenie usunie to zadanie.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-118">The command deletes that task.</span></span>
<span data-ttu-id="7bfa9-119">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="7bfa9-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7bfa9-120">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7bfa9-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7bfa9-121">PARAMETERS</span></span>

### <span data-ttu-id="7bfa9-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7bfa9-122">-BatchContext</span></span>
<span data-ttu-id="7bfa9-123">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7bfa9-124">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7bfa9-125">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7bfa9-126">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7bfa9-127">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7bfa9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bfa9-128">-DefaultProfile</span></span>
<span data-ttu-id="7bfa9-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bfa9-130">-Force</span><span class="sxs-lookup"><span data-stu-id="7bfa9-130">-Force</span></span>
<span data-ttu-id="7bfa9-131">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bfa9-132">-ID</span><span class="sxs-lookup"><span data-stu-id="7bfa9-132">-Id</span></span>
<span data-ttu-id="7bfa9-133">Określa identyfikator zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="7bfa9-134">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="7bfa9-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7bfa9-135">-InputObject</span></span>
<span data-ttu-id="7bfa9-136">Określa zadanie, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="7bfa9-137">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="7bfa9-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="7bfa9-138">-JobId</span></span>
<span data-ttu-id="7bfa9-139">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="7bfa9-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7bfa9-140">-Confirm</span></span>
<span data-ttu-id="7bfa9-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bfa9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bfa9-142">-WhatIf</span></span>
<span data-ttu-id="7bfa9-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bfa9-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bfa9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bfa9-145">CommonParameters</span></span>
<span data-ttu-id="7bfa9-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bfa9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bfa9-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bfa9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bfa9-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bfa9-148">INPUTS</span></span>

### <span data-ttu-id="7bfa9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7bfa9-149">System.String</span></span>

### <span data-ttu-id="7bfa9-150">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="7bfa9-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="7bfa9-151">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7bfa9-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7bfa9-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7bfa9-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="7bfa9-153">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7bfa9-153">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="7bfa9-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7bfa9-154">OUTPUTS</span></span>

### <span data-ttu-id="7bfa9-155">System. void</span><span class="sxs-lookup"><span data-stu-id="7bfa9-155">System.Void</span></span>

## <span data-ttu-id="7bfa9-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7bfa9-156">NOTES</span></span>

## <span data-ttu-id="7bfa9-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7bfa9-157">RELATED LINKS</span></span>

[<span data-ttu-id="7bfa9-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7bfa9-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7bfa9-159">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7bfa9-159">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="7bfa9-160">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7bfa9-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="7bfa9-161">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7bfa9-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="7bfa9-162">Zatrzymaj — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="7bfa9-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="7bfa9-163">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7bfa9-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


