---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: e067eea86e3a4350d08c5c0f9ec34b4af65b07f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345589"
---
# <span data-ttu-id="774f4-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="774f4-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="774f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="774f4-102">SYNOPSIS</span></span>
<span data-ttu-id="774f4-103">Umożliwia usunięcie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="774f4-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="774f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="774f4-104">SYNTAX</span></span>

### <span data-ttu-id="774f4-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="774f4-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="774f4-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="774f4-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="774f4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="774f4-107">DESCRIPTION</span></span>
<span data-ttu-id="774f4-108">Polecenie cmdlet **Remove-AzBatchTask** usuwa zadanie wsadowe usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="774f4-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="774f4-109">To polecenie cmdlet monituje o potwierdzenie, chyba że parametr *Force* zostanie określony.</span><span class="sxs-lookup"><span data-stu-id="774f4-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="774f4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="774f4-110">EXAMPLES</span></span>

### <span data-ttu-id="774f4-111">Przykład 1: usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="774f4-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="774f4-112">To polecenie usuwa zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="774f4-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="774f4-113">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="774f4-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="774f4-114">Użyj polecenia cmdlet **Get-AzBatchAccountKey** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="774f4-114">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="774f4-115">Przykład 2: usuwanie zadania wsadowego przy użyciu rurociągu bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="774f4-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="774f4-116">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task26 w zadaniu z identyfikatorem zadania ID-000001 przy użyciu polecenia cmdlet **Get-AzBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="774f4-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="774f4-117">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="774f4-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="774f4-118">Polecenie usunie to zadanie.</span><span class="sxs-lookup"><span data-stu-id="774f4-118">The command deletes that task.</span></span>
<span data-ttu-id="774f4-119">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="774f4-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="774f4-120">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="774f4-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="774f4-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="774f4-121">PARAMETERS</span></span>

### <span data-ttu-id="774f4-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="774f4-122">-BatchContext</span></span>
<span data-ttu-id="774f4-123">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="774f4-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="774f4-124">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="774f4-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="774f4-125">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="774f4-125">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="774f4-126">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="774f4-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="774f4-127">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="774f4-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="774f4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="774f4-128">-DefaultProfile</span></span>
<span data-ttu-id="774f4-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="774f4-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="774f4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="774f4-130">-Force</span></span>
<span data-ttu-id="774f4-131">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="774f4-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="774f4-132">-ID</span><span class="sxs-lookup"><span data-stu-id="774f4-132">-Id</span></span>
<span data-ttu-id="774f4-133">Określa identyfikator zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="774f4-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="774f4-134">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="774f4-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="774f4-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="774f4-135">-InputObject</span></span>
<span data-ttu-id="774f4-136">Określa zadanie, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="774f4-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="774f4-137">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="774f4-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="774f4-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="774f4-138">-JobId</span></span>
<span data-ttu-id="774f4-139">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="774f4-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="774f4-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="774f4-140">-Confirm</span></span>
<span data-ttu-id="774f4-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="774f4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="774f4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="774f4-142">-WhatIf</span></span>
<span data-ttu-id="774f4-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="774f4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="774f4-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="774f4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="774f4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="774f4-145">CommonParameters</span></span>
<span data-ttu-id="774f4-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="774f4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="774f4-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="774f4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="774f4-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="774f4-148">INPUTS</span></span>

### <span data-ttu-id="774f4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="774f4-149">System.String</span></span>

### <span data-ttu-id="774f4-150">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="774f4-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="774f4-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="774f4-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="774f4-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="774f4-152">OUTPUTS</span></span>

### <span data-ttu-id="774f4-153">System. void</span><span class="sxs-lookup"><span data-stu-id="774f4-153">System.Void</span></span>

## <span data-ttu-id="774f4-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="774f4-154">NOTES</span></span>

## <span data-ttu-id="774f4-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="774f4-155">RELATED LINKS</span></span>

[<span data-ttu-id="774f4-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="774f4-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="774f4-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="774f4-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="774f4-158">Nowe — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="774f4-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="774f4-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="774f4-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="774f4-160">Zatrzymaj — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="774f4-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="774f4-161">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="774f4-161">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
