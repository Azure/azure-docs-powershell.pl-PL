---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: 28727ed903030c360b436edfac3d4cfb2a5d38ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545907"
---
# <span data-ttu-id="1b2c6-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1b2c6-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="1b2c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b2c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2c6-103">Pobiera właściwości usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="1b2c6-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b2c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b2c6-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b2c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b2c6-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2c6-106">Polecenie cmdlet **Get-AzureStorageServiceProperty** pobiera właściwości usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="1b2c6-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="1b2c6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b2c6-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2c6-108">Przykład 1: pobieranie właściwości usług Azure Storage Services w usłudze BLOB</span><span class="sxs-lookup"><span data-stu-id="1b2c6-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29

```

<span data-ttu-id="1b2c6-109">To polecenie pobiera właściwość DefaultServiceVersion usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="1b2c6-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="1b2c6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b2c6-110">PARAMETERS</span></span>

### <span data-ttu-id="1b2c6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1b2c6-111">-Context</span></span>
<span data-ttu-id="1b2c6-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="1b2c6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1b2c6-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b2c6-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1b2c6-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="1b2c6-114">-ServiceType</span></span>
<span data-ttu-id="1b2c6-115">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="1b2c6-115">Specifies the storage service type.</span></span>
<span data-ttu-id="1b2c6-116">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1b2c6-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="1b2c6-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1b2c6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b2c6-118">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="1b2c6-118">Blob</span></span> 
- <span data-ttu-id="1b2c6-119">Tworząc</span><span class="sxs-lookup"><span data-stu-id="1b2c6-119">Table</span></span>
- <span data-ttu-id="1b2c6-120">Wykonany</span><span class="sxs-lookup"><span data-stu-id="1b2c6-120">Queue</span></span>
- <span data-ttu-id="1b2c6-121">Plik</span><span class="sxs-lookup"><span data-stu-id="1b2c6-121">File</span></span>

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

### <span data-ttu-id="1b2c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2c6-122">CommonParameters</span></span>
<span data-ttu-id="1b2c6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b2c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2c6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b2c6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2c6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b2c6-125">INPUTS</span></span>

### <span data-ttu-id="1b2c6-126">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b2c6-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1b2c6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b2c6-127">OUTPUTS</span></span>

### <span data-ttu-id="1b2c6-128">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="1b2c6-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="1b2c6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b2c6-129">NOTES</span></span>

## <span data-ttu-id="1b2c6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b2c6-130">RELATED LINKS</span></span>

