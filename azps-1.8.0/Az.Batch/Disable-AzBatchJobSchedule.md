---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 59afa8f2ad5b1cf8739bece249d63574c8db6e4c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710875"
---
# <span data-ttu-id="d4ddb-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d4ddb-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="d4ddb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ddb-103">Wyłącza harmonogram zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="d4ddb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4ddb-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4ddb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d4ddb-105">DESCRIPTION</span></span>
<span data-ttu-id="d4ddb-106">Polecenie cmdlet **disable-AzBatchJobSchedule** wyłącza harmonogram zadań usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="d4ddb-107">W przypadku wyłączenia harmonogramu zadania nie są tworzone zgodnie z tym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="d4ddb-108">Możesz włączyć wyłączony harmonogram później.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="d4ddb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4ddb-109">EXAMPLES</span></span>

### <span data-ttu-id="d4ddb-110">Przykład 1: wyłączanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="d4ddb-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="d4ddb-111">To polecenie wyłącza harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="d4ddb-112">Użyj polecenia cmdlet **Get-AzBatchAccountKeys** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-112">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d4ddb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4ddb-113">PARAMETERS</span></span>

### <span data-ttu-id="d4ddb-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d4ddb-114">-BatchContext</span></span>
<span data-ttu-id="d4ddb-115">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d4ddb-116">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d4ddb-117">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d4ddb-118">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d4ddb-119">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d4ddb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ddb-120">-DefaultProfile</span></span>
<span data-ttu-id="d4ddb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4ddb-122">-ID</span><span class="sxs-lookup"><span data-stu-id="d4ddb-122">-Id</span></span>
<span data-ttu-id="d4ddb-123">Określa identyfikator harmonogramu zadań, który ma zostać wyłączony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="d4ddb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ddb-124">CommonParameters</span></span>
<span data-ttu-id="d4ddb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4ddb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ddb-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4ddb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ddb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4ddb-127">INPUTS</span></span>

### <span data-ttu-id="d4ddb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d4ddb-128">System.String</span></span>

### <span data-ttu-id="d4ddb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d4ddb-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d4ddb-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4ddb-130">OUTPUTS</span></span>

### <span data-ttu-id="d4ddb-131">System. void</span><span class="sxs-lookup"><span data-stu-id="d4ddb-131">System.Void</span></span>

## <span data-ttu-id="d4ddb-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4ddb-132">NOTES</span></span>

## <span data-ttu-id="d4ddb-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4ddb-133">RELATED LINKS</span></span>

[<span data-ttu-id="d4ddb-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d4ddb-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="d4ddb-135">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d4ddb-135">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d4ddb-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d4ddb-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="d4ddb-137">Nowe — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d4ddb-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="d4ddb-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d4ddb-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="d4ddb-139">Zatrzymaj — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d4ddb-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="d4ddb-140">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d4ddb-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


