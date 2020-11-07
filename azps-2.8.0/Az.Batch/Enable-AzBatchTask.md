---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 1eef03db73e6b1afcb2c9ca92f507e8b0f3ff0ae
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93897021"
---
# <span data-ttu-id="c3c5e-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c3c5e-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="c3c5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c5e-103">Uaktywnia ponownie zadanie.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-103">Reactivates a task.</span></span>

## <span data-ttu-id="c3c5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3c5e-104">SYNTAX</span></span>

### <span data-ttu-id="c3c5e-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="c3c5e-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3c5e-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3c5e-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3c5e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c3c5e-107">DESCRIPTION</span></span>
<span data-ttu-id="c3c5e-108">Polecenie cmdlet **enable-AzBatchTask** uaktywnia ponownie zadanie.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="c3c5e-109">Jeśli zadanie przekroczyło liczbę ponownych prób, to polecenie cmdlet umożliwia jednak jego uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="c3c5e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3c5e-110">EXAMPLES</span></span>

### <span data-ttu-id="c3c5e-111">Przykład 1: ponowne uaktywnianie zadania</span><span class="sxs-lookup"><span data-stu-id="c3c5e-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="c3c5e-112">To polecenie uaktywnia ponownie Zadanie2 zadań w Job7 zadań.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="c3c5e-113">Przykład 2: ponowne uaktywnianie zadania przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="c3c5e-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="c3c5e-114">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task3 w zadaniu o IDENTYFIKATORze Job8 przy użyciu polecenia cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="c3c5e-115">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c3c5e-116">Polecenie ponownie uaktywnia to zadanie.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-116">The command reactivates that task.</span></span>

## <span data-ttu-id="c3c5e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3c5e-117">PARAMETERS</span></span>

### <span data-ttu-id="c3c5e-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c3c5e-118">-BatchContext</span></span>
<span data-ttu-id="c3c5e-119">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c3c5e-120">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c3c5e-121">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c3c5e-122">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c3c5e-123">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c3c5e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c5e-124">-DefaultProfile</span></span>
<span data-ttu-id="c3c5e-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3c5e-126">-ID</span><span class="sxs-lookup"><span data-stu-id="c3c5e-126">-Id</span></span>
<span data-ttu-id="c3c5e-127">Określa identyfikator zadania do ponownego aktywowania.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="c3c5e-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="c3c5e-128">-JobId</span></span>
<span data-ttu-id="c3c5e-129">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="c3c5e-130">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="c3c5e-130">-Task</span></span>
<span data-ttu-id="c3c5e-131">Określa zadanie, które zostanie ponownie uaktywnione przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="c3c5e-132">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="c3c5e-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3c5e-133">-Confirm</span></span>
<span data-ttu-id="c3c5e-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3c5e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3c5e-135">-WhatIf</span></span>
<span data-ttu-id="c3c5e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3c5e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3c5e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c5e-138">CommonParameters</span></span>
<span data-ttu-id="c3c5e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3c5e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c5e-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3c5e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c5e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3c5e-141">INPUTS</span></span>

### <span data-ttu-id="c3c5e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c3c5e-142">System.String</span></span>

### <span data-ttu-id="c3c5e-143">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="c3c5e-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="c3c5e-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3c5e-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c3c5e-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3c5e-145">OUTPUTS</span></span>

### <span data-ttu-id="c3c5e-146">System. void</span><span class="sxs-lookup"><span data-stu-id="c3c5e-146">System.Void</span></span>

## <span data-ttu-id="c3c5e-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3c5e-147">NOTES</span></span>

## <span data-ttu-id="c3c5e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3c5e-148">RELATED LINKS</span></span>

[<span data-ttu-id="c3c5e-149">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c3c5e-149">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c3c5e-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c3c5e-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="c3c5e-151">Nowe — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c3c5e-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="c3c5e-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c3c5e-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="c3c5e-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c3c5e-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="c3c5e-154">Zatrzymaj — AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="c3c5e-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


