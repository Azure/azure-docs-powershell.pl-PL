---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 1470f02570462a3a7bb922c88504e3c8a20eb8fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971562"
---
# <span data-ttu-id="e523b-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e523b-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="e523b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e523b-102">SYNOPSIS</span></span>
<span data-ttu-id="e523b-103">Włącza zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="e523b-103">Enables a Batch job.</span></span>

## <span data-ttu-id="e523b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e523b-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e523b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e523b-105">DESCRIPTION</span></span>
<span data-ttu-id="e523b-106">Polecenie **cmdlet Enable-AzBatchJob** włącza zadanie partii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e523b-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="e523b-107">Po włączeniu zadania można uruchamiać nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="e523b-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="e523b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e523b-108">EXAMPLES</span></span>

### <span data-ttu-id="e523b-109">Przykład 1. Włączanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="e523b-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="e523b-110">To polecenie umożliwia włączenie zadania o identyfikatorze Zadanie-000001.</span><span class="sxs-lookup"><span data-stu-id="e523b-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="e523b-111">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="e523b-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e523b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e523b-112">PARAMETERS</span></span>

### <span data-ttu-id="e523b-113">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="e523b-113">-BatchContext</span></span>
<span data-ttu-id="e523b-114">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="e523b-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e523b-115">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e523b-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e523b-116">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="e523b-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e523b-117">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="e523b-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e523b-118">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e523b-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e523b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e523b-119">-DefaultProfile</span></span>
<span data-ttu-id="e523b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e523b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e523b-121">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="e523b-121">-Id</span></span>
<span data-ttu-id="e523b-122">Określa identyfikator zadania, które włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e523b-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="e523b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e523b-123">CommonParameters</span></span>
<span data-ttu-id="e523b-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e523b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e523b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e523b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e523b-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e523b-126">INPUTS</span></span>

### <span data-ttu-id="e523b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e523b-127">System.String</span></span>

### <span data-ttu-id="e523b-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e523b-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e523b-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e523b-129">OUTPUTS</span></span>

### <span data-ttu-id="e523b-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="e523b-130">System.Void</span></span>

## <span data-ttu-id="e523b-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e523b-131">NOTES</span></span>

## <span data-ttu-id="e523b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e523b-132">RELATED LINKS</span></span>

[<span data-ttu-id="e523b-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e523b-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="e523b-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e523b-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="e523b-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e523b-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="e523b-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e523b-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="e523b-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="e523b-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="e523b-138">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e523b-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
