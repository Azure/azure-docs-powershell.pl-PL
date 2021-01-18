---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502125"
---
# <span data-ttu-id="9f29a-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f29a-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="9f29a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f29a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f29a-103">Umożliwia usunięcie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9f29a-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="9f29a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f29a-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f29a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9f29a-105">DESCRIPTION</span></span>
<span data-ttu-id="9f29a-106">Polecenie cmdlet **Remove-AzBatchJob** usuwa zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="9f29a-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="9f29a-107">To polecenie cmdlet monituje o potwierdzenie przed usunięciem zadania, o ile parametr *Force* nie zostanie określony.</span><span class="sxs-lookup"><span data-stu-id="9f29a-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="9f29a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f29a-108">EXAMPLES</span></span>

### <span data-ttu-id="9f29a-109">Przykład 1: usuwanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="9f29a-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="9f29a-110">To polecenie umożliwia usunięcie zadania o identyfikatorze zadania ID-000001.</span><span class="sxs-lookup"><span data-stu-id="9f29a-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="9f29a-111">Polecenie wyświetli monit o potwierdzenie przed usunięciem zadania.</span><span class="sxs-lookup"><span data-stu-id="9f29a-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="9f29a-112">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="9f29a-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9f29a-113">Przykład 2: usuwanie zadania wsadowego bez potwierdzenia przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="9f29a-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="9f29a-114">To polecenie pobiera zadanie o IDENTYFIKATORze Job-000002 przy użyciu polecenia cmdlet Get-AzBatchJob.</span><span class="sxs-lookup"><span data-stu-id="9f29a-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="9f29a-115">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9f29a-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9f29a-116">Polecenie usunie to zadanie.</span><span class="sxs-lookup"><span data-stu-id="9f29a-116">The command deletes that job.</span></span>
<span data-ttu-id="9f29a-117">Polecenie zawiera parametr *Force* , dlatego nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9f29a-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9f29a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f29a-118">PARAMETERS</span></span>

### <span data-ttu-id="9f29a-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9f29a-119">-BatchContext</span></span>
<span data-ttu-id="9f29a-120">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9f29a-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9f29a-121">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9f29a-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9f29a-122">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="9f29a-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9f29a-123">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="9f29a-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9f29a-124">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9f29a-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9f29a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f29a-125">-DefaultProfile</span></span>
<span data-ttu-id="9f29a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f29a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f29a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9f29a-127">-Force</span></span>
<span data-ttu-id="9f29a-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9f29a-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f29a-129">-ID</span><span class="sxs-lookup"><span data-stu-id="9f29a-129">-Id</span></span>
<span data-ttu-id="9f29a-130">Określa identyfikator zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f29a-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="9f29a-131">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="9f29a-131">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f29a-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f29a-132">-Confirm</span></span>
<span data-ttu-id="9f29a-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f29a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f29a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f29a-134">-WhatIf</span></span>
<span data-ttu-id="9f29a-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f29a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f29a-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9f29a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f29a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f29a-137">CommonParameters</span></span>
<span data-ttu-id="9f29a-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f29a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f29a-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f29a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f29a-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f29a-140">INPUTS</span></span>

### <span data-ttu-id="9f29a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9f29a-141">System.String</span></span>

### <span data-ttu-id="9f29a-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9f29a-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9f29a-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f29a-143">OUTPUTS</span></span>

### <span data-ttu-id="9f29a-144">System. void</span><span class="sxs-lookup"><span data-stu-id="9f29a-144">System.Void</span></span>

## <span data-ttu-id="9f29a-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f29a-145">NOTES</span></span>

## <span data-ttu-id="9f29a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f29a-146">RELATED LINKS</span></span>

[<span data-ttu-id="9f29a-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f29a-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="9f29a-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f29a-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="9f29a-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f29a-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="9f29a-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="9f29a-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="9f29a-151">Nowe — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f29a-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="9f29a-152">Zatrzymaj — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="9f29a-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="9f29a-153">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="9f29a-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
