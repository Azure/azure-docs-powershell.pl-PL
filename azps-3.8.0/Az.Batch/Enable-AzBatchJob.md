---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: dc3b169df0b29ec47dc54864c5a2999a220a60de
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "94061655"
---
# <span data-ttu-id="99a74-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="99a74-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="99a74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99a74-102">SYNOPSIS</span></span>
<span data-ttu-id="99a74-103">Umożliwia wykonywanie zadań wsadowych.</span><span class="sxs-lookup"><span data-stu-id="99a74-103">Enables a Batch job.</span></span>

## <span data-ttu-id="99a74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99a74-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99a74-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99a74-105">DESCRIPTION</span></span>
<span data-ttu-id="99a74-106">Polecenie cmdlet **enable-AzBatchJob** włącza zadanie usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="99a74-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="99a74-107">Po włączeniu zadania można uruchamiać nowe zadania.</span><span class="sxs-lookup"><span data-stu-id="99a74-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="99a74-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99a74-108">EXAMPLES</span></span>

### <span data-ttu-id="99a74-109">Przykład 1. Włączanie zadania wsadowego</span><span class="sxs-lookup"><span data-stu-id="99a74-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="99a74-110">To polecenie umożliwia włączenie zadania o identyfikatorze ID-000001.</span><span class="sxs-lookup"><span data-stu-id="99a74-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="99a74-111">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="99a74-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="99a74-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99a74-112">PARAMETERS</span></span>

### <span data-ttu-id="99a74-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="99a74-113">-BatchContext</span></span>
<span data-ttu-id="99a74-114">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="99a74-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="99a74-115">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="99a74-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="99a74-116">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="99a74-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="99a74-117">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="99a74-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="99a74-118">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="99a74-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="99a74-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a74-119">-DefaultProfile</span></span>
<span data-ttu-id="99a74-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99a74-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99a74-121">-ID</span><span class="sxs-lookup"><span data-stu-id="99a74-121">-Id</span></span>
<span data-ttu-id="99a74-122">Określa identyfikator zadania, które włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99a74-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="99a74-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a74-123">CommonParameters</span></span>
<span data-ttu-id="99a74-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a74-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a74-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99a74-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a74-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99a74-126">INPUTS</span></span>

### <span data-ttu-id="99a74-127">System. String</span><span class="sxs-lookup"><span data-stu-id="99a74-127">System.String</span></span>

### <span data-ttu-id="99a74-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="99a74-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="99a74-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99a74-129">OUTPUTS</span></span>

### <span data-ttu-id="99a74-130">System. void</span><span class="sxs-lookup"><span data-stu-id="99a74-130">System.Void</span></span>

## <span data-ttu-id="99a74-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99a74-131">NOTES</span></span>

## <span data-ttu-id="99a74-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99a74-132">RELATED LINKS</span></span>

[<span data-ttu-id="99a74-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="99a74-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="99a74-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="99a74-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="99a74-135">Nowe — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="99a74-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="99a74-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="99a74-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="99a74-137">Zatrzymaj — AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="99a74-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="99a74-138">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="99a74-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


