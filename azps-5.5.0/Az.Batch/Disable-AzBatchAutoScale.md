---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: c0a0f0a11b4caf18b12c21d37dd18ef153220a97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239482"
---
# <span data-ttu-id="f9c8f-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f9c8f-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="f9c8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c8f-103">Wyłącza automatyczne skalowanie puli.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="f9c8f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f9c8f-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9c8f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f9c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="f9c8f-106">Polecenie cmdlet **Disable-AzBatchAutoScale** wyłącza automatyczne skalowanie określonej puli.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="f9c8f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f9c8f-107">EXAMPLES</span></span>

### <span data-ttu-id="f9c8f-108">Przykład 1. Wyłączanie automatycznego skalowania puli</span><span class="sxs-lookup"><span data-stu-id="f9c8f-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="f9c8f-109">To polecenie wyłącza automatyczne skalowanie puli o nazwie MyPool.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="f9c8f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9c8f-110">PARAMETERS</span></span>

### <span data-ttu-id="f9c8f-111">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="f9c8f-111">-BatchContext</span></span>
<span data-ttu-id="f9c8f-112">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f9c8f-113">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f9c8f-114">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f9c8f-115">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f9c8f-116">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f9c8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c8f-117">-DefaultProfile</span></span>
<span data-ttu-id="f9c8f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9c8f-119">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="f9c8f-119">-Id</span></span>
<span data-ttu-id="f9c8f-120">Określa identyfikator obiektu puli.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="f9c8f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c8f-121">CommonParameters</span></span>
<span data-ttu-id="f9c8f-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c8f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9c8f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c8f-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9c8f-124">INPUTS</span></span>

### <span data-ttu-id="f9c8f-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f9c8f-125">System.String</span></span>

### <span data-ttu-id="f9c8f-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f9c8f-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f9c8f-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9c8f-127">OUTPUTS</span></span>

### <span data-ttu-id="f9c8f-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="f9c8f-128">System.Void</span></span>

## <span data-ttu-id="f9c8f-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f9c8f-129">NOTES</span></span>

## <span data-ttu-id="f9c8f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9c8f-130">RELATED LINKS</span></span>

[<span data-ttu-id="f9c8f-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f9c8f-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="f9c8f-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="f9c8f-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="f9c8f-133">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f9c8f-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


