---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548375"
---
# <span data-ttu-id="865b4-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="865b4-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="865b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="865b4-102">SYNOPSIS</span></span>
<span data-ttu-id="865b4-103">Wyłącza automatyczne skalowanie puli.</span><span class="sxs-lookup"><span data-stu-id="865b4-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="865b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="865b4-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="865b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="865b4-105">DESCRIPTION</span></span>
<span data-ttu-id="865b4-106">Polecenie cmdlet **disable-AzureBatchAutoScale** wyłącza automatyczne skalowanie określonej puli.</span><span class="sxs-lookup"><span data-stu-id="865b4-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="865b4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="865b4-107">EXAMPLES</span></span>

### <span data-ttu-id="865b4-108">Przykład 1: wyłączanie automatycznego skalowania puli</span><span class="sxs-lookup"><span data-stu-id="865b4-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="865b4-109">To polecenie wyłącza automatyczne skalowanie puli o nazwie Moja Pula.</span><span class="sxs-lookup"><span data-stu-id="865b4-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="865b4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="865b4-110">PARAMETERS</span></span>

### <span data-ttu-id="865b4-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="865b4-111">-BatchContext</span></span>
<span data-ttu-id="865b4-112">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="865b4-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="865b4-113">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="865b4-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="865b4-114">-ID</span><span class="sxs-lookup"><span data-stu-id="865b4-114">-Id</span></span>
<span data-ttu-id="865b4-115">Określa identyfikator obiektu puli.</span><span class="sxs-lookup"><span data-stu-id="865b4-115">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="865b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865b4-116">-DefaultProfile</span></span>
<span data-ttu-id="865b4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="865b4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="865b4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865b4-118">CommonParameters</span></span>
<span data-ttu-id="865b4-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="865b4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865b4-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="865b4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865b4-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="865b4-121">INPUTS</span></span>

### <span data-ttu-id="865b4-122">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="865b4-122">BatchAccountContext</span></span>
<span data-ttu-id="865b4-123">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="865b4-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="865b4-124">Ciąg</span><span class="sxs-lookup"><span data-stu-id="865b4-124">String</span></span>
<span data-ttu-id="865b4-125">Parametr "ID" akceptuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="865b4-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="865b4-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="865b4-126">OUTPUTS</span></span>

## <span data-ttu-id="865b4-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="865b4-127">NOTES</span></span>

## <span data-ttu-id="865b4-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="865b4-128">RELATED LINKS</span></span>

[<span data-ttu-id="865b4-129">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="865b4-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="865b4-130">Test — AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="865b4-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="865b4-131">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="865b4-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


