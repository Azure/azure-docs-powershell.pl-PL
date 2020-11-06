---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: fdcc1b7a119028d792000b10d26aa7900ab0477b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547595"
---
# <span data-ttu-id="53adb-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="53adb-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="53adb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53adb-102">SYNOPSIS</span></span>
<span data-ttu-id="53adb-103">Uaktywnia ponownie zadanie.</span><span class="sxs-lookup"><span data-stu-id="53adb-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53adb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53adb-104">SYNTAX</span></span>

### <span data-ttu-id="53adb-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="53adb-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53adb-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="53adb-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53adb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="53adb-107">DESCRIPTION</span></span>
<span data-ttu-id="53adb-108">Polecenie cmdlet **enable-AzureBatchTask** uaktywnia ponownie zadanie.</span><span class="sxs-lookup"><span data-stu-id="53adb-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="53adb-109">Jeśli zadanie przekroczyło liczbę ponownych prób, to polecenie cmdlet umożliwia jednak jego uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="53adb-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="53adb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53adb-110">EXAMPLES</span></span>

### <span data-ttu-id="53adb-111">Przykład 1: ponowne uaktywnianie zadania</span><span class="sxs-lookup"><span data-stu-id="53adb-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="53adb-112">To polecenie uaktywnia ponownie Zadanie2 zadań w Job7 zadań.</span><span class="sxs-lookup"><span data-stu-id="53adb-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="53adb-113">Przykład 2: ponowne uaktywnianie zadania przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="53adb-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="53adb-114">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task3 w zadaniu o IDENTYFIKATORze Job8 przy użyciu polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="53adb-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="53adb-115">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="53adb-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="53adb-116">Polecenie ponownie uaktywnia to zadanie.</span><span class="sxs-lookup"><span data-stu-id="53adb-116">The command reactivates that task.</span></span>

## <span data-ttu-id="53adb-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53adb-117">PARAMETERS</span></span>

### <span data-ttu-id="53adb-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="53adb-118">-BatchContext</span></span>
<span data-ttu-id="53adb-119">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="53adb-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="53adb-120">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="53adb-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="53adb-121">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="53adb-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="53adb-122">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="53adb-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="53adb-123">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="53adb-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="53adb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53adb-124">-DefaultProfile</span></span>
<span data-ttu-id="53adb-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53adb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53adb-126">-ID</span><span class="sxs-lookup"><span data-stu-id="53adb-126">-Id</span></span>
<span data-ttu-id="53adb-127">Określa identyfikator zadania do ponownego aktywowania.</span><span class="sxs-lookup"><span data-stu-id="53adb-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="53adb-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="53adb-128">-JobId</span></span>
<span data-ttu-id="53adb-129">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="53adb-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="53adb-130">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="53adb-130">-Task</span></span>
<span data-ttu-id="53adb-131">Określa zadanie, które zostanie ponownie uaktywnione przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="53adb-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="53adb-132">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="53adb-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="53adb-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53adb-133">-Confirm</span></span>
<span data-ttu-id="53adb-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53adb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53adb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53adb-135">-WhatIf</span></span>
<span data-ttu-id="53adb-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53adb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53adb-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53adb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53adb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53adb-138">CommonParameters</span></span>
<span data-ttu-id="53adb-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53adb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53adb-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53adb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53adb-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53adb-141">INPUTS</span></span>

### <span data-ttu-id="53adb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="53adb-142">System.String</span></span>

### <span data-ttu-id="53adb-143">Microsoft.Azure.Commands.Batch. Modele. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="53adb-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="53adb-144">Parametry: zadanie (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53adb-144">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="53adb-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="53adb-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="53adb-146">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53adb-146">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="53adb-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53adb-147">OUTPUTS</span></span>

### <span data-ttu-id="53adb-148">System. void</span><span class="sxs-lookup"><span data-stu-id="53adb-148">System.Void</span></span>

## <span data-ttu-id="53adb-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53adb-149">NOTES</span></span>

## <span data-ttu-id="53adb-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53adb-150">RELATED LINKS</span></span>

[<span data-ttu-id="53adb-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="53adb-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="53adb-152">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="53adb-152">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="53adb-153">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="53adb-153">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="53adb-154">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="53adb-154">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="53adb-155">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="53adb-155">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="53adb-156">Zatrzymaj — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="53adb-156">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


