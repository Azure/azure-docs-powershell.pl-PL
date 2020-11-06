---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ba1759d9efb1c5e624b1ced5cddd03ee79917c4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545875"
---
# <span data-ttu-id="2a698-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a698-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="2a698-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a698-102">SYNOPSIS</span></span>
<span data-ttu-id="2a698-103">Tworzy zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a698-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a698-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a698-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="2a698-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2a698-105">DESCRIPTION</span></span>
<span data-ttu-id="2a698-106">Polecenie cmdlet **New-AzureStorageQueueStoredAccessPolicy** tworzy zapisane zasady dostępu dla kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a698-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="2a698-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a698-107">EXAMPLES</span></span>

### <span data-ttu-id="2a698-108">Przykład 1. Tworzenie zapisanych zasad dostępu w kolejce magazynu</span><span class="sxs-lookup"><span data-stu-id="2a698-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="2a698-109">To polecenie tworzy zasady dostępu o nazwie Policy01 w kolejce magazynu o nazwie Moja kolejka.</span><span class="sxs-lookup"><span data-stu-id="2a698-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="2a698-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a698-110">PARAMETERS</span></span>

### <span data-ttu-id="2a698-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2a698-111">-Context</span></span>
<span data-ttu-id="2a698-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2a698-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2a698-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2a698-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2a698-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2a698-114">-ExpiryTime</span></span>
<span data-ttu-id="2a698-115">Określa godzinę, o której zapisane zasady dostępu staną się nieprawidłowe.</span><span class="sxs-lookup"><span data-stu-id="2a698-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a698-116">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="2a698-116">-Permission</span></span>
<span data-ttu-id="2a698-117">Określa uprawnienia w przechowywanych zasadach dostępu w celu uzyskiwania dostępu do kolejki magazynu.</span><span class="sxs-lookup"><span data-stu-id="2a698-117">Specifies permissions in the stored access policy to access the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a698-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="2a698-118">-Policy</span></span>
<span data-ttu-id="2a698-119">Określa nazwę przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="2a698-119">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a698-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="2a698-120">-Queue</span></span>
<span data-ttu-id="2a698-121">Określa nazwę kolejki magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a698-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="2a698-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2a698-122">-StartTime</span></span>
<span data-ttu-id="2a698-123">Określa czas ważności przechowywanych zasad dostępu.</span><span class="sxs-lookup"><span data-stu-id="2a698-123">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a698-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a698-124">CommonParameters</span></span>
<span data-ttu-id="2a698-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a698-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a698-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a698-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a698-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a698-127">INPUTS</span></span>

### <span data-ttu-id="2a698-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2a698-128">IStorageContext</span></span>

<span data-ttu-id="2a698-129">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="2a698-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="2a698-130">Ciąg</span><span class="sxs-lookup"><span data-stu-id="2a698-130">String</span></span>

<span data-ttu-id="2a698-131">Parametr "queue" przyjmuje wartość typu "String" z procesu</span><span class="sxs-lookup"><span data-stu-id="2a698-131">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2a698-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a698-132">OUTPUTS</span></span>

### <span data-ttu-id="2a698-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2a698-133">System.String</span></span>

## <span data-ttu-id="2a698-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a698-134">NOTES</span></span>

## <span data-ttu-id="2a698-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a698-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a698-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a698-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2a698-137">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2a698-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2a698-138">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a698-138">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2a698-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a698-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


