---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719373"
---
# <span data-ttu-id="a3628-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3628-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="a3628-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3628-102">SYNOPSIS</span></span>
<span data-ttu-id="a3628-103">Uaktywnia ponownie zadanie.</span><span class="sxs-lookup"><span data-stu-id="a3628-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3628-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3628-104">SYNTAX</span></span>

### <span data-ttu-id="a3628-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="a3628-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3628-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3628-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3628-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a3628-107">DESCRIPTION</span></span>
<span data-ttu-id="a3628-108">Polecenie cmdlet **enable-AzureBatchTask** uaktywnia ponownie zadanie.</span><span class="sxs-lookup"><span data-stu-id="a3628-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="a3628-109">Jeśli zadanie przekroczyło liczbę ponownych prób, to polecenie cmdlet umożliwia jednak jego uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="a3628-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="a3628-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3628-110">EXAMPLES</span></span>

### <span data-ttu-id="a3628-111">Przykład 1: ponowne uaktywnianie zadania</span><span class="sxs-lookup"><span data-stu-id="a3628-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="a3628-112">To polecenie uaktywnia ponownie Zadanie2 zadań w Job7 zadań.</span><span class="sxs-lookup"><span data-stu-id="a3628-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="a3628-113">Przykład 2: ponowne uaktywnianie zadania przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="a3628-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="a3628-114">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task3 w zadaniu o IDENTYFIKATORze Job8 przy użyciu polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="a3628-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="a3628-115">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="a3628-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a3628-116">Polecenie ponownie uaktywnia to zadanie.</span><span class="sxs-lookup"><span data-stu-id="a3628-116">The command reactivates that task.</span></span>

## <span data-ttu-id="a3628-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3628-117">PARAMETERS</span></span>

### <span data-ttu-id="a3628-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a3628-118">-BatchContext</span></span>
<span data-ttu-id="a3628-119">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a3628-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a3628-120">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="a3628-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a3628-121">-ID</span><span class="sxs-lookup"><span data-stu-id="a3628-121">-Id</span></span>
<span data-ttu-id="a3628-122">Określa identyfikator zadania do ponownego aktywowania.</span><span class="sxs-lookup"><span data-stu-id="a3628-122">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="a3628-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="a3628-123">-JobId</span></span>
<span data-ttu-id="a3628-124">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="a3628-124">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="a3628-125">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="a3628-125">-Task</span></span>
<span data-ttu-id="a3628-126">Określa zadanie, które zostanie ponownie uaktywnione przez ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="a3628-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="a3628-127">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="a3628-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="a3628-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3628-128">-Confirm</span></span>
<span data-ttu-id="a3628-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3628-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3628-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3628-130">-WhatIf</span></span>
<span data-ttu-id="a3628-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3628-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3628-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3628-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3628-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3628-133">-DefaultProfile</span></span>
<span data-ttu-id="a3628-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3628-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3628-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3628-135">CommonParameters</span></span>
<span data-ttu-id="a3628-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3628-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3628-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3628-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3628-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3628-138">INPUTS</span></span>

### <span data-ttu-id="a3628-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a3628-139">BatchAccountContext</span></span>
<span data-ttu-id="a3628-140">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="a3628-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a3628-141">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="a3628-141">PSCloudTask</span></span>
<span data-ttu-id="a3628-142">Parametr "zadanie" akceptuje wartość typu "PSCloudTask" z potoku.</span><span class="sxs-lookup"><span data-stu-id="a3628-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="a3628-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3628-143">OUTPUTS</span></span>

## <span data-ttu-id="a3628-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3628-144">NOTES</span></span>

## <span data-ttu-id="a3628-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3628-145">RELATED LINKS</span></span>

[<span data-ttu-id="a3628-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a3628-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a3628-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3628-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="a3628-148">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3628-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="a3628-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3628-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="a3628-150">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3628-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="a3628-151">Zatrzymaj — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="a3628-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


