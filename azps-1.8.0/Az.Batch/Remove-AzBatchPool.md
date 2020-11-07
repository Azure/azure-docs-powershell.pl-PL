---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: be9b7d5ed8f5f26e31c04f96e14d14573fd0a0f0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710801"
---
# <span data-ttu-id="e1e7f-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e1e7f-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="e1e7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e7f-103">Usuwa określoną pulę partii.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="e1e7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1e7f-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1e7f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1e7f-105">DESCRIPTION</span></span>
<span data-ttu-id="e1e7f-106">Polecenie cmdlet **Remove-AzBatchPool** usuwa określoną pulę usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="e1e7f-107">Zostanie wyświetlony monit o potwierdzenie, chyba że zostanie użyty parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="e1e7f-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="e1e7f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1e7f-108">EXAMPLES</span></span>

### <span data-ttu-id="e1e7f-109">Przykład 1: Usuwanie puli partii według identyfikatora puli</span><span class="sxs-lookup"><span data-stu-id="e1e7f-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="e1e7f-110">To polecenie usuwa pulę o IDENTYFIKATORze moja Pula.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="e1e7f-111">Użytkownik jest monitowany o potwierdzenie przed wykonaniem operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="e1e7f-112">Przykład 2: Usuwanie wszystkich pul partii według siły</span><span class="sxs-lookup"><span data-stu-id="e1e7f-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="e1e7f-113">To polecenie usuwa wszystkie pule partii.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="e1e7f-114">Ponieważ parametr *Force* jest obecny, monit o potwierdzenie jest pomijany.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="e1e7f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1e7f-115">PARAMETERS</span></span>

### <span data-ttu-id="e1e7f-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e1e7f-116">-BatchContext</span></span>
<span data-ttu-id="e1e7f-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e1e7f-118">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e1e7f-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e1e7f-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e1e7f-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e1e7f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e7f-122">-DefaultProfile</span></span>
<span data-ttu-id="e1e7f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1e7f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e1e7f-124">-Force</span></span>
<span data-ttu-id="e1e7f-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1e7f-126">-ID</span><span class="sxs-lookup"><span data-stu-id="e1e7f-126">-Id</span></span>
<span data-ttu-id="e1e7f-127">Określa identyfikator puli, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="e1e7f-128">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="e1e7f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1e7f-129">-Confirm</span></span>
<span data-ttu-id="e1e7f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1e7f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1e7f-131">-WhatIf</span></span>
<span data-ttu-id="e1e7f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1e7f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1e7f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e7f-134">CommonParameters</span></span>
<span data-ttu-id="e1e7f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e7f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e7f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1e7f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e7f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1e7f-137">INPUTS</span></span>

### <span data-ttu-id="e1e7f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e1e7f-138">System.String</span></span>

### <span data-ttu-id="e1e7f-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e1e7f-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e1e7f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1e7f-140">OUTPUTS</span></span>

### <span data-ttu-id="e1e7f-141">System. void</span><span class="sxs-lookup"><span data-stu-id="e1e7f-141">System.Void</span></span>

## <span data-ttu-id="e1e7f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1e7f-142">NOTES</span></span>

## <span data-ttu-id="e1e7f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1e7f-143">RELATED LINKS</span></span>

[<span data-ttu-id="e1e7f-144">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e1e7f-144">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e1e7f-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e1e7f-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="e1e7f-146">Nowe — AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e1e7f-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="e1e7f-147">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e1e7f-147">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


