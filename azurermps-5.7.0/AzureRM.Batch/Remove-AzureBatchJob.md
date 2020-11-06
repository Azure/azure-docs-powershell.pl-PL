---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: f6a7d03370184b45cc8066e2f17842187cbab98c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553040"
---
# <span data-ttu-id="06222-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="06222-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="06222-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06222-102">SYNOPSIS</span></span>
<span data-ttu-id="06222-103">Umożliwia usunięcie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="06222-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06222-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06222-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06222-105">Opis</span><span class="sxs-lookup"><span data-stu-id="06222-105">DESCRIPTION</span></span>
<span data-ttu-id="06222-106">Polecenie cmdlet **Remove-AzureBatchJob** usuwa zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="06222-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="06222-107">To polecenie cmdlet monituje o potwierdzenie przed usunięciem zadania, o ile parametr *Force* nie zostanie określony.</span><span class="sxs-lookup"><span data-stu-id="06222-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="06222-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06222-108">EXAMPLES</span></span>

### <span data-ttu-id="06222-109">Przykład 1: usuwanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="06222-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="06222-110">To polecenie umożliwia usunięcie zadania o identyfikatorze zadania ID-000001.</span><span class="sxs-lookup"><span data-stu-id="06222-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="06222-111">Polecenie wyświetli monit o potwierdzenie przed usunięciem zadania.</span><span class="sxs-lookup"><span data-stu-id="06222-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="06222-112">Użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="06222-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="06222-113">Przykład 2: usuwanie zadania wsadowego bez potwierdzenia przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="06222-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="06222-114">To polecenie pobiera zadanie o IDENTYFIKATORze Job-000002 przy użyciu polecenia cmdlet Get-AzureBatchJob.</span><span class="sxs-lookup"><span data-stu-id="06222-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="06222-115">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="06222-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="06222-116">Polecenie usunie to zadanie.</span><span class="sxs-lookup"><span data-stu-id="06222-116">The command deletes that job.</span></span>
<span data-ttu-id="06222-117">Polecenie zawiera parametr *Force* , dlatego nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06222-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="06222-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06222-118">PARAMETERS</span></span>

### <span data-ttu-id="06222-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="06222-119">-BatchContext</span></span>
<span data-ttu-id="06222-120">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="06222-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="06222-121">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="06222-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="06222-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="06222-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="06222-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="06222-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="06222-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="06222-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="06222-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06222-125">-DefaultProfile</span></span>
<span data-ttu-id="06222-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06222-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06222-127">-Force</span><span class="sxs-lookup"><span data-stu-id="06222-127">-Force</span></span>
<span data-ttu-id="06222-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="06222-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06222-129">-ID</span><span class="sxs-lookup"><span data-stu-id="06222-129">-Id</span></span>
<span data-ttu-id="06222-130">Określa identyfikator zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06222-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="06222-131">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="06222-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06222-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06222-132">-Confirm</span></span>
<span data-ttu-id="06222-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06222-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06222-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06222-134">-WhatIf</span></span>
<span data-ttu-id="06222-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06222-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06222-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06222-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06222-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06222-137">CommonParameters</span></span>
<span data-ttu-id="06222-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06222-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06222-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06222-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06222-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06222-140">INPUTS</span></span>

### <span data-ttu-id="06222-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="06222-141">BatchAccountContext</span></span>
<span data-ttu-id="06222-142">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="06222-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="06222-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06222-143">OUTPUTS</span></span>

## <span data-ttu-id="06222-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06222-144">NOTES</span></span>

## <span data-ttu-id="06222-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06222-145">RELATED LINKS</span></span>

[<span data-ttu-id="06222-146">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="06222-146">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="06222-147">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="06222-147">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="06222-148">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="06222-148">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="06222-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="06222-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="06222-150">Nowe — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="06222-150">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="06222-151">Zatrzymaj — AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="06222-151">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="06222-152">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="06222-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


