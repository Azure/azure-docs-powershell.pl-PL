---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceProperty.md
ms.openlocfilehash: a36b1f13f08cd94339f9791512d764a872019672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547803"
---
# <span data-ttu-id="a7d3f-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a7d3f-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="a7d3f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a7d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d3f-103">Pobiera właściwości usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="a7d3f-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7d3f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a7d3f-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d3f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a7d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d3f-106">Polecenie cmdlet **Get-AzureStorageServiceProperty** pobiera właściwości usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="a7d3f-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="a7d3f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a7d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d3f-108">Przykład 1: pobieranie właściwości usług Azure Storage Services w usłudze BLOB</span><span class="sxs-lookup"><span data-stu-id="a7d3f-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="a7d3f-109">To polecenie pobiera właściwość DefaultServiceVersion usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="a7d3f-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="a7d3f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a7d3f-110">PARAMETERS</span></span>

### <span data-ttu-id="a7d3f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a7d3f-111">-Context</span></span>
<span data-ttu-id="a7d3f-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a7d3f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a7d3f-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a7d3f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a7d3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d3f-114">-DefaultProfile</span></span>
<span data-ttu-id="a7d3f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d3f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d3f-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a7d3f-116">-ServiceType</span></span>
<span data-ttu-id="a7d3f-117">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="a7d3f-117">Specifies the storage service type.</span></span>
<span data-ttu-id="a7d3f-118">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a7d3f-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="a7d3f-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a7d3f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a7d3f-120">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="a7d3f-120">Blob</span></span> 
- <span data-ttu-id="a7d3f-121">Tworząc</span><span class="sxs-lookup"><span data-stu-id="a7d3f-121">Table</span></span>
- <span data-ttu-id="a7d3f-122">Wykonany</span><span class="sxs-lookup"><span data-stu-id="a7d3f-122">Queue</span></span>
- <span data-ttu-id="a7d3f-123">Plik</span><span class="sxs-lookup"><span data-stu-id="a7d3f-123">File</span></span>

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

### <span data-ttu-id="a7d3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d3f-124">CommonParameters</span></span>
<span data-ttu-id="a7d3f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d3f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d3f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d3f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a7d3f-127">INPUTS</span></span>

### <span data-ttu-id="a7d3f-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7d3f-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a7d3f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a7d3f-129">OUTPUTS</span></span>

### <span data-ttu-id="a7d3f-130">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="a7d3f-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="a7d3f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a7d3f-131">NOTES</span></span>

## <span data-ttu-id="a7d3f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a7d3f-132">RELATED LINKS</span></span>
