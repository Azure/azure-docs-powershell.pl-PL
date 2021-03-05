---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: cf4512bc0d219c164be6543d5633a43c9052cc4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004618"
---
# <span data-ttu-id="52960-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="52960-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="52960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52960-102">SYNOPSIS</span></span>
<span data-ttu-id="52960-103">Ustawia harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="52960-103">Sets a job schedule.</span></span>

## <span data-ttu-id="52960-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52960-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52960-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="52960-105">DESCRIPTION</span></span>
<span data-ttu-id="52960-106">Polecenie **cmdlet Set-AzBatchJobSchedule** ustawia harmonogram zadań w usłudze wsadowej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="52960-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="52960-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52960-107">EXAMPLES</span></span>

### <span data-ttu-id="52960-108">Przykład 1. Aktualizowanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="52960-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="52960-109">Pierwsze polecenie otrzymuje zadanie za pomocą polecenia **Get-AzBatchJobSchedule,** a następnie zapisuje je w $JobSchedule danych.</span><span class="sxs-lookup"><span data-stu-id="52960-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="52960-110">Drugie polecenie modyfikuje interwał cyklu `$JobSchedule.Schedule` obiektu.</span><span class="sxs-lookup"><span data-stu-id="52960-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="52960-111">Ostatnie polecenie aktualizuje usługę Batch, aby dopasować obiekt lokalny w $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="52960-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="52960-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52960-112">PARAMETERS</span></span>

### <span data-ttu-id="52960-113">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="52960-113">-BatchContext</span></span>
<span data-ttu-id="52960-114">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="52960-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="52960-115">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="52960-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="52960-116">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="52960-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="52960-117">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="52960-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="52960-118">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="52960-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="52960-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52960-119">-DefaultProfile</span></span>
<span data-ttu-id="52960-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52960-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52960-121">— Harmonogram zadań</span><span class="sxs-lookup"><span data-stu-id="52960-121">-JobSchedule</span></span>
<span data-ttu-id="52960-122">Określa **obiekt PSCloudJobSchedule** reprezentujący harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="52960-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="52960-123">Aby uzyskać **obiekt PSCloudJobSchedule,** użyj Get-AzBatchJobSchedule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52960-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52960-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52960-124">CommonParameters</span></span>
<span data-ttu-id="52960-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52960-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52960-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52960-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52960-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52960-127">INPUTS</span></span>

### <span data-ttu-id="52960-128">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="52960-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="52960-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="52960-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="52960-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52960-130">OUTPUTS</span></span>

### <span data-ttu-id="52960-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="52960-131">System.Void</span></span>

## <span data-ttu-id="52960-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52960-132">NOTES</span></span>

## <span data-ttu-id="52960-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52960-133">RELATED LINKS</span></span>

[<span data-ttu-id="52960-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="52960-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="52960-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="52960-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="52960-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="52960-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="52960-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="52960-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="52960-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="52960-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="52960-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="52960-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


