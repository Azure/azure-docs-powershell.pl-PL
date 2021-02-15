---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197003"
---
# <span data-ttu-id="00b85-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="00b85-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="00b85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00b85-102">SYNOPSIS</span></span>
<span data-ttu-id="00b85-103">Usuwa konto użytkownika z węzła obliczeniowego Batch.</span><span class="sxs-lookup"><span data-stu-id="00b85-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="00b85-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="00b85-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00b85-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="00b85-105">DESCRIPTION</span></span>
<span data-ttu-id="00b85-106">Polecenie **cmdlet Remove-AzBatchComputeNodeUser** usuwa konto użytkownika z węzła obliczeniowego usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="00b85-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="00b85-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="00b85-107">EXAMPLES</span></span>

### <span data-ttu-id="00b85-108">Przykład 1. Usuwanie użytkownika z węzła obliczeniowego bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="00b85-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="00b85-109">To polecenie usuwa użytkownika o nazwie Użytkownik14 z węzła obliczeniowego o nazwie ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="00b85-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="00b85-110">Węzeł obliczeniowy znajduje się w puli o nazwie Pula01.</span><span class="sxs-lookup"><span data-stu-id="00b85-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="00b85-111">To polecenie określa *parametr Force.*</span><span class="sxs-lookup"><span data-stu-id="00b85-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="00b85-112">Dlatego to polecenie nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00b85-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="00b85-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00b85-113">PARAMETERS</span></span>

### <span data-ttu-id="00b85-114">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="00b85-114">-BatchContext</span></span>
<span data-ttu-id="00b85-115">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="00b85-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="00b85-116">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00b85-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="00b85-117">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="00b85-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="00b85-118">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="00b85-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="00b85-119">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="00b85-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="00b85-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="00b85-120">-ComputeNodeId</span></span>
<span data-ttu-id="00b85-121">Określa identyfikator węzła obliczeniowego, z którego to polecenie cmdlet usuwa konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00b85-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b85-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b85-122">-DefaultProfile</span></span>
<span data-ttu-id="00b85-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="00b85-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00b85-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="00b85-124">-Name</span></span>
<span data-ttu-id="00b85-125">Określa nazwę konta użytkownika do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="00b85-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="00b85-126">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="00b85-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00b85-127">- PoolId</span><span class="sxs-lookup"><span data-stu-id="00b85-127">-PoolId</span></span>
<span data-ttu-id="00b85-128">Określa identyfikator puli zawierającej węzeł obliczeniowy, z którego ma być usunięte konto użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00b85-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="00b85-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00b85-129">-Confirm</span></span>
<span data-ttu-id="00b85-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00b85-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00b85-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00b85-131">-WhatIf</span></span>
<span data-ttu-id="00b85-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00b85-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00b85-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="00b85-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00b85-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b85-134">CommonParameters</span></span>
<span data-ttu-id="00b85-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00b85-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b85-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00b85-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b85-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00b85-137">INPUTS</span></span>

### <span data-ttu-id="00b85-138">System.String</span><span class="sxs-lookup"><span data-stu-id="00b85-138">System.String</span></span>

### <span data-ttu-id="00b85-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="00b85-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="00b85-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00b85-140">OUTPUTS</span></span>

### <span data-ttu-id="00b85-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="00b85-141">System.Void</span></span>

## <span data-ttu-id="00b85-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="00b85-142">NOTES</span></span>

## <span data-ttu-id="00b85-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00b85-143">RELATED LINKS</span></span>

[<span data-ttu-id="00b85-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="00b85-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="00b85-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="00b85-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="00b85-146">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="00b85-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
