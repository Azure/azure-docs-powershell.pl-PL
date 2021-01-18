---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502128"
---
# <span data-ttu-id="8e1e6-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e1e6-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="8e1e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1e6-103">Usuwa węzły obliczeniowe z puli.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="8e1e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e1e6-104">SYNTAX</span></span>

### <span data-ttu-id="8e1e6-105">Identyfikator (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8e1e6-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e1e6-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e1e6-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e1e6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8e1e6-107">DESCRIPTION</span></span>
<span data-ttu-id="8e1e6-108">Polecenie cmdlet **Remove-AzBatchComputeNode** usuwa węzły obliczeniowe usługi Azure Batch z puli.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="8e1e6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e1e6-109">EXAMPLES</span></span>

### <span data-ttu-id="8e1e6-110">Przykład 1. Usuń węzeł obliczeniowy</span><span class="sxs-lookup"><span data-stu-id="8e1e6-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="8e1e6-111">To polecenie usuwa węzeł obliczeniowy o określonym IDENTYFIKATORze z puli o IDENTYFIKATORze Pool07.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="8e1e6-112">Polecenie określa opcję zakończenia dealokacji.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="8e1e6-113">Limit czasu zmiany rozmiaru wynosi 10 minut.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="8e1e6-114">Przykład 2: Usuwanie węzła obliczeniowego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="8e1e6-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="8e1e6-115">To polecenie uzyskuje węzeł obliczeniowy z pulą o określonym IDENTYFIKATORze, który ma identyfikator Pool07, przy użyciu polecenia cmdlet Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="8e1e6-116">Polecenie przekazuje ten węzeł do bieżącego polecenia cmdlet za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="8e1e6-117">Bieżące polecenie cmdlet powoduje usunięcie węzła obliczeniowego.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="8e1e6-118">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="8e1e6-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8e1e6-119">Dlatego polecenie nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8e1e6-120">Przykład 3: usuwanie wielu węzłów</span><span class="sxs-lookup"><span data-stu-id="8e1e6-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="8e1e6-121">To polecenie powoduje usunięcie dwóch węzłów obliczeniowych z puli o IDENTYFIKATORze Pool07.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="8e1e6-122">Polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8e1e6-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e1e6-123">PARAMETERS</span></span>

### <span data-ttu-id="8e1e6-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8e1e6-124">-BatchContext</span></span>
<span data-ttu-id="8e1e6-125">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8e1e6-126">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8e1e6-127">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8e1e6-128">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8e1e6-129">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8e1e6-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e1e6-130">-ComputeNode</span></span>
<span data-ttu-id="8e1e6-131">Określa obiekt **PSComputeNode** reprezentujący węzeł obliczeniowy, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8e1e6-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="8e1e6-132">-DeallocationOption</span></span>
<span data-ttu-id="8e1e6-133">Określa opcję cofnięcia przydziału dla operacji usuwania, która zostanie uruchomiona przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="8e1e6-134">Wartość domyślna to requeue.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="8e1e6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1e6-135">-DefaultProfile</span></span>
<span data-ttu-id="8e1e6-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e1e6-137">-Force</span><span class="sxs-lookup"><span data-stu-id="8e1e6-137">-Force</span></span>
<span data-ttu-id="8e1e6-138">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e1e6-139">-IDS</span><span class="sxs-lookup"><span data-stu-id="8e1e6-139">-Ids</span></span>
<span data-ttu-id="8e1e6-140">Określa tablicę identyfikatorów węzłów obliczeniowych, które polecenie cmdlet usuwa z puli.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="8e1e6-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="8e1e6-141">-PoolId</span></span>
<span data-ttu-id="8e1e6-142">Określa identyfikator puli zawierającej węzły obliczeniowe, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8e1e6-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="8e1e6-143">-ResizeTimeout</span></span>
<span data-ttu-id="8e1e6-144">Określa interwał limitu czasu dla usuwania węzłów obliczeniowych z puli.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="8e1e6-145">Wartość domyślna to 10 minut.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="8e1e6-146">Minimalna wartość to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="8e1e6-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e1e6-147">-Confirm</span></span>
<span data-ttu-id="8e1e6-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e1e6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e1e6-149">-WhatIf</span></span>
<span data-ttu-id="8e1e6-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e1e6-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e1e6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1e6-152">CommonParameters</span></span>
<span data-ttu-id="8e1e6-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e1e6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1e6-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e1e6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1e6-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e1e6-155">INPUTS</span></span>

### <span data-ttu-id="8e1e6-156">Microsoft.Azure.Commands.Batch. Modele. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e1e6-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="8e1e6-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8e1e6-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8e1e6-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e1e6-158">OUTPUTS</span></span>

### <span data-ttu-id="8e1e6-159">System. void</span><span class="sxs-lookup"><span data-stu-id="8e1e6-159">System.Void</span></span>

## <span data-ttu-id="8e1e6-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e1e6-160">NOTES</span></span>

## <span data-ttu-id="8e1e6-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e1e6-161">RELATED LINKS</span></span>

[<span data-ttu-id="8e1e6-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8e1e6-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8e1e6-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e1e6-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="8e1e6-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e1e6-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


