---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: a42e6876336e409cca8df9e0fc72e65e8b6e1b3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552236"
---
# <span data-ttu-id="2b1b8-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="2b1b8-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="2b1b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1b8-103">Usuwa określoną pulę partii.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b1b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b1b8-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b1b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b1b8-105">DESCRIPTION</span></span>
<span data-ttu-id="2b1b8-106">Polecenie cmdlet **Remove-AzureBatchPool** usuwa określoną pulę usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="2b1b8-107">Zostanie wyświetlony monit o potwierdzenie, chyba że zostanie użyty parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="2b1b8-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="2b1b8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b1b8-108">EXAMPLES</span></span>

### <span data-ttu-id="2b1b8-109">Przykład 1: Usuwanie puli partii według identyfikatora puli</span><span class="sxs-lookup"><span data-stu-id="2b1b8-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="2b1b8-110">To polecenie usuwa pulę o IDENTYFIKATORze moja Pula.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="2b1b8-111">Użytkownik jest monitowany o potwierdzenie przed wykonaniem operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="2b1b8-112">Przykład 2: Usuwanie wszystkich pul partii według siły</span><span class="sxs-lookup"><span data-stu-id="2b1b8-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="2b1b8-113">To polecenie usuwa wszystkie pule partii.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="2b1b8-114">Ponieważ parametr *Force* jest obecny, monit o potwierdzenie jest pomijany.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="2b1b8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b1b8-115">PARAMETERS</span></span>

### <span data-ttu-id="2b1b8-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2b1b8-116">-BatchContext</span></span>
<span data-ttu-id="2b1b8-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2b1b8-118">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2b1b8-119">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2b1b8-120">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2b1b8-121">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1b8-122">-DefaultProfile</span></span>
<span data-ttu-id="2b1b8-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1b8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2b1b8-124">-Force</span></span>
<span data-ttu-id="2b1b8-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1b8-126">-ID</span><span class="sxs-lookup"><span data-stu-id="2b1b8-126">-Id</span></span>
<span data-ttu-id="2b1b8-127">Określa identyfikator puli, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="2b1b8-128">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b1b8-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b1b8-129">-Confirm</span></span>
<span data-ttu-id="2b1b8-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1b8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b1b8-131">-WhatIf</span></span>
<span data-ttu-id="2b1b8-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b1b8-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1b8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1b8-134">CommonParameters</span></span>
<span data-ttu-id="2b1b8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b1b8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1b8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b1b8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1b8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b1b8-137">INPUTS</span></span>

### <span data-ttu-id="2b1b8-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2b1b8-138">BatchAccountContext</span></span>
<span data-ttu-id="2b1b8-139">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="2b1b8-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="2b1b8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b1b8-140">OUTPUTS</span></span>

## <span data-ttu-id="2b1b8-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b1b8-141">NOTES</span></span>

## <span data-ttu-id="2b1b8-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b1b8-142">RELATED LINKS</span></span>

[<span data-ttu-id="2b1b8-143">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2b1b8-143">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2b1b8-144">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="2b1b8-144">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="2b1b8-145">Nowe — AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="2b1b8-145">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="2b1b8-146">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="2b1b8-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


