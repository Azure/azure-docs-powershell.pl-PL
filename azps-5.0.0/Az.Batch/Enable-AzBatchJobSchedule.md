---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225234"
---
# <span data-ttu-id="24346-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="24346-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="24346-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24346-102">SYNOPSIS</span></span>
<span data-ttu-id="24346-103">Umożliwia planowanie zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="24346-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="24346-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24346-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24346-105">Opis</span><span class="sxs-lookup"><span data-stu-id="24346-105">DESCRIPTION</span></span>
<span data-ttu-id="24346-106">Polecenie cmdlet **enable-AzBatchJobSchedule** włącza harmonogram zadania usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="24346-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="24346-107">Po włączeniu harmonogramu zadań można utworzyć zadania według harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="24346-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="24346-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24346-108">EXAMPLES</span></span>

### <span data-ttu-id="24346-109">Przykład 1. Włączanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="24346-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="24346-110">To polecenie włącza harmonogram zadań o IDENTYFIKATORze JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="24346-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="24346-111">Użyj polecenia cmdlet **Get-AzBatchAccountKey** w celu przypisania kontekstu do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="24346-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="24346-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24346-112">PARAMETERS</span></span>

### <span data-ttu-id="24346-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="24346-113">-BatchContext</span></span>
<span data-ttu-id="24346-114">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="24346-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="24346-115">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="24346-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="24346-116">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="24346-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="24346-117">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="24346-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="24346-118">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="24346-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="24346-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24346-119">-DefaultProfile</span></span>
<span data-ttu-id="24346-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24346-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24346-121">-ID</span><span class="sxs-lookup"><span data-stu-id="24346-121">-Id</span></span>
<span data-ttu-id="24346-122">Określa identyfikator harmonogramu zadań, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24346-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="24346-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24346-123">CommonParameters</span></span>
<span data-ttu-id="24346-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24346-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24346-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24346-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24346-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24346-126">INPUTS</span></span>

### <span data-ttu-id="24346-127">System. String</span><span class="sxs-lookup"><span data-stu-id="24346-127">System.String</span></span>

### <span data-ttu-id="24346-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="24346-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="24346-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24346-129">OUTPUTS</span></span>

### <span data-ttu-id="24346-130">System. void</span><span class="sxs-lookup"><span data-stu-id="24346-130">System.Void</span></span>

## <span data-ttu-id="24346-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24346-131">NOTES</span></span>

## <span data-ttu-id="24346-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24346-132">RELATED LINKS</span></span>

[<span data-ttu-id="24346-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="24346-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="24346-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="24346-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="24346-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="24346-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="24346-136">Nowe — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="24346-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="24346-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="24346-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="24346-138">Zatrzymaj — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="24346-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="24346-139">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="24346-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
