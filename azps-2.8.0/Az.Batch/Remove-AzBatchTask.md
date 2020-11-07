---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: c2b198359bbd793353c9b416a631d94cad0709fa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93897009"
---
# <span data-ttu-id="28801-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="28801-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="28801-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28801-102">SYNOPSIS</span></span>
<span data-ttu-id="28801-103">Umożliwia usunięcie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="28801-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="28801-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28801-104">SYNTAX</span></span>

### <span data-ttu-id="28801-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="28801-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28801-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="28801-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28801-107">Opis</span><span class="sxs-lookup"><span data-stu-id="28801-107">DESCRIPTION</span></span>
<span data-ttu-id="28801-108">Polecenie cmdlet **Remove-AzBatchTask** usuwa zadanie wsadowe usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="28801-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="28801-109">To polecenie cmdlet monituje o potwierdzenie, chyba że parametr *Force* zostanie określony.</span><span class="sxs-lookup"><span data-stu-id="28801-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="28801-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28801-110">EXAMPLES</span></span>

### <span data-ttu-id="28801-111">Przykład 1: usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="28801-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="28801-112">To polecenie usuwa zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="28801-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="28801-113">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="28801-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="28801-114">Użyj polecenia cmdlet **Get-AzBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="28801-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="28801-115">Przykład 2: usuwanie zadania wsadowego przy użyciu rurociągu bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="28801-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="28801-116">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task26 w zadaniu z identyfikatorem zadania ID-000001 przy użyciu polecenia cmdlet **Get-AzBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="28801-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="28801-117">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="28801-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="28801-118">Polecenie usunie to zadanie.</span><span class="sxs-lookup"><span data-stu-id="28801-118">The command deletes that task.</span></span>
<span data-ttu-id="28801-119">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="28801-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="28801-120">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="28801-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="28801-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28801-121">PARAMETERS</span></span>

### <span data-ttu-id="28801-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="28801-122">-BatchContext</span></span>
<span data-ttu-id="28801-123">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="28801-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="28801-124">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="28801-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="28801-125">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="28801-125">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="28801-126">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="28801-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="28801-127">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="28801-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="28801-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28801-128">-DefaultProfile</span></span>
<span data-ttu-id="28801-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28801-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28801-130">-Force</span><span class="sxs-lookup"><span data-stu-id="28801-130">-Force</span></span>
<span data-ttu-id="28801-131">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="28801-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28801-132">-ID</span><span class="sxs-lookup"><span data-stu-id="28801-132">-Id</span></span>
<span data-ttu-id="28801-133">Określa identyfikator zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28801-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="28801-134">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="28801-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="28801-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28801-135">-InputObject</span></span>
<span data-ttu-id="28801-136">Określa zadanie, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28801-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="28801-137">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="28801-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="28801-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="28801-138">-JobId</span></span>
<span data-ttu-id="28801-139">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="28801-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="28801-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28801-140">-Confirm</span></span>
<span data-ttu-id="28801-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28801-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28801-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28801-142">-WhatIf</span></span>
<span data-ttu-id="28801-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28801-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28801-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="28801-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28801-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28801-145">CommonParameters</span></span>
<span data-ttu-id="28801-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28801-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28801-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28801-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28801-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28801-148">INPUTS</span></span>

### <span data-ttu-id="28801-149">System. String</span><span class="sxs-lookup"><span data-stu-id="28801-149">System.String</span></span>

### <span data-ttu-id="28801-150">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="28801-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="28801-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="28801-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="28801-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28801-152">OUTPUTS</span></span>

### <span data-ttu-id="28801-153">System. void</span><span class="sxs-lookup"><span data-stu-id="28801-153">System.Void</span></span>

## <span data-ttu-id="28801-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28801-154">NOTES</span></span>

## <span data-ttu-id="28801-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28801-155">RELATED LINKS</span></span>

[<span data-ttu-id="28801-156">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="28801-156">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="28801-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="28801-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="28801-158">Nowe — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="28801-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="28801-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="28801-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="28801-160">Zatrzymaj — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="28801-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="28801-161">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="28801-161">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


