---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239230"
---
# <span data-ttu-id="02989-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="02989-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="02989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02989-102">SYNOPSIS</span></span>
<span data-ttu-id="02989-103">Usuwa węzły obliczeniowe z puli.</span><span class="sxs-lookup"><span data-stu-id="02989-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="02989-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="02989-104">SYNTAX</span></span>

### <span data-ttu-id="02989-105">Identyfikator (domyślne)</span><span class="sxs-lookup"><span data-stu-id="02989-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02989-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="02989-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02989-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="02989-107">DESCRIPTION</span></span>
<span data-ttu-id="02989-108">Polecenie **cmdlet Remove-AzBatchComputeNode** usuwa węzły obliczeniowe usługi Azure Batch z puli.</span><span class="sxs-lookup"><span data-stu-id="02989-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="02989-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="02989-109">EXAMPLES</span></span>

### <span data-ttu-id="02989-110">Przykład 1. Usuwanie węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="02989-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="02989-111">To polecenie usuwa węzeł obliczeniowy o określonym identyfikatorze z puli, która ma pulę identyfikatorów 07.</span><span class="sxs-lookup"><span data-stu-id="02989-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="02989-112">To polecenie określa opcję Zakończ alokację.</span><span class="sxs-lookup"><span data-stu-id="02989-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="02989-113">Czas zmiany rozmiaru to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="02989-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="02989-114">Przykład 2. Usuwanie węzła obliczeniowego przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="02989-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="02989-115">To polecenie pobiera węzeł obliczeniowy, który ma określony identyfikator z puli, która ma identyfikator Pool07, przy użyciu Get-AzBatchComputeNode cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02989-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="02989-116">Polecenie przekazuje ten węzeł do bieżącego polecenia cmdlet przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="02989-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="02989-117">Bieżące polecenie cmdlet usuwa węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="02989-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="02989-118">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="02989-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="02989-119">Dlatego polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02989-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="02989-120">Przykład 3. Usuwanie wielu węzłów</span><span class="sxs-lookup"><span data-stu-id="02989-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="02989-121">To polecenie usuwa dwa węzły obliczeniowe z puli, która ma pulę identyfikatorów 07.</span><span class="sxs-lookup"><span data-stu-id="02989-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="02989-122">To polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02989-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="02989-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02989-123">PARAMETERS</span></span>

### <span data-ttu-id="02989-124">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="02989-124">-BatchContext</span></span>
<span data-ttu-id="02989-125">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="02989-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="02989-126">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="02989-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="02989-127">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="02989-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="02989-128">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="02989-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="02989-129">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="02989-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="02989-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="02989-130">-ComputeNode</span></span>
<span data-ttu-id="02989-131">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02989-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02989-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="02989-132">-DeallocationOption</span></span>
<span data-ttu-id="02989-133">Określa opcję lokalizacji transakcji dla operacji usuwania, która zostanie uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02989-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="02989-134">Wartość domyślna to Kolejkowanie ponowne.</span><span class="sxs-lookup"><span data-stu-id="02989-134">The default value is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02989-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02989-135">-DefaultProfile</span></span>
<span data-ttu-id="02989-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="02989-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02989-137">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="02989-137">-Force</span></span>
<span data-ttu-id="02989-138">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="02989-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02989-139">— Identyfikatory</span><span class="sxs-lookup"><span data-stu-id="02989-139">-Ids</span></span>
<span data-ttu-id="02989-140">Określa tablicę identyfikatorów węzłów obliczeniowych usuwanych przez to polecenie cmdlet z puli.</span><span class="sxs-lookup"><span data-stu-id="02989-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02989-141">- PoolId</span><span class="sxs-lookup"><span data-stu-id="02989-141">-PoolId</span></span>
<span data-ttu-id="02989-142">Określa identyfikator puli zawierającej węzły obliczeniowe, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02989-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02989-143">- ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="02989-143">-ResizeTimeout</span></span>
<span data-ttu-id="02989-144">Określa interwał dla usunięcia węzłów obliczeniowych z puli.</span><span class="sxs-lookup"><span data-stu-id="02989-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="02989-145">Wartość domyślna to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="02989-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="02989-146">Minimalna wartość to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="02989-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02989-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02989-147">-Confirm</span></span>
<span data-ttu-id="02989-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="02989-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02989-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02989-149">-WhatIf</span></span>
<span data-ttu-id="02989-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02989-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02989-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="02989-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02989-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02989-152">CommonParameters</span></span>
<span data-ttu-id="02989-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02989-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02989-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02989-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02989-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02989-155">INPUTS</span></span>

### <span data-ttu-id="02989-156">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="02989-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="02989-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="02989-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="02989-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02989-158">OUTPUTS</span></span>

### <span data-ttu-id="02989-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="02989-159">System.Void</span></span>

## <span data-ttu-id="02989-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="02989-160">NOTES</span></span>

## <span data-ttu-id="02989-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02989-161">RELATED LINKS</span></span>

[<span data-ttu-id="02989-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="02989-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="02989-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="02989-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="02989-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="02989-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


