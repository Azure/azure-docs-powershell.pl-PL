---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: b622f117549a77c54a24964240cd6d17a084993d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717293"
---
# <span data-ttu-id="86667-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="86667-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="86667-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86667-102">SYNOPSIS</span></span>
<span data-ttu-id="86667-103">Pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="86667-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86667-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86667-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86667-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86667-105">DESCRIPTION</span></span>
<span data-ttu-id="86667-106">Polecenie cmdlet **Get-AzureStorageServiceLoggingProperty** pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="86667-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="86667-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86667-107">EXAMPLES</span></span>

### <span data-ttu-id="86667-108">Przykład 1: uzyskiwanie właściwości rejestrowania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="86667-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="86667-109">To polecenie pobiera właściwości rejestrowania dla magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="86667-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="86667-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86667-110">PARAMETERS</span></span>

### <span data-ttu-id="86667-111">-Context</span><span class="sxs-lookup"><span data-stu-id="86667-111">-Context</span></span>
<span data-ttu-id="86667-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="86667-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="86667-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="86667-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="86667-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86667-114">-DefaultProfile</span></span>
<span data-ttu-id="86667-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86667-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86667-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="86667-116">-ServiceType</span></span>
<span data-ttu-id="86667-117">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="86667-117">Specifies the storage service type.</span></span>
<span data-ttu-id="86667-118">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="86667-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="86667-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="86667-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="86667-120">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="86667-120">Blob</span></span> 
- <span data-ttu-id="86667-121">Tworząc</span><span class="sxs-lookup"><span data-stu-id="86667-121">Table</span></span>
- <span data-ttu-id="86667-122">Wykonany</span><span class="sxs-lookup"><span data-stu-id="86667-122">Queue</span></span>
- <span data-ttu-id="86667-123">Plik wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="86667-123">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86667-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86667-124">CommonParameters</span></span>
<span data-ttu-id="86667-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86667-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86667-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86667-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86667-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86667-127">INPUTS</span></span>

### <span data-ttu-id="86667-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="86667-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="86667-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86667-129">OUTPUTS</span></span>

### <span data-ttu-id="86667-130">Microsoft. platformy windowsazure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="86667-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="86667-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86667-131">NOTES</span></span>

## <span data-ttu-id="86667-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86667-132">RELATED LINKS</span></span>

[<span data-ttu-id="86667-133">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="86667-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="86667-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="86667-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


