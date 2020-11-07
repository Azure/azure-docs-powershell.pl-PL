---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 398671292e67520977a683c3da9178b33dc69329
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706654"
---
# <span data-ttu-id="9c0a1-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9c0a1-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="9c0a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="9c0a1-103">Usuwa harmonogram zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="9c0a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c0a1-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c0a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9c0a1-105">DESCRIPTION</span></span>
<span data-ttu-id="9c0a1-106">Polecenie cmdlet **Remove-AzBatchJobSchedule** usuwa harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="9c0a1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c0a1-107">EXAMPLES</span></span>

### <span data-ttu-id="9c0a1-108">Przykład 1: Usuwanie harmonogramu zadań wsadowych</span><span class="sxs-lookup"><span data-stu-id="9c0a1-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="9c0a1-109">To polecenie usuwa harmonogram zadań o IDENTYFIKATORze MyJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="9c0a1-110">Polecenie wyświetli monit o potwierdzenie przed usunięciem zadania.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="9c0a1-111">Użyj polecenia cmdlet Get-AzBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9c0a1-112">Przykład 2: usuwanie zadania wsadowego bez potwierdzenia przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="9c0a1-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="9c0a1-113">To polecenie pobiera harmonogram zadań o IDENTYFIKATORze MyJobSchedule przy użyciu polecenia cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="9c0a1-114">Polecenie przekazuje ten harmonogram zadań do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9c0a1-115">Polecenie usunie harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="9c0a1-116">Polecenie zawiera parametr *Force* , dlatego nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9c0a1-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c0a1-117">PARAMETERS</span></span>

### <span data-ttu-id="9c0a1-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9c0a1-118">-BatchContext</span></span>
<span data-ttu-id="9c0a1-119">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9c0a1-120">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9c0a1-121">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9c0a1-122">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9c0a1-123">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9c0a1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c0a1-124">-DefaultProfile</span></span>
<span data-ttu-id="9c0a1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c0a1-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9c0a1-126">-Force</span></span>
<span data-ttu-id="9c0a1-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c0a1-128">-ID</span><span class="sxs-lookup"><span data-stu-id="9c0a1-128">-Id</span></span>
<span data-ttu-id="9c0a1-129">Określa identyfikator harmonogramu zadań, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="9c0a1-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c0a1-130">-Confirm</span></span>
<span data-ttu-id="9c0a1-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c0a1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c0a1-132">-WhatIf</span></span>
<span data-ttu-id="9c0a1-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c0a1-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c0a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c0a1-135">CommonParameters</span></span>
<span data-ttu-id="9c0a1-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c0a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c0a1-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c0a1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c0a1-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c0a1-138">INPUTS</span></span>

### <span data-ttu-id="9c0a1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9c0a1-139">System.String</span></span>

### <span data-ttu-id="9c0a1-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9c0a1-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="9c0a1-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c0a1-141">OUTPUTS</span></span>

### <span data-ttu-id="9c0a1-142">System. void</span><span class="sxs-lookup"><span data-stu-id="9c0a1-142">System.Void</span></span>

## <span data-ttu-id="9c0a1-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c0a1-143">NOTES</span></span>

## <span data-ttu-id="9c0a1-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c0a1-144">RELATED LINKS</span></span>

[<span data-ttu-id="9c0a1-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9c0a1-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="9c0a1-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9c0a1-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="9c0a1-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9c0a1-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="9c0a1-148">Nowe — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9c0a1-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="9c0a1-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9c0a1-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="9c0a1-150">Zatrzymaj — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="9c0a1-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

