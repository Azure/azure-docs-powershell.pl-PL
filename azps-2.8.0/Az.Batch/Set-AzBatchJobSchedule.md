---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: 91ac0d6202eb02f724f3ea17e57846e6db6b7412
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706649"
---
# <span data-ttu-id="423bc-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="423bc-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="423bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="423bc-102">SYNOPSIS</span></span>
<span data-ttu-id="423bc-103">Ustawia harmonogram zadań.</span><span class="sxs-lookup"><span data-stu-id="423bc-103">Sets a job schedule.</span></span>

## <span data-ttu-id="423bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="423bc-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="423bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="423bc-105">DESCRIPTION</span></span>
<span data-ttu-id="423bc-106">Polecenie cmdlet **Set-AzBatchJobSchedule** ustawia harmonogram zadań w usłudze Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="423bc-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="423bc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="423bc-107">EXAMPLES</span></span>

### <span data-ttu-id="423bc-108">Przykład 1: aktualizowanie harmonogramu zadań</span><span class="sxs-lookup"><span data-stu-id="423bc-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="423bc-109">Pierwsze polecenie pobiera zadanie przy użyciu polecenia **Get-AzBatchJobSchedule** , a następnie zapisuje je w zmiennej $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="423bc-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="423bc-110">Drugie polecenie modyfikuje interwał cyklu na `$JobSchedule.Schedule` obiekcie.</span><span class="sxs-lookup"><span data-stu-id="423bc-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="423bc-111">Polecenie ostatnie aktualizuje usługę wsadu tak, aby odpowiadała obiektowi lokalnemu w $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="423bc-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="423bc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="423bc-112">PARAMETERS</span></span>

### <span data-ttu-id="423bc-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="423bc-113">-BatchContext</span></span>
<span data-ttu-id="423bc-114">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="423bc-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="423bc-115">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="423bc-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="423bc-116">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="423bc-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="423bc-117">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="423bc-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="423bc-118">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="423bc-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="423bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423bc-119">-DefaultProfile</span></span>
<span data-ttu-id="423bc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="423bc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="423bc-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="423bc-121">-JobSchedule</span></span>
<span data-ttu-id="423bc-122">Określa obiekt **PSCloudJobSchedule** , który reprezentuje harmonogram zadania.</span><span class="sxs-lookup"><span data-stu-id="423bc-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="423bc-123">Aby uzyskać obiekt **PSCloudJobSchedule** , użyj polecenia cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="423bc-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="423bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423bc-124">CommonParameters</span></span>
<span data-ttu-id="423bc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="423bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423bc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="423bc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423bc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="423bc-127">INPUTS</span></span>

### <span data-ttu-id="423bc-128">Microsoft.Azure.Commands.Batch. Modele. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="423bc-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="423bc-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="423bc-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="423bc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="423bc-130">OUTPUTS</span></span>

### <span data-ttu-id="423bc-131">System. void</span><span class="sxs-lookup"><span data-stu-id="423bc-131">System.Void</span></span>

## <span data-ttu-id="423bc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="423bc-132">NOTES</span></span>

## <span data-ttu-id="423bc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="423bc-133">RELATED LINKS</span></span>

[<span data-ttu-id="423bc-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="423bc-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="423bc-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="423bc-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="423bc-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="423bc-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="423bc-137">Nowe — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="423bc-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="423bc-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="423bc-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="423bc-139">Zatrzymaj — AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="423bc-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


