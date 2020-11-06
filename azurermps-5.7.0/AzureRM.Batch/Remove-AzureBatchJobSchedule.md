---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544552"
---
# <span data-ttu-id="5f3bc-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5f3bc-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="5f3bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="5f3bc-103">Usuwa harmonogram zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f3bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f3bc-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f3bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f3bc-105">DESCRIPTION</span></span>
<span data-ttu-id="5f3bc-106">Polecenie cmdlet **Remove-AzureBatchJobSchedule** usuwa harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="5f3bc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f3bc-107">EXAMPLES</span></span>

## <span data-ttu-id="5f3bc-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f3bc-108">PARAMETERS</span></span>

### <span data-ttu-id="5f3bc-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5f3bc-109">-BatchContext</span></span>
<span data-ttu-id="5f3bc-110">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5f3bc-111">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5f3bc-112">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5f3bc-113">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5f3bc-114">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5f3bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f3bc-115">-DefaultProfile</span></span>
<span data-ttu-id="5f3bc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f3bc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5f3bc-117">-Force</span></span>
<span data-ttu-id="5f3bc-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5f3bc-119">-ID</span><span class="sxs-lookup"><span data-stu-id="5f3bc-119">-Id</span></span>
<span data-ttu-id="5f3bc-120">Określa identyfikator harmonogramu zadań, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-120">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="5f3bc-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f3bc-121">-Confirm</span></span>
<span data-ttu-id="5f3bc-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f3bc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f3bc-123">-WhatIf</span></span>
<span data-ttu-id="5f3bc-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f3bc-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f3bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f3bc-126">CommonParameters</span></span>
<span data-ttu-id="5f3bc-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f3bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f3bc-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f3bc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f3bc-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f3bc-129">INPUTS</span></span>

### <span data-ttu-id="5f3bc-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5f3bc-130">BatchAccountContext</span></span>
<span data-ttu-id="5f3bc-131">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="5f3bc-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="5f3bc-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f3bc-132">OUTPUTS</span></span>

## <span data-ttu-id="5f3bc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f3bc-133">NOTES</span></span>

## <span data-ttu-id="5f3bc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f3bc-134">RELATED LINKS</span></span>

[<span data-ttu-id="5f3bc-135">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5f3bc-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="5f3bc-136">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5f3bc-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="5f3bc-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5f3bc-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="5f3bc-138">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5f3bc-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="5f3bc-139">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5f3bc-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="5f3bc-140">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5f3bc-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


