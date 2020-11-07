---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 59a906420e2326564e779c9358e07a5003946b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716788"
---
# <span data-ttu-id="45095-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45095-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="45095-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45095-102">SYNOPSIS</span></span>
<span data-ttu-id="45095-103">Usuwa harmonogram zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="45095-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45095-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45095-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45095-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45095-105">DESCRIPTION</span></span>
<span data-ttu-id="45095-106">Polecenie cmdlet **Remove-AzureBatchJobSchedule** usuwa harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="45095-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="45095-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45095-107">EXAMPLES</span></span>

## <span data-ttu-id="45095-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45095-108">PARAMETERS</span></span>

### <span data-ttu-id="45095-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="45095-109">-BatchContext</span></span>
<span data-ttu-id="45095-110">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="45095-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="45095-111">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="45095-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="45095-112">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="45095-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="45095-113">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="45095-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="45095-114">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="45095-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="45095-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45095-115">-DefaultProfile</span></span>
<span data-ttu-id="45095-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45095-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45095-117">-Force</span><span class="sxs-lookup"><span data-stu-id="45095-117">-Force</span></span>
<span data-ttu-id="45095-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="45095-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45095-119">-ID</span><span class="sxs-lookup"><span data-stu-id="45095-119">-Id</span></span>
<span data-ttu-id="45095-120">Określa identyfikator harmonogramu zadań, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="45095-120">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="45095-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45095-121">-Confirm</span></span>
<span data-ttu-id="45095-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45095-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45095-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45095-123">-WhatIf</span></span>
<span data-ttu-id="45095-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45095-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45095-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45095-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45095-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45095-126">CommonParameters</span></span>
<span data-ttu-id="45095-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45095-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45095-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45095-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45095-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45095-129">INPUTS</span></span>

### <span data-ttu-id="45095-130">System. String</span><span class="sxs-lookup"><span data-stu-id="45095-130">System.String</span></span>

### <span data-ttu-id="45095-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="45095-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="45095-132">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="45095-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="45095-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45095-133">OUTPUTS</span></span>

### <span data-ttu-id="45095-134">System. void</span><span class="sxs-lookup"><span data-stu-id="45095-134">System.Void</span></span>

## <span data-ttu-id="45095-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45095-135">NOTES</span></span>

## <span data-ttu-id="45095-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45095-136">RELATED LINKS</span></span>

[<span data-ttu-id="45095-137">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45095-137">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="45095-138">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45095-138">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="45095-139">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45095-139">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="45095-140">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45095-140">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="45095-141">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45095-141">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="45095-142">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="45095-142">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


