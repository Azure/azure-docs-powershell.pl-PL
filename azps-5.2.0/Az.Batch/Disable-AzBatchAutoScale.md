---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: c0a0f0a11b4caf18b12c21d37dd18ef153220a97
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353917"
---
# <span data-ttu-id="74ecf-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="74ecf-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="74ecf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="74ecf-103">Wyłącza automatyczne skalowanie puli.</span><span class="sxs-lookup"><span data-stu-id="74ecf-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="74ecf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74ecf-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74ecf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="74ecf-106">Polecenie cmdlet **disable-AzBatchAutoScale** wyłącza automatyczne skalowanie określonej puli.</span><span class="sxs-lookup"><span data-stu-id="74ecf-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="74ecf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74ecf-107">EXAMPLES</span></span>

### <span data-ttu-id="74ecf-108">Przykład 1: wyłączanie automatycznego skalowania puli</span><span class="sxs-lookup"><span data-stu-id="74ecf-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="74ecf-109">To polecenie wyłącza automatyczne skalowanie puli o nazwie Moja Pula.</span><span class="sxs-lookup"><span data-stu-id="74ecf-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="74ecf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74ecf-110">PARAMETERS</span></span>

### <span data-ttu-id="74ecf-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="74ecf-111">-BatchContext</span></span>
<span data-ttu-id="74ecf-112">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="74ecf-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="74ecf-113">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="74ecf-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="74ecf-114">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="74ecf-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="74ecf-115">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="74ecf-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="74ecf-116">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="74ecf-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="74ecf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ecf-117">-DefaultProfile</span></span>
<span data-ttu-id="74ecf-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74ecf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74ecf-119">-ID</span><span class="sxs-lookup"><span data-stu-id="74ecf-119">-Id</span></span>
<span data-ttu-id="74ecf-120">Określa identyfikator obiektu puli.</span><span class="sxs-lookup"><span data-stu-id="74ecf-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="74ecf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ecf-121">CommonParameters</span></span>
<span data-ttu-id="74ecf-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74ecf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ecf-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74ecf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ecf-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74ecf-124">INPUTS</span></span>

### <span data-ttu-id="74ecf-125">System. String</span><span class="sxs-lookup"><span data-stu-id="74ecf-125">System.String</span></span>

### <span data-ttu-id="74ecf-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="74ecf-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="74ecf-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74ecf-127">OUTPUTS</span></span>

### <span data-ttu-id="74ecf-128">System. void</span><span class="sxs-lookup"><span data-stu-id="74ecf-128">System.Void</span></span>

## <span data-ttu-id="74ecf-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74ecf-129">NOTES</span></span>

## <span data-ttu-id="74ecf-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74ecf-130">RELATED LINKS</span></span>

[<span data-ttu-id="74ecf-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="74ecf-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="74ecf-132">Test — AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="74ecf-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="74ecf-133">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="74ecf-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


