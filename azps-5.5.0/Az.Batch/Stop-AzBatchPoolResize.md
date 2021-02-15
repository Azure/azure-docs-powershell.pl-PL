---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195218"
---
# <span data-ttu-id="fbef5-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="fbef5-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="fbef5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbef5-102">SYNOPSIS</span></span>
<span data-ttu-id="fbef5-103">Zatrzymuje operację zmiany rozmiaru puli.</span><span class="sxs-lookup"><span data-stu-id="fbef5-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="fbef5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbef5-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbef5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbef5-105">DESCRIPTION</span></span>
<span data-ttu-id="fbef5-106">Polecenie **cmdlet Stop-AzBatchPoolResize** zatrzymuje operację zmiany rozmiaru partii platformy Azure w puli.</span><span class="sxs-lookup"><span data-stu-id="fbef5-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="fbef5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbef5-107">EXAMPLES</span></span>

### <span data-ttu-id="fbef5-108">Przykład 1. Zatrzymywanie zmiany rozmiaru puli</span><span class="sxs-lookup"><span data-stu-id="fbef5-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="fbef5-109">To polecenie zatrzymuje operację zmiany rozmiaru puli o identyfikatorze ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="fbef5-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="fbef5-110">Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.</span><span class="sxs-lookup"><span data-stu-id="fbef5-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="fbef5-111">Przykład 2. Zatrzymywanie zmiany rozmiaru puli przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="fbef5-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="fbef5-112">To polecenie zatrzymuje zmienianie rozmiaru puli przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="fbef5-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="fbef5-113">Polecenie pobiera pulę o identyfikatorze ContosoPool06 przy użyciu Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbef5-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="fbef5-114">Polecenie przekazuje ten obiekt puli do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbef5-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="fbef5-115">To polecenie zatrzymuje operację zmiany rozmiaru tej puli.</span><span class="sxs-lookup"><span data-stu-id="fbef5-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="fbef5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbef5-116">PARAMETERS</span></span>

### <span data-ttu-id="fbef5-117">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="fbef5-117">-BatchContext</span></span>
<span data-ttu-id="fbef5-118">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="fbef5-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fbef5-119">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fbef5-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fbef5-120">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="fbef5-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fbef5-121">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="fbef5-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fbef5-122">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="fbef5-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fbef5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbef5-123">-DefaultProfile</span></span>
<span data-ttu-id="fbef5-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbef5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbef5-125">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="fbef5-125">-Id</span></span>
<span data-ttu-id="fbef5-126">Określa identyfikator puli, dla której to polecenie cmdlet zatrzymuje operację zmiany rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="fbef5-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="fbef5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbef5-127">CommonParameters</span></span>
<span data-ttu-id="fbef5-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbef5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbef5-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbef5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbef5-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbef5-130">INPUTS</span></span>

### <span data-ttu-id="fbef5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fbef5-131">System.String</span></span>

### <span data-ttu-id="fbef5-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fbef5-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fbef5-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbef5-133">OUTPUTS</span></span>

### <span data-ttu-id="fbef5-134">System.Void</span><span class="sxs-lookup"><span data-stu-id="fbef5-134">System.Void</span></span>

## <span data-ttu-id="fbef5-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbef5-135">NOTES</span></span>

## <span data-ttu-id="fbef5-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbef5-136">RELATED LINKS</span></span>

[<span data-ttu-id="fbef5-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fbef5-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fbef5-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="fbef5-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="fbef5-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="fbef5-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="fbef5-140">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="fbef5-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
