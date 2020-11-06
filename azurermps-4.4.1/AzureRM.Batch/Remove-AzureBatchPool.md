---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 01098a20ebb754d4445a85dd5a6bb0d327453234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547028"
---
# <span data-ttu-id="176ad-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="176ad-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="176ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="176ad-102">SYNOPSIS</span></span>
<span data-ttu-id="176ad-103">Usuwa określoną pulę partii.</span><span class="sxs-lookup"><span data-stu-id="176ad-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="176ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="176ad-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="176ad-105">DESCRIPTION</span></span>
<span data-ttu-id="176ad-106">Polecenie cmdlet **Remove-AzureBatchPool** usuwa określoną pulę usługi Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="176ad-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="176ad-107">Zostanie wyświetlony monit o potwierdzenie, chyba że zostanie użyty parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="176ad-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="176ad-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="176ad-108">EXAMPLES</span></span>

### <span data-ttu-id="176ad-109">Przykład 1: Usuwanie puli partii według identyfikatora puli</span><span class="sxs-lookup"><span data-stu-id="176ad-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="176ad-110">To polecenie usuwa pulę o IDENTYFIKATORze moja Pula.</span><span class="sxs-lookup"><span data-stu-id="176ad-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="176ad-111">Użytkownik jest monitowany o potwierdzenie przed wykonaniem operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="176ad-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="176ad-112">Przykład 2: Usuwanie wszystkich pul partii według siły</span><span class="sxs-lookup"><span data-stu-id="176ad-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="176ad-113">To polecenie usuwa wszystkie pule partii.</span><span class="sxs-lookup"><span data-stu-id="176ad-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="176ad-114">Ponieważ parametr *Force* jest obecny, monit o potwierdzenie jest pomijany.</span><span class="sxs-lookup"><span data-stu-id="176ad-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="176ad-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="176ad-115">PARAMETERS</span></span>

### <span data-ttu-id="176ad-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="176ad-116">-BatchContext</span></span>
<span data-ttu-id="176ad-117">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="176ad-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="176ad-118">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="176ad-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="176ad-119">-Force</span><span class="sxs-lookup"><span data-stu-id="176ad-119">-Force</span></span>
<span data-ttu-id="176ad-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="176ad-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176ad-121">-ID</span><span class="sxs-lookup"><span data-stu-id="176ad-121">-Id</span></span>
<span data-ttu-id="176ad-122">Określa identyfikator puli, którą należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="176ad-122">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="176ad-123">Nie można określać symboli wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="176ad-123">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="176ad-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="176ad-124">-Confirm</span></span>
<span data-ttu-id="176ad-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176ad-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176ad-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176ad-126">-WhatIf</span></span>
<span data-ttu-id="176ad-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176ad-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176ad-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="176ad-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176ad-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176ad-129">-DefaultProfile</span></span>
<span data-ttu-id="176ad-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="176ad-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176ad-131">CommonParameters</span></span>
<span data-ttu-id="176ad-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176ad-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176ad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176ad-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="176ad-134">INPUTS</span></span>

### <span data-ttu-id="176ad-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="176ad-135">BatchAccountContext</span></span>
<span data-ttu-id="176ad-136">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="176ad-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="176ad-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="176ad-137">OUTPUTS</span></span>

## <span data-ttu-id="176ad-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="176ad-138">NOTES</span></span>

## <span data-ttu-id="176ad-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="176ad-139">RELATED LINKS</span></span>

[<span data-ttu-id="176ad-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="176ad-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="176ad-141">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="176ad-141">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="176ad-142">Nowe — AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="176ad-142">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="176ad-143">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="176ad-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


