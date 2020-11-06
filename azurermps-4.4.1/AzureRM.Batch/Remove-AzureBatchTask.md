---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 6200ee0d929aaadccb8e2be0e8fb646929907d73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551087"
---
# <span data-ttu-id="c16be-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c16be-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="c16be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c16be-102">SYNOPSIS</span></span>
<span data-ttu-id="c16be-103">Umożliwia usunięcie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c16be-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c16be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c16be-104">SYNTAX</span></span>

### <span data-ttu-id="c16be-105">Identyfikacji</span><span class="sxs-lookup"><span data-stu-id="c16be-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c16be-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="c16be-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c16be-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c16be-107">DESCRIPTION</span></span>
<span data-ttu-id="c16be-108">Polecenie cmdlet **Remove-AzureBatchTask** usuwa zadanie wsadowe usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="c16be-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="c16be-109">To polecenie cmdlet monituje o potwierdzenie, chyba że parametr *Force* zostanie określony.</span><span class="sxs-lookup"><span data-stu-id="c16be-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="c16be-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c16be-110">EXAMPLES</span></span>

### <span data-ttu-id="c16be-111">Przykład 1: usuwanie zadania wsadowego według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="c16be-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="c16be-112">To polecenie usuwa zadanie o IDENTYFIKATORze Task23 w ramach zadania o identyfikatorze Job ID-000001.</span><span class="sxs-lookup"><span data-stu-id="c16be-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="c16be-113">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c16be-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="c16be-114">Użyj polecenia cmdlet **Get-AzureRmBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="c16be-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c16be-115">Przykład 2: usuwanie zadania wsadowego przy użyciu rurociągu bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="c16be-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="c16be-116">To polecenie pobiera zadanie wsadowe o IDENTYFIKATORze Task26 w zadaniu z identyfikatorem zadania ID-000001 przy użyciu polecenia cmdlet **Get-AzureBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="c16be-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="c16be-117">Polecenie przekazuje to zadanie do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="c16be-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c16be-118">Polecenie usunie to zadanie.</span><span class="sxs-lookup"><span data-stu-id="c16be-118">The command deletes that task.</span></span>
<span data-ttu-id="c16be-119">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="c16be-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c16be-120">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c16be-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c16be-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c16be-121">PARAMETERS</span></span>

### <span data-ttu-id="c16be-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c16be-122">-BatchContext</span></span>
<span data-ttu-id="c16be-123">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="c16be-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c16be-124">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="c16be-124">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c16be-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c16be-125">-Force</span></span>
<span data-ttu-id="c16be-126">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c16be-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c16be-127">-ID</span><span class="sxs-lookup"><span data-stu-id="c16be-127">-Id</span></span>
<span data-ttu-id="c16be-128">Określa identyfikator zadania, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c16be-128">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="c16be-129">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="c16be-129">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="c16be-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c16be-130">-InputObject</span></span>
<span data-ttu-id="c16be-131">Określa zadanie, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c16be-131">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="c16be-132">Aby uzyskać obiekt **PSCloudTask** , użyj polecenia cmdlet Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="c16be-132">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="c16be-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="c16be-133">-JobId</span></span>
<span data-ttu-id="c16be-134">Określa identyfikator zadania, które zawiera zadanie.</span><span class="sxs-lookup"><span data-stu-id="c16be-134">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="c16be-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c16be-135">-Confirm</span></span>
<span data-ttu-id="c16be-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c16be-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c16be-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c16be-137">-WhatIf</span></span>
<span data-ttu-id="c16be-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c16be-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c16be-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c16be-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c16be-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16be-140">-DefaultProfile</span></span>
<span data-ttu-id="c16be-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c16be-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c16be-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16be-142">CommonParameters</span></span>
<span data-ttu-id="c16be-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c16be-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16be-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c16be-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16be-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c16be-145">INPUTS</span></span>

### <span data-ttu-id="c16be-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c16be-146">BatchAccountContext</span></span>
<span data-ttu-id="c16be-147">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c16be-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c16be-148">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="c16be-148">PSCloudTask</span></span>
<span data-ttu-id="c16be-149">Parametr "Inputobject" przyjmuje wartość typu "PSCloudTask" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c16be-149">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="c16be-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c16be-150">OUTPUTS</span></span>

## <span data-ttu-id="c16be-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c16be-151">NOTES</span></span>

## <span data-ttu-id="c16be-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c16be-152">RELATED LINKS</span></span>

[<span data-ttu-id="c16be-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c16be-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c16be-154">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c16be-154">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="c16be-155">Nowe — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c16be-155">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="c16be-156">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c16be-156">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="c16be-157">Zatrzymaj — AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="c16be-157">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="c16be-158">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c16be-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


