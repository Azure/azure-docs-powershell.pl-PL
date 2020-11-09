---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 975B707C-5001-43ED-81AB-9BB6665135BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJob.md
ms.openlocfilehash: ffaac0bdd4a144cc3979da052c0c40cb824862f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317299"
---
# <span data-ttu-id="610fc-101">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="610fc-101">Stop-AzBatchJob</span></span>

## <span data-ttu-id="610fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="610fc-102">SYNOPSIS</span></span>
<span data-ttu-id="610fc-103">Zatrzymuje zadanie wsadowe.</span><span class="sxs-lookup"><span data-stu-id="610fc-103">Stops a Batch job.</span></span>

## <span data-ttu-id="610fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="610fc-104">SYNTAX</span></span>

```
Stop-AzBatchJob [-Id] <String> [[-TerminateReason] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="610fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="610fc-105">DESCRIPTION</span></span>
<span data-ttu-id="610fc-106">Polecenie cmdlet **stop-AzBatchJob** zatrzymuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="610fc-106">The **Stop-AzBatchJob** cmdlet stops an Azure Batch job.</span></span>
<span data-ttu-id="610fc-107">To polecenie oznacza zadanie jako ukończone.</span><span class="sxs-lookup"><span data-stu-id="610fc-107">This command marks the job as completed.</span></span>

## <span data-ttu-id="610fc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="610fc-108">EXAMPLES</span></span>

### <span data-ttu-id="610fc-109">Przykład 1. zatrzymanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="610fc-109">Example 1: Stop a Batch job</span></span>
```
PS C:\>Stop-AzBatchJob -Id "Job-000001" -TerminateReason "No more tasks to run" -BatchContext $Context
```

<span data-ttu-id="610fc-110">To polecenie zatrzymuje zadanie o identyfikatorze zadania ID-000001.</span><span class="sxs-lookup"><span data-stu-id="610fc-110">This command stops the job that has the ID Job-000001.</span></span>
<span data-ttu-id="610fc-111">Polecenie określa powód, dla którego wybrano zatrzymanie zadania.</span><span class="sxs-lookup"><span data-stu-id="610fc-111">The command specifies a reason that you chose to stop the job.</span></span>
<span data-ttu-id="610fc-112">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="610fc-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="610fc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="610fc-113">PARAMETERS</span></span>

### <span data-ttu-id="610fc-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="610fc-114">-BatchContext</span></span>
<span data-ttu-id="610fc-115">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="610fc-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="610fc-116">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="610fc-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="610fc-117">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="610fc-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="610fc-118">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="610fc-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="610fc-119">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="610fc-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="610fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610fc-120">-DefaultProfile</span></span>
<span data-ttu-id="610fc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="610fc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="610fc-122">-ID</span><span class="sxs-lookup"><span data-stu-id="610fc-122">-Id</span></span>
<span data-ttu-id="610fc-123">Określa identyfikator zadania, które zostanie zatrzymane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="610fc-123">Specifies the ID of the job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="610fc-124">-TerminateReason</span><span class="sxs-lookup"><span data-stu-id="610fc-124">-TerminateReason</span></span>
<span data-ttu-id="610fc-125">Umożliwia określenie przyczyny zadecydowania o zatrzymywaniu zadania.</span><span class="sxs-lookup"><span data-stu-id="610fc-125">Specifies the reason that you decided to stop the job.</span></span>
<span data-ttu-id="610fc-126">To polecenie cmdlet zapisuje ten tekst jako właściwość **TerminateReason** zadania.</span><span class="sxs-lookup"><span data-stu-id="610fc-126">This cmdlet stores this text as the **TerminateReason** property of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610fc-127">CommonParameters</span></span>
<span data-ttu-id="610fc-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="610fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610fc-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="610fc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610fc-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="610fc-130">INPUTS</span></span>

### <span data-ttu-id="610fc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="610fc-131">System.String</span></span>

### <span data-ttu-id="610fc-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="610fc-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="610fc-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="610fc-133">OUTPUTS</span></span>

### <span data-ttu-id="610fc-134">System. void</span><span class="sxs-lookup"><span data-stu-id="610fc-134">System.Void</span></span>

## <span data-ttu-id="610fc-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="610fc-135">NOTES</span></span>

## <span data-ttu-id="610fc-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="610fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="610fc-137">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="610fc-137">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="610fc-138">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="610fc-138">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="610fc-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="610fc-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="610fc-140">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="610fc-140">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="610fc-141">Nowe — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="610fc-141">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="610fc-142">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="610fc-142">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="610fc-143">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="610fc-143">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
