---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: f43386ff1eca223e8ff0e1e8ea7a07d1d8e25d0d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897726"
---
# <span data-ttu-id="38b86-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="38b86-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="38b86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38b86-102">SYNOPSIS</span></span>
<span data-ttu-id="38b86-103">Pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="38b86-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38b86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38b86-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38b86-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38b86-105">DESCRIPTION</span></span>
<span data-ttu-id="38b86-106">Polecenie cmdlet **Get-AzureStorageServiceLoggingProperty** pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="38b86-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="38b86-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38b86-107">EXAMPLES</span></span>

### <span data-ttu-id="38b86-108">Przykład 1: uzyskiwanie właściwości rejestrowania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="38b86-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="38b86-109">To polecenie pobiera właściwości rejestrowania dla magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="38b86-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="38b86-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38b86-110">PARAMETERS</span></span>

### <span data-ttu-id="38b86-111">-Context</span><span class="sxs-lookup"><span data-stu-id="38b86-111">-Context</span></span>
<span data-ttu-id="38b86-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="38b86-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="38b86-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="38b86-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="38b86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b86-114">-DefaultProfile</span></span>
<span data-ttu-id="38b86-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38b86-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b86-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="38b86-116">-ServiceType</span></span>
<span data-ttu-id="38b86-117">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="38b86-117">Specifies the storage service type.</span></span>
<span data-ttu-id="38b86-118">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="38b86-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="38b86-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="38b86-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38b86-120">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="38b86-120">Blob</span></span> 
- <span data-ttu-id="38b86-121">Tworząc</span><span class="sxs-lookup"><span data-stu-id="38b86-121">Table</span></span>
- <span data-ttu-id="38b86-122">Wykonany</span><span class="sxs-lookup"><span data-stu-id="38b86-122">Queue</span></span>
- <span data-ttu-id="38b86-123">Plik wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="38b86-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="38b86-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b86-124">CommonParameters</span></span>
<span data-ttu-id="38b86-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b86-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b86-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b86-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b86-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38b86-127">INPUTS</span></span>

### <span data-ttu-id="38b86-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="38b86-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="38b86-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38b86-129">OUTPUTS</span></span>

### <span data-ttu-id="38b86-130">Microsoft. platformy windowsazure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="38b86-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="38b86-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38b86-131">NOTES</span></span>

## <span data-ttu-id="38b86-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38b86-132">RELATED LINKS</span></span>

[<span data-ttu-id="38b86-133">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="38b86-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="38b86-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="38b86-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


