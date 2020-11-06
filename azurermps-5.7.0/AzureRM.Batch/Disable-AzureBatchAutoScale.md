---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a53e72cd31d3ca43cf5c9a4e6a66de4bc2bd59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554295"
---
# <span data-ttu-id="58689-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="58689-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="58689-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58689-102">SYNOPSIS</span></span>
<span data-ttu-id="58689-103">Wyłącza automatyczne skalowanie puli.</span><span class="sxs-lookup"><span data-stu-id="58689-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58689-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58689-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58689-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58689-105">DESCRIPTION</span></span>
<span data-ttu-id="58689-106">Polecenie cmdlet **disable-AzureBatchAutoScale** wyłącza automatyczne skalowanie określonej puli.</span><span class="sxs-lookup"><span data-stu-id="58689-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="58689-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58689-107">EXAMPLES</span></span>

### <span data-ttu-id="58689-108">Przykład 1: wyłączanie automatycznego skalowania puli</span><span class="sxs-lookup"><span data-stu-id="58689-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="58689-109">To polecenie wyłącza automatyczne skalowanie puli o nazwie Moja Pula.</span><span class="sxs-lookup"><span data-stu-id="58689-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="58689-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58689-110">PARAMETERS</span></span>

### <span data-ttu-id="58689-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="58689-111">-BatchContext</span></span>
<span data-ttu-id="58689-112">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="58689-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="58689-113">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="58689-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="58689-114">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="58689-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="58689-115">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="58689-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="58689-116">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="58689-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58689-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58689-117">-DefaultProfile</span></span>
<span data-ttu-id="58689-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58689-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58689-119">-ID</span><span class="sxs-lookup"><span data-stu-id="58689-119">-Id</span></span>
<span data-ttu-id="58689-120">Określa identyfikator obiektu puli.</span><span class="sxs-lookup"><span data-stu-id="58689-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58689-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58689-121">CommonParameters</span></span>
<span data-ttu-id="58689-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58689-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58689-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58689-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58689-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58689-124">INPUTS</span></span>

### <span data-ttu-id="58689-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="58689-125">BatchAccountContext</span></span>
<span data-ttu-id="58689-126">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="58689-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="58689-127">Ciąg</span><span class="sxs-lookup"><span data-stu-id="58689-127">String</span></span>
<span data-ttu-id="58689-128">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="58689-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="58689-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58689-129">OUTPUTS</span></span>

## <span data-ttu-id="58689-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58689-130">NOTES</span></span>

## <span data-ttu-id="58689-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58689-131">RELATED LINKS</span></span>

[<span data-ttu-id="58689-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="58689-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="58689-133">Test — AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="58689-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="58689-134">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="58689-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


