---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357049"
---
# <span data-ttu-id="a2122-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="a2122-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="a2122-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2122-102">SYNOPSIS</span></span>
<span data-ttu-id="a2122-103">Zatrzymuje operację zmiany rozmiaru puli.</span><span class="sxs-lookup"><span data-stu-id="a2122-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="a2122-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2122-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2122-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a2122-105">DESCRIPTION</span></span>
<span data-ttu-id="a2122-106">Polecenie cmdlet **stop-AzBatchPoolResize** zatrzymuje operację zmiany rozmiaru wsadu Azure Part na puli.</span><span class="sxs-lookup"><span data-stu-id="a2122-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="a2122-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2122-107">EXAMPLES</span></span>

### <span data-ttu-id="a2122-108">Przykład 1. Zatrzymaj zmianę rozmiaru puli</span><span class="sxs-lookup"><span data-stu-id="a2122-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="a2122-109">To polecenie zatrzymuje operację zmiany rozmiaru puli o IDENTYFIKATORze ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="a2122-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="a2122-110">Użyj polecenia cmdlet Get-AzBatchAccountKey, aby przypisać kontekst do zmiennej $Context.</span><span class="sxs-lookup"><span data-stu-id="a2122-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a2122-111">Przykład 2: zatrzymywanie zmiany rozmiaru puli za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="a2122-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="a2122-112">To polecenie zatrzymuje zmianę rozmiaru puli za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="a2122-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="a2122-113">Polecenie pobiera pulę o IDENTYFIKATORze ContosoPool06 przy użyciu polecenia cmdlet Get-AzBatchPool.</span><span class="sxs-lookup"><span data-stu-id="a2122-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="a2122-114">Polecenie przekazuje ten obiekt puli do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2122-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="a2122-115">Polecenie zatrzyma operację zmiany rozmiaru w tej puli.</span><span class="sxs-lookup"><span data-stu-id="a2122-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="a2122-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2122-116">PARAMETERS</span></span>

### <span data-ttu-id="a2122-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a2122-117">-BatchContext</span></span>
<span data-ttu-id="a2122-118">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a2122-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a2122-119">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="a2122-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a2122-120">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="a2122-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a2122-121">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="a2122-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a2122-122">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a2122-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a2122-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2122-123">-DefaultProfile</span></span>
<span data-ttu-id="a2122-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2122-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2122-125">-ID</span><span class="sxs-lookup"><span data-stu-id="a2122-125">-Id</span></span>
<span data-ttu-id="a2122-126">Określa identyfikator puli, dla którego to polecenie cmdlet zatrzyma operację zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="a2122-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="a2122-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2122-127">CommonParameters</span></span>
<span data-ttu-id="a2122-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2122-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2122-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2122-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2122-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2122-130">INPUTS</span></span>

### <span data-ttu-id="a2122-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a2122-131">System.String</span></span>

### <span data-ttu-id="a2122-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a2122-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a2122-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2122-133">OUTPUTS</span></span>

### <span data-ttu-id="a2122-134">System. void</span><span class="sxs-lookup"><span data-stu-id="a2122-134">System.Void</span></span>

## <span data-ttu-id="a2122-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2122-135">NOTES</span></span>

## <span data-ttu-id="a2122-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2122-136">RELATED LINKS</span></span>

[<span data-ttu-id="a2122-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a2122-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a2122-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="a2122-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="a2122-139">Start — AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="a2122-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="a2122-140">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="a2122-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
