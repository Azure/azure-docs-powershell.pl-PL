---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: d0edbcc3b519f9600a2ad36832dee0305ce49be7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542771"
---
# <span data-ttu-id="ffc9c-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ffc9c-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="ffc9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc9c-103">Pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="ffc9c-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffc9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffc9c-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="ffc9c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ffc9c-105">DESCRIPTION</span></span>
<span data-ttu-id="ffc9c-106">Polecenie cmdlet **Get-AzureStorageServiceLoggingProperty** pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="ffc9c-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="ffc9c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffc9c-107">EXAMPLES</span></span>

### <span data-ttu-id="ffc9c-108">Przykład 1: uzyskiwanie właściwości rejestrowania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="ffc9c-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="ffc9c-109">To polecenie pobiera właściwości rejestrowania dla magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="ffc9c-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="ffc9c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffc9c-110">PARAMETERS</span></span>

### <span data-ttu-id="ffc9c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ffc9c-111">-Context</span></span>
<span data-ttu-id="ffc9c-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="ffc9c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ffc9c-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ffc9c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ffc9c-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ffc9c-114">-ServiceType</span></span>
<span data-ttu-id="ffc9c-115">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="ffc9c-115">Specifies the storage service type.</span></span>
<span data-ttu-id="ffc9c-116">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="ffc9c-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ffc9c-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ffc9c-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ffc9c-118">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="ffc9c-118">Blob</span></span> 
- <span data-ttu-id="ffc9c-119">Tworząc</span><span class="sxs-lookup"><span data-stu-id="ffc9c-119">Table</span></span>
- <span data-ttu-id="ffc9c-120">Wykonany</span><span class="sxs-lookup"><span data-stu-id="ffc9c-120">Queue</span></span>
- <span data-ttu-id="ffc9c-121">Plik</span><span class="sxs-lookup"><span data-stu-id="ffc9c-121">File</span></span>

<span data-ttu-id="ffc9c-122">Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="ffc9c-122">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc9c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc9c-123">CommonParameters</span></span>
<span data-ttu-id="ffc9c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc9c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc9c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc9c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc9c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffc9c-126">INPUTS</span></span>

### <span data-ttu-id="ffc9c-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ffc9c-127">IStorageContext</span></span>

<span data-ttu-id="ffc9c-128">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="ffc9c-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="ffc9c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffc9c-129">OUTPUTS</span></span>

### <span data-ttu-id="ffc9c-130">Microsoft. platformy windowsazure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="ffc9c-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="ffc9c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffc9c-131">NOTES</span></span>

## <span data-ttu-id="ffc9c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffc9c-132">RELATED LINKS</span></span>

[<span data-ttu-id="ffc9c-133">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ffc9c-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ffc9c-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ffc9c-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


