---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: d0daabef3f4fe9ef60a90365054e12e869f0856a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716972"
---
# <span data-ttu-id="1b0f5-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b0f5-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="1b0f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="1b0f5-103">Pobiera zasady lub zasady dostępu do kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b0f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b0f5-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b0f5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b0f5-105">DESCRIPTION</span></span>
<span data-ttu-id="1b0f5-106">Polecenie cmdlet **Get-AzureStorageQueueStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="1b0f5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b0f5-107">EXAMPLES</span></span>

### <span data-ttu-id="1b0f5-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w kolejce</span><span class="sxs-lookup"><span data-stu-id="1b0f5-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="1b0f5-109">To polecenie pobiera zasady dostępu o nazwie Policy12 w kolejce magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="1b0f5-110">Przykład 2: pobieranie wszystkich przechowywanych zasad dostępu w kolejce</span><span class="sxs-lookup"><span data-stu-id="1b0f5-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="1b0f5-111">To polecenie pobiera wszystkie zapisane zasady dostępu w kolejce o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="1b0f5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b0f5-112">PARAMETERS</span></span>

### <span data-ttu-id="1b0f5-113">-Context</span><span class="sxs-lookup"><span data-stu-id="1b0f5-113">-Context</span></span>
<span data-ttu-id="1b0f5-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1b0f5-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b0f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b0f5-116">-DefaultProfile</span></span>
<span data-ttu-id="1b0f5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b0f5-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="1b0f5-118">-Policy</span></span>
<span data-ttu-id="1b0f5-119">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="1b0f5-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b0f5-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="1b0f5-120">-Queue</span></span>
<span data-ttu-id="1b0f5-121">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b0f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b0f5-122">CommonParameters</span></span>
<span data-ttu-id="1b0f5-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b0f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b0f5-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b0f5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b0f5-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b0f5-125">INPUTS</span></span>

### <span data-ttu-id="1b0f5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1b0f5-126">System.String</span></span>

### <span data-ttu-id="1b0f5-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b0f5-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1b0f5-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b0f5-128">OUTPUTS</span></span>

### <span data-ttu-id="1b0f5-129">Microsoft. platformy windowsazure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="1b0f5-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="1b0f5-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b0f5-130">NOTES</span></span>

## <span data-ttu-id="1b0f5-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b0f5-131">RELATED LINKS</span></span>

[<span data-ttu-id="1b0f5-132">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b0f5-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1b0f5-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b0f5-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1b0f5-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b0f5-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1b0f5-135">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b0f5-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


