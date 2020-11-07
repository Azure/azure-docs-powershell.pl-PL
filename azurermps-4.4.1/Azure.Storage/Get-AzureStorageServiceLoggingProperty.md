---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: a3981ba2b0759afec06bb4cf34bc1e086658765a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716554"
---
# <span data-ttu-id="1aabc-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1aabc-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="1aabc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1aabc-102">SYNOPSIS</span></span>
<span data-ttu-id="1aabc-103">Pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="1aabc-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aabc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1aabc-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="1aabc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1aabc-105">DESCRIPTION</span></span>
<span data-ttu-id="1aabc-106">Polecenie cmdlet **Get-AzureStorageServiceLoggingProperty** pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="1aabc-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="1aabc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1aabc-107">EXAMPLES</span></span>

### <span data-ttu-id="1aabc-108">Przykład 1: uzyskiwanie właściwości rejestrowania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="1aabc-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="1aabc-109">To polecenie pobiera właściwości rejestrowania dla magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="1aabc-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="1aabc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1aabc-110">PARAMETERS</span></span>

### <span data-ttu-id="1aabc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1aabc-111">-Context</span></span>
<span data-ttu-id="1aabc-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1aabc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1aabc-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1aabc-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1aabc-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="1aabc-114">-ServiceType</span></span>
<span data-ttu-id="1aabc-115">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="1aabc-115">Specifies the storage service type.</span></span>
<span data-ttu-id="1aabc-116">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1aabc-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="1aabc-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1aabc-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1aabc-118">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="1aabc-118">Blob</span></span> 
- <span data-ttu-id="1aabc-119">Tworząc</span><span class="sxs-lookup"><span data-stu-id="1aabc-119">Table</span></span>
- <span data-ttu-id="1aabc-120">Wykonany</span><span class="sxs-lookup"><span data-stu-id="1aabc-120">Queue</span></span>
- <span data-ttu-id="1aabc-121">Plik</span><span class="sxs-lookup"><span data-stu-id="1aabc-121">File</span></span>

<span data-ttu-id="1aabc-122">Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="1aabc-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="1aabc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aabc-123">CommonParameters</span></span>
<span data-ttu-id="1aabc-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aabc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aabc-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aabc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aabc-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1aabc-126">INPUTS</span></span>

### <span data-ttu-id="1aabc-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1aabc-127">IStorageContext</span></span>

<span data-ttu-id="1aabc-128">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="1aabc-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="1aabc-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1aabc-129">OUTPUTS</span></span>

### <span data-ttu-id="1aabc-130">Microsoft. platformy windowsazure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="1aabc-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="1aabc-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1aabc-131">NOTES</span></span>

## <span data-ttu-id="1aabc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1aabc-132">RELATED LINKS</span></span>

[<span data-ttu-id="1aabc-133">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1aabc-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1aabc-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1aabc-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


