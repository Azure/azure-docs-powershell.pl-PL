---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 86e977c3d538c9eeb5f26da7d70db1726adf119b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710792"
---
# <span data-ttu-id="a18a7-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18a7-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="a18a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a18a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a18a7-103">Umożliwia zaktualizowanie zadania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a18a7-103">Updates a Batch job.</span></span>

## <span data-ttu-id="a18a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a18a7-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a18a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a18a7-105">DESCRIPTION</span></span>
<span data-ttu-id="a18a7-106">Polecenie cmdlet **Set-AzBatchJob** aktualizuje zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="a18a7-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="a18a7-107">Użyj polecenia cmdlet Get-AzBatchJob, aby uzyskać obiekt **PSCloudJob** .</span><span class="sxs-lookup"><span data-stu-id="a18a7-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="a18a7-108">Zmodyfikuj właściwości tego obiektu, a następnie użyj bieżącego polecenia cmdlet, aby zatwierdzić zmiany w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a18a7-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="a18a7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a18a7-109">EXAMPLES</span></span>

### <span data-ttu-id="a18a7-110">Przykład 1: aktualizowanie zadania</span><span class="sxs-lookup"><span data-stu-id="a18a7-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="a18a7-111">Pierwsze polecenie pobiera zadanie przy użyciu polecenia **Get-AzBatchJob** , a następnie zapisuje je w zmiennej $Job.</span><span class="sxs-lookup"><span data-stu-id="a18a7-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="a18a7-112">Drugie polecenie modyfikuje specyfikację priorytetu obiektu $Job.</span><span class="sxs-lookup"><span data-stu-id="a18a7-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="a18a7-113">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $Job.</span><span class="sxs-lookup"><span data-stu-id="a18a7-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="a18a7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a18a7-114">PARAMETERS</span></span>

### <span data-ttu-id="a18a7-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a18a7-115">-BatchContext</span></span>
<span data-ttu-id="a18a7-116">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a18a7-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a18a7-117">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a18a7-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a18a7-118">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="a18a7-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a18a7-119">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="a18a7-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a18a7-120">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a18a7-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a18a7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18a7-121">-DefaultProfile</span></span>
<span data-ttu-id="a18a7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a18a7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a18a7-123">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="a18a7-123">-Job</span></span>
<span data-ttu-id="a18a7-124">Określa **PSCloudJob** , do którego to polecenie cmdlet aktualizuje usługę wsadu.</span><span class="sxs-lookup"><span data-stu-id="a18a7-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a18a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18a7-125">CommonParameters</span></span>
<span data-ttu-id="a18a7-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18a7-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a18a7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18a7-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a18a7-128">INPUTS</span></span>

### <span data-ttu-id="a18a7-129">Microsoft.Azure.Commands.Batch. Modele. PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="a18a7-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="a18a7-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a18a7-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a18a7-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a18a7-131">OUTPUTS</span></span>

### <span data-ttu-id="a18a7-132">System. void</span><span class="sxs-lookup"><span data-stu-id="a18a7-132">System.Void</span></span>

## <span data-ttu-id="a18a7-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a18a7-133">NOTES</span></span>

## <span data-ttu-id="a18a7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a18a7-134">RELATED LINKS</span></span>

[<span data-ttu-id="a18a7-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18a7-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="a18a7-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18a7-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="a18a7-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18a7-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="a18a7-138">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a18a7-138">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a18a7-139">Nowe — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18a7-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="a18a7-140">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18a7-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="a18a7-141">Zatrzymaj — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a18a7-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="a18a7-142">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="a18a7-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


