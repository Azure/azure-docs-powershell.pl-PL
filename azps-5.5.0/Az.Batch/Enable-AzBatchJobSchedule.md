---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 03decd5b1d32defb25692220c63ffe768445697e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239427"
---
# <span data-ttu-id="a2c59-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a2c59-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="a2c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c59-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c59-103">Włącza harmonogram zadań partii.</span><span class="sxs-lookup"><span data-stu-id="a2c59-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="a2c59-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a2c59-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2c59-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a2c59-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c59-106">Polecenie **cmdlet Enable-AzBatchJobSchedule** umożliwia włączenie harmonogramu zadań partii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c59-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="a2c59-107">Po włączeniu harmonogramu zadań można tworzyć zadania zgodnie z tym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="a2c59-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="a2c59-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a2c59-108">EXAMPLES</span></span>

### <span data-ttu-id="a2c59-109">Przykład 1. Włączanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="a2c59-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="a2c59-110">To polecenie umożliwia włączenie harmonogramu zadań z identyfikatorem Harmonogram zadań17.</span><span class="sxs-lookup"><span data-stu-id="a2c59-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="a2c59-111">Użyj polecenia **cmdlet Get-AzBatchAccountKey,** aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="a2c59-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="a2c59-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2c59-112">PARAMETERS</span></span>

### <span data-ttu-id="a2c59-113">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="a2c59-113">-BatchContext</span></span>
<span data-ttu-id="a2c59-114">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="a2c59-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a2c59-115">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2c59-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a2c59-116">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="a2c59-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a2c59-117">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="a2c59-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a2c59-118">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a2c59-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a2c59-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c59-119">-DefaultProfile</span></span>
<span data-ttu-id="a2c59-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c59-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c59-121">— Id</span><span class="sxs-lookup"><span data-stu-id="a2c59-121">-Id</span></span>
<span data-ttu-id="a2c59-122">Określa identyfikator harmonogramu zadań włączane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2c59-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="a2c59-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c59-123">CommonParameters</span></span>
<span data-ttu-id="a2c59-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c59-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c59-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2c59-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c59-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2c59-126">INPUTS</span></span>

### <span data-ttu-id="a2c59-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a2c59-127">System.String</span></span>

### <span data-ttu-id="a2c59-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a2c59-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a2c59-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2c59-129">OUTPUTS</span></span>

### <span data-ttu-id="a2c59-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="a2c59-130">System.Void</span></span>

## <span data-ttu-id="a2c59-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a2c59-131">NOTES</span></span>

## <span data-ttu-id="a2c59-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2c59-132">RELATED LINKS</span></span>

[<span data-ttu-id="a2c59-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a2c59-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="a2c59-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a2c59-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a2c59-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a2c59-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="a2c59-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a2c59-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="a2c59-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a2c59-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="a2c59-138">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a2c59-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="a2c59-139">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a2c59-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
