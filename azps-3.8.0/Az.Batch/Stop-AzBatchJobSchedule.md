---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 9536de21d205a051f0a0a2ea6f4a83c759b94c8c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061703"
---
# <span data-ttu-id="5690b-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5690b-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="5690b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5690b-102">SYNOPSIS</span></span>
<span data-ttu-id="5690b-103">Zatrzymuje harmonogram zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="5690b-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="5690b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5690b-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5690b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5690b-105">DESCRIPTION</span></span>
<span data-ttu-id="5690b-106">Polecenie cmdlet **stop-AzBatchJobSchedule** zatrzymuje harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="5690b-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="5690b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5690b-107">EXAMPLES</span></span>

### <span data-ttu-id="5690b-108">Przykład 1: zatrzymywanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="5690b-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="5690b-109">To polecenie zatrzymuje harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="5690b-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="5690b-110">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="5690b-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5690b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5690b-111">PARAMETERS</span></span>

### <span data-ttu-id="5690b-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5690b-112">-BatchContext</span></span>
<span data-ttu-id="5690b-113">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5690b-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5690b-114">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5690b-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5690b-115">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="5690b-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5690b-116">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="5690b-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5690b-117">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5690b-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5690b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5690b-118">-DefaultProfile</span></span>
<span data-ttu-id="5690b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5690b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5690b-120">-ID</span><span class="sxs-lookup"><span data-stu-id="5690b-120">-Id</span></span>
<span data-ttu-id="5690b-121">Określa identyfikator harmonogramu zadań, który zostanie zatrzymany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5690b-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5690b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5690b-122">CommonParameters</span></span>
<span data-ttu-id="5690b-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5690b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5690b-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5690b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5690b-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5690b-125">INPUTS</span></span>

### <span data-ttu-id="5690b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5690b-126">System.String</span></span>

### <span data-ttu-id="5690b-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5690b-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5690b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5690b-128">OUTPUTS</span></span>

### <span data-ttu-id="5690b-129">System. void</span><span class="sxs-lookup"><span data-stu-id="5690b-129">System.Void</span></span>

## <span data-ttu-id="5690b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5690b-130">NOTES</span></span>

## <span data-ttu-id="5690b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5690b-131">RELATED LINKS</span></span>

[<span data-ttu-id="5690b-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5690b-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="5690b-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5690b-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="5690b-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5690b-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5690b-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5690b-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="5690b-136">Nowe — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5690b-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="5690b-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="5690b-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="5690b-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="5690b-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


