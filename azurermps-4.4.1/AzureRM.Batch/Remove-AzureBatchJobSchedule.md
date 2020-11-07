---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 673d9e5034b1e7c97d3b6b7cfdd6f89e9a79a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717240"
---
# <span data-ttu-id="f7310-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7310-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="f7310-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7310-102">SYNOPSIS</span></span>
<span data-ttu-id="f7310-103">Usuwa harmonogram zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f7310-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7310-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7310-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7310-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7310-105">DESCRIPTION</span></span>
<span data-ttu-id="f7310-106">Polecenie cmdlet **Remove-AzureBatchJobSchedule** usuwa harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="f7310-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="f7310-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7310-107">EXAMPLES</span></span>

## <span data-ttu-id="f7310-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7310-108">PARAMETERS</span></span>

### <span data-ttu-id="f7310-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f7310-109">-BatchContext</span></span>
<span data-ttu-id="f7310-110">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f7310-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f7310-111">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f7310-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f7310-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f7310-112">-Force</span></span>
<span data-ttu-id="f7310-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f7310-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f7310-114">-ID</span><span class="sxs-lookup"><span data-stu-id="f7310-114">-Id</span></span>
<span data-ttu-id="f7310-115">Określa identyfikator harmonogramu zadań, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f7310-115">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="f7310-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7310-116">-Confirm</span></span>
<span data-ttu-id="f7310-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7310-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7310-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7310-118">-WhatIf</span></span>
<span data-ttu-id="f7310-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7310-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7310-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7310-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7310-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7310-121">-DefaultProfile</span></span>
<span data-ttu-id="f7310-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7310-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7310-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7310-123">CommonParameters</span></span>
<span data-ttu-id="f7310-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7310-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7310-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7310-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7310-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7310-126">INPUTS</span></span>

### <span data-ttu-id="f7310-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f7310-127">BatchAccountContext</span></span>
<span data-ttu-id="f7310-128">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="f7310-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="f7310-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7310-129">OUTPUTS</span></span>

## <span data-ttu-id="f7310-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7310-130">NOTES</span></span>

## <span data-ttu-id="f7310-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7310-131">RELATED LINKS</span></span>

[<span data-ttu-id="f7310-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7310-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f7310-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7310-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="f7310-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7310-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="f7310-135">Nowe — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7310-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="f7310-136">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7310-136">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="f7310-137">Zatrzymaj — AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f7310-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


