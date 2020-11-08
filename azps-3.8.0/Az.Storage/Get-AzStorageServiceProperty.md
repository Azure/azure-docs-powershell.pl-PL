---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051246"
---
# <span data-ttu-id="d293d-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d293d-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="d293d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d293d-102">SYNOPSIS</span></span>
<span data-ttu-id="d293d-103">Pobiera właściwości usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="d293d-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="d293d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d293d-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d293d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d293d-105">DESCRIPTION</span></span>
<span data-ttu-id="d293d-106">Polecenie cmdlet **Get-AzStorageServiceProperty** pobiera właściwości usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="d293d-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="d293d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d293d-107">EXAMPLES</span></span>

### <span data-ttu-id="d293d-108">Przykład 1: pobieranie właściwości usług Azure Storage Services w usłudze BLOB</span><span class="sxs-lookup"><span data-stu-id="d293d-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

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

<span data-ttu-id="d293d-109">To polecenie pobiera właściwość DefaultServiceVersion usługi BLOB.</span><span class="sxs-lookup"><span data-stu-id="d293d-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="d293d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d293d-110">PARAMETERS</span></span>

### <span data-ttu-id="d293d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d293d-111">-Context</span></span>
<span data-ttu-id="d293d-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d293d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d293d-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d293d-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d293d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d293d-114">-DefaultProfile</span></span>
<span data-ttu-id="d293d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d293d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d293d-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d293d-116">-ServiceType</span></span>
<span data-ttu-id="d293d-117">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="d293d-117">Specifies the storage service type.</span></span>
<span data-ttu-id="d293d-118">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d293d-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="d293d-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d293d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d293d-120">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="d293d-120">Blob</span></span> 
- <span data-ttu-id="d293d-121">Tworząc</span><span class="sxs-lookup"><span data-stu-id="d293d-121">Table</span></span>
- <span data-ttu-id="d293d-122">Wykonany</span><span class="sxs-lookup"><span data-stu-id="d293d-122">Queue</span></span>
- <span data-ttu-id="d293d-123">Plik</span><span class="sxs-lookup"><span data-stu-id="d293d-123">File</span></span>

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

### <span data-ttu-id="d293d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d293d-124">CommonParameters</span></span>
<span data-ttu-id="d293d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d293d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d293d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d293d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d293d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d293d-127">INPUTS</span></span>

### <span data-ttu-id="d293d-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d293d-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d293d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d293d-129">OUTPUTS</span></span>

### <span data-ttu-id="d293d-130">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="d293d-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="d293d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d293d-131">NOTES</span></span>

## <span data-ttu-id="d293d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d293d-132">RELATED LINKS</span></span>
