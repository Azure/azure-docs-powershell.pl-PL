---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504281"
---
# <span data-ttu-id="e2063-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="e2063-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="e2063-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2063-102">SYNOPSIS</span></span>
<span data-ttu-id="e2063-103">Zatrzymuje operację zmiany rozmiaru puli.</span><span class="sxs-lookup"><span data-stu-id="e2063-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="e2063-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2063-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2063-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2063-105">DESCRIPTION</span></span>
<span data-ttu-id="e2063-106">Polecenie cmdlet **stop-AzBatchPoolResize** zatrzymuje operację zmiany rozmiaru wsadu Azure Part na puli.</span><span class="sxs-lookup"><span data-stu-id="e2063-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="e2063-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2063-107">EXAMPLES</span></span>

### <span data-ttu-id="e2063-108">Przykład 1. Zatrzymaj zmianę rozmiaru puli</span><span class="sxs-lookup"><span data-stu-id="e2063-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="e2063-109">To polecenie zatrzymuje operację zmiany rozmiaru puli o IDENTYFIKATORze ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="e2063-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="e2063-110">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="e2063-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e2063-111">Przykład 2: zatrzymywanie zmiany rozmiaru puli za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="e2063-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="e2063-112">To polecenie zatrzymuje zmianę rozmiaru puli za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="e2063-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="e2063-113">Polecenie pobiera pulę o IDENTYFIKATORze ContosoPool06 przy użyciu polecenia cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="e2063-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="e2063-114">Polecenie przekazuje ten obiekt puli do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2063-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="e2063-115">Polecenie zatrzyma operację zmiany rozmiaru w tej puli.</span><span class="sxs-lookup"><span data-stu-id="e2063-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="e2063-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2063-116">PARAMETERS</span></span>

### <span data-ttu-id="e2063-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e2063-117">-BatchContext</span></span>
<span data-ttu-id="e2063-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e2063-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e2063-119">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="e2063-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e2063-120">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="e2063-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e2063-121">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="e2063-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e2063-122">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e2063-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e2063-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2063-123">-DefaultProfile</span></span>
<span data-ttu-id="e2063-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2063-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2063-125">-ID</span><span class="sxs-lookup"><span data-stu-id="e2063-125">-Id</span></span>
<span data-ttu-id="e2063-126">Określa identyfikator puli, dla którego to polecenie cmdlet zatrzyma operację zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="e2063-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="e2063-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2063-127">CommonParameters</span></span>
<span data-ttu-id="e2063-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2063-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2063-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2063-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2063-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2063-130">INPUTS</span></span>

### <span data-ttu-id="e2063-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e2063-131">System.String</span></span>

### <span data-ttu-id="e2063-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e2063-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e2063-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2063-133">OUTPUTS</span></span>

### <span data-ttu-id="e2063-134">System. void</span><span class="sxs-lookup"><span data-stu-id="e2063-134">System.Void</span></span>

## <span data-ttu-id="e2063-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2063-135">NOTES</span></span>

## <span data-ttu-id="e2063-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2063-136">RELATED LINKS</span></span>

[<span data-ttu-id="e2063-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e2063-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e2063-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e2063-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="e2063-139">Start — AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="e2063-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="e2063-140">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e2063-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
