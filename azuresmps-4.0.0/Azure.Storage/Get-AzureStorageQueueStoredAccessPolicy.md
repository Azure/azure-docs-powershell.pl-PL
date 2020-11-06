---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524021"
---
# <span data-ttu-id="91408-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="91408-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="91408-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91408-102">SYNOPSIS</span></span>
<span data-ttu-id="91408-103">Pobiera zasady lub zasady dostępu do kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="91408-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="91408-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91408-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="91408-105">Opis</span><span class="sxs-lookup"><span data-stu-id="91408-105">DESCRIPTION</span></span>
<span data-ttu-id="91408-106">Polecenie cmdlet **Get-AzureStorageQueueStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu lub zasad dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="91408-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="91408-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91408-107">EXAMPLES</span></span>

### <span data-ttu-id="91408-108">Przykład 1: uzyskiwanie zapisanych zasad dostępu w kolejce</span><span class="sxs-lookup"><span data-stu-id="91408-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="91408-109">To polecenie pobiera zasady dostępu o nazwie Policy12 w kolejce magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="91408-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="91408-110">Przykład 2: pobieranie wszystkich przechowywanych zasad dostępu w kolejce</span><span class="sxs-lookup"><span data-stu-id="91408-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="91408-111">To polecenie pobiera wszystkie zapisane zasady dostępu w kolejce o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="91408-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="91408-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91408-112">PARAMETERS</span></span>

### <span data-ttu-id="91408-113">-Context</span><span class="sxs-lookup"><span data-stu-id="91408-113">-Context</span></span>
<span data-ttu-id="91408-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="91408-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="91408-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="91408-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="91408-116">-Policy</span><span class="sxs-lookup"><span data-stu-id="91408-116">-Policy</span></span>
<span data-ttu-id="91408-117">Określa przechowywane zasady dostępu, które zawierają uprawnienia do tego tokenu współdzielonego podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="91408-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="91408-118">-Queue</span><span class="sxs-lookup"><span data-stu-id="91408-118">-Queue</span></span>
<span data-ttu-id="91408-119">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="91408-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="91408-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91408-120">CommonParameters</span></span>
<span data-ttu-id="91408-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91408-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91408-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91408-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91408-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91408-123">INPUTS</span></span>

## <span data-ttu-id="91408-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91408-124">OUTPUTS</span></span>

## <span data-ttu-id="91408-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91408-125">NOTES</span></span>

## <span data-ttu-id="91408-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91408-126">RELATED LINKS</span></span>

[<span data-ttu-id="91408-127">Nowe — AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="91408-127">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="91408-128">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="91408-128">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="91408-129">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="91408-129">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="91408-130">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="91408-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


