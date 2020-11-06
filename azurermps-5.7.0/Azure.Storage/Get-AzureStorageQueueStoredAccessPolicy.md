---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ebf5596ba63a86e3865c5a6dc05bdea648dc18c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545920"
---
# <span data-ttu-id="14bcc-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14bcc-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="14bcc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="14bcc-103">Pobiera zasady lub zasady dostępu do kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14bcc-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14bcc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14bcc-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="14bcc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="14bcc-105">DESCRIPTION</span></span>
<span data-ttu-id="14bcc-106">Polecenie cmdlet **Get-AzureStorageQueueStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14bcc-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="14bcc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14bcc-107">EXAMPLES</span></span>

### <span data-ttu-id="14bcc-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w kolejce</span><span class="sxs-lookup"><span data-stu-id="14bcc-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="14bcc-109">To polecenie pobiera zasady dostępu o nazwie Policy12 w kolejce magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="14bcc-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="14bcc-110">Przykład 2: pobieranie wszystkich przechowywanych zasad dostępu w kolejce</span><span class="sxs-lookup"><span data-stu-id="14bcc-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="14bcc-111">To polecenie pobiera wszystkie zapisane zasady dostępu w kolejce o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="14bcc-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="14bcc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14bcc-112">PARAMETERS</span></span>

### <span data-ttu-id="14bcc-113">-Context</span><span class="sxs-lookup"><span data-stu-id="14bcc-113">-Context</span></span>
<span data-ttu-id="14bcc-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="14bcc-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="14bcc-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="14bcc-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14bcc-116">-Policy</span><span class="sxs-lookup"><span data-stu-id="14bcc-116">-Policy</span></span>
<span data-ttu-id="14bcc-117">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="14bcc-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14bcc-118">-Queue</span><span class="sxs-lookup"><span data-stu-id="14bcc-118">-Queue</span></span>
<span data-ttu-id="14bcc-119">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14bcc-119">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14bcc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14bcc-120">CommonParameters</span></span>
<span data-ttu-id="14bcc-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14bcc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14bcc-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14bcc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14bcc-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14bcc-123">INPUTS</span></span>

### <span data-ttu-id="14bcc-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="14bcc-124">IStorageContext</span></span>

<span data-ttu-id="14bcc-125">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="14bcc-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="14bcc-126">Ciąg</span><span class="sxs-lookup"><span data-stu-id="14bcc-126">String</span></span>

<span data-ttu-id="14bcc-127">Parametr "queue" przyjmuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="14bcc-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="14bcc-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14bcc-128">OUTPUTS</span></span>

### <span data-ttu-id="14bcc-129">Microsoft. platformy windowsazure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="14bcc-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="14bcc-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14bcc-130">NOTES</span></span>

## <span data-ttu-id="14bcc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14bcc-131">RELATED LINKS</span></span>

[<span data-ttu-id="14bcc-132">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14bcc-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="14bcc-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14bcc-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="14bcc-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="14bcc-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="14bcc-135">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="14bcc-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


