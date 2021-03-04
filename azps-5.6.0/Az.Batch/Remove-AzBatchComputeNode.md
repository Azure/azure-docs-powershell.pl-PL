---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 7e2b2bca042573ec96fefdf85e5077ec1138d1da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956026"
---
# <span data-ttu-id="d9dc9-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9dc9-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="d9dc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="d9dc9-103">Usuwa węzły obliczeniowe z puli.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="d9dc9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9dc9-104">SYNTAX</span></span>

### <span data-ttu-id="d9dc9-105">Identyfikator (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d9dc9-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9dc9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d9dc9-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9dc9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9dc9-107">DESCRIPTION</span></span>
<span data-ttu-id="d9dc9-108">Polecenie **cmdlet Remove-AzBatchComputeNode** usuwa węzły obliczeniowe usługi Azure Batch z puli.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="d9dc9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9dc9-109">EXAMPLES</span></span>

### <span data-ttu-id="d9dc9-110">Przykład 1. Usuwanie węzła obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="d9dc9-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="d9dc9-111">To polecenie usuwa węzeł obliczeniowy o określonym identyfikatorze z puli, która ma pulę identyfikatorów 07.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="d9dc9-112">To polecenie określa opcję Zakończ alokację.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="d9dc9-113">Czas zmiany rozmiaru to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="d9dc9-114">Przykład 2. Usuwanie węzła obliczeniowego przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="d9dc9-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="d9dc9-115">To polecenie pobiera węzeł obliczeniowy, który ma określony identyfikator z puli, która ma identyfikator Pool07, przy użyciu Get-AzBatchComputeNode cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="d9dc9-116">Polecenie przekazuje ten węzeł do bieżącego polecenia cmdlet przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="d9dc9-117">Bieżące polecenie cmdlet usuwa węzeł obliczeniowy.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="d9dc9-118">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="d9dc9-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d9dc9-119">Dlatego to polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="d9dc9-120">Przykład 3. Usuwanie wielu węzłów</span><span class="sxs-lookup"><span data-stu-id="d9dc9-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="d9dc9-121">To polecenie usuwa dwa węzły obliczeniowe z puli, która ma pulę identyfikatorów 07.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="d9dc9-122">To polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d9dc9-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9dc9-123">PARAMETERS</span></span>

### <span data-ttu-id="d9dc9-124">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="d9dc9-124">-BatchContext</span></span>
<span data-ttu-id="d9dc9-125">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d9dc9-126">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d9dc9-127">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d9dc9-128">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d9dc9-129">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d9dc9-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9dc9-130">-ComputeNode</span></span>
<span data-ttu-id="d9dc9-131">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d9dc9-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="d9dc9-132">-DeallocationOption</span></span>
<span data-ttu-id="d9dc9-133">Określa opcję lokalizacji transakcji dla operacji usuwania, która zostanie uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="d9dc9-134">Wartość domyślna to Kolejkowanie ponowne.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="d9dc9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9dc9-135">-DefaultProfile</span></span>
<span data-ttu-id="d9dc9-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9dc9-137">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d9dc9-137">-Force</span></span>
<span data-ttu-id="d9dc9-138">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9dc9-139">— Identyfikatory</span><span class="sxs-lookup"><span data-stu-id="d9dc9-139">-Ids</span></span>
<span data-ttu-id="d9dc9-140">Określa tablicę identyfikatorów węzłów obliczeniowych usuwanych przez to polecenie cmdlet z puli.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="d9dc9-141">- PoolId</span><span class="sxs-lookup"><span data-stu-id="d9dc9-141">-PoolId</span></span>
<span data-ttu-id="d9dc9-142">Określa identyfikator puli zawierającej węzły obliczeniowe, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d9dc9-143">- ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="d9dc9-143">-ResizeTimeout</span></span>
<span data-ttu-id="d9dc9-144">Określa interwał dla usunięcia węzłów obliczeniowych z puli.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="d9dc9-145">Wartość domyślna to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="d9dc9-146">Minimalna wartość to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="d9dc9-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9dc9-147">-Confirm</span></span>
<span data-ttu-id="d9dc9-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9dc9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9dc9-149">-WhatIf</span></span>
<span data-ttu-id="d9dc9-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9dc9-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9dc9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9dc9-152">CommonParameters</span></span>
<span data-ttu-id="d9dc9-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9dc9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9dc9-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9dc9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9dc9-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9dc9-155">INPUTS</span></span>

### <span data-ttu-id="d9dc9-156">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9dc9-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d9dc9-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d9dc9-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d9dc9-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9dc9-158">OUTPUTS</span></span>

### <span data-ttu-id="d9dc9-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="d9dc9-159">System.Void</span></span>

## <span data-ttu-id="d9dc9-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9dc9-160">NOTES</span></span>

## <span data-ttu-id="d9dc9-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9dc9-161">RELATED LINKS</span></span>

[<span data-ttu-id="d9dc9-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d9dc9-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d9dc9-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9dc9-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d9dc9-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d9dc9-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


