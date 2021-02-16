---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199530"
---
# <span data-ttu-id="8b790-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8b790-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="8b790-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b790-102">SYNOPSIS</span></span>
<span data-ttu-id="8b790-103">Usuwa określoną pulę partii.</span><span class="sxs-lookup"><span data-stu-id="8b790-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="8b790-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b790-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b790-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b790-105">DESCRIPTION</span></span>
<span data-ttu-id="8b790-106">Polecenie **cmdlet Remove-AzBatchPool** usuwa określoną pulę partii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8b790-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="8b790-107">Zostanie wyświetlony monit o potwierdzenie, chyba że używasz *parametru Force.*</span><span class="sxs-lookup"><span data-stu-id="8b790-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="8b790-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b790-108">EXAMPLES</span></span>

### <span data-ttu-id="8b790-109">Przykład 1. Usuwanie puli partii według identyfikatora puli</span><span class="sxs-lookup"><span data-stu-id="8b790-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="8b790-110">To polecenie usuwa pulę o identyfikatorze MyPool.</span><span class="sxs-lookup"><span data-stu-id="8b790-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="8b790-111">Przed rozpoczęciem operacji usuwania użytkownik jest monitowany o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8b790-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="8b790-112">Przykład 2. Usuwanie wszystkich pul partii według wymuszania</span><span class="sxs-lookup"><span data-stu-id="8b790-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="8b790-113">To polecenie usuwa wszystkie pule wsadowe.</span><span class="sxs-lookup"><span data-stu-id="8b790-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="8b790-114">Parametr *Force jest* wyświetlany, dlatego monit o potwierdzenie jest pomijany.</span><span class="sxs-lookup"><span data-stu-id="8b790-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="8b790-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b790-115">PARAMETERS</span></span>

### <span data-ttu-id="8b790-116">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="8b790-116">-BatchContext</span></span>
<span data-ttu-id="8b790-117">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="8b790-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8b790-118">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8b790-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8b790-119">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="8b790-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8b790-120">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="8b790-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8b790-121">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8b790-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8b790-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b790-122">-DefaultProfile</span></span>
<span data-ttu-id="8b790-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b790-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b790-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8b790-124">-Force</span></span>
<span data-ttu-id="8b790-125">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8b790-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b790-126">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="8b790-126">-Id</span></span>
<span data-ttu-id="8b790-127">Określa identyfikator puli do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8b790-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="8b790-128">Nie można określić symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="8b790-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="8b790-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b790-129">-Confirm</span></span>
<span data-ttu-id="8b790-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8b790-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b790-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b790-131">-WhatIf</span></span>
<span data-ttu-id="8b790-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b790-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b790-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8b790-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b790-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b790-134">CommonParameters</span></span>
<span data-ttu-id="8b790-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b790-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b790-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b790-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b790-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b790-137">INPUTS</span></span>

### <span data-ttu-id="8b790-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8b790-138">System.String</span></span>

### <span data-ttu-id="8b790-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8b790-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8b790-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b790-140">OUTPUTS</span></span>

### <span data-ttu-id="8b790-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="8b790-141">System.Void</span></span>

## <span data-ttu-id="8b790-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b790-142">NOTES</span></span>

## <span data-ttu-id="8b790-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b790-143">RELATED LINKS</span></span>

[<span data-ttu-id="8b790-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8b790-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8b790-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8b790-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="8b790-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="8b790-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="8b790-147">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="8b790-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
