---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 01e34258d7c3e94975032d0e77087b05acf3f264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963306"
---
# <span data-ttu-id="22513-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22513-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="22513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22513-102">SYNOPSIS</span></span>
<span data-ttu-id="22513-103">Włącza harmonogram zadań partii.</span><span class="sxs-lookup"><span data-stu-id="22513-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="22513-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22513-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22513-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="22513-105">DESCRIPTION</span></span>
<span data-ttu-id="22513-106">Polecenie **cmdlet Enable-AzBatchJobSchedule** umożliwia włączenie harmonogramu zadań partii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="22513-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="22513-107">Po włączeniu harmonogramu zadań można tworzyć zadania zgodnie z tym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="22513-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="22513-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22513-108">EXAMPLES</span></span>

### <span data-ttu-id="22513-109">Przykład 1. Włączanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="22513-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="22513-110">To polecenie umożliwia włączenie harmonogramu zadań z identyfikatorem Harmonogram zadań17.</span><span class="sxs-lookup"><span data-stu-id="22513-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="22513-111">Użyj polecenia **cmdlet Get-AzBatchAccountKey,** aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="22513-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="22513-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22513-112">PARAMETERS</span></span>

### <span data-ttu-id="22513-113">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="22513-113">-BatchContext</span></span>
<span data-ttu-id="22513-114">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="22513-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="22513-115">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22513-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="22513-116">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="22513-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="22513-117">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="22513-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="22513-118">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="22513-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="22513-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22513-119">-DefaultProfile</span></span>
<span data-ttu-id="22513-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="22513-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22513-121">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="22513-121">-Id</span></span>
<span data-ttu-id="22513-122">Określa identyfikator harmonogramu zadań włączane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22513-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="22513-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22513-123">CommonParameters</span></span>
<span data-ttu-id="22513-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22513-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22513-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22513-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22513-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22513-126">INPUTS</span></span>

### <span data-ttu-id="22513-127">System.String</span><span class="sxs-lookup"><span data-stu-id="22513-127">System.String</span></span>

### <span data-ttu-id="22513-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="22513-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="22513-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22513-129">OUTPUTS</span></span>

### <span data-ttu-id="22513-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="22513-130">System.Void</span></span>

## <span data-ttu-id="22513-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22513-131">NOTES</span></span>

## <span data-ttu-id="22513-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22513-132">RELATED LINKS</span></span>

[<span data-ttu-id="22513-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22513-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="22513-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="22513-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="22513-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22513-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="22513-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22513-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="22513-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22513-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="22513-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="22513-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="22513-139">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="22513-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
