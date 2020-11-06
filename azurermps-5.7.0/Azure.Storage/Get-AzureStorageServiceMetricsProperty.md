---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 9d7e8f5d69d2f0e570cd7ce7fb21b29eb7f11648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545911"
---
# <span data-ttu-id="9ce28-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9ce28-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="9ce28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ce28-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce28-103">Pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9ce28-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ce28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ce28-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="9ce28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9ce28-105">DESCRIPTION</span></span>
<span data-ttu-id="9ce28-106">Polecenie cmdlet **Get-AzureStorageServiceMetricsProperty** pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9ce28-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="9ce28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ce28-107">EXAMPLES</span></span>

### <span data-ttu-id="9ce28-108">Przykład 1: uzyskiwanie właściwości metryk dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="9ce28-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="9ce28-109">To polecenie pobiera właściwości metryk magazynu obiektów BLOB dla typu metryki godzinowych.</span><span class="sxs-lookup"><span data-stu-id="9ce28-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="9ce28-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ce28-110">PARAMETERS</span></span>

### <span data-ttu-id="9ce28-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9ce28-111">-Context</span></span>
<span data-ttu-id="9ce28-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9ce28-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9ce28-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9ce28-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9ce28-114">-Metryki</span><span class="sxs-lookup"><span data-stu-id="9ce28-114">-MetricsType</span></span>
<span data-ttu-id="9ce28-115">Określa typ metryk.</span><span class="sxs-lookup"><span data-stu-id="9ce28-115">Specifies a metrics type.</span></span>
<span data-ttu-id="9ce28-116">To polecenie cmdlet umożliwia pobieranie właściwości metryki usługi Azure Storage dla typu metryki, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9ce28-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="9ce28-117">Dopuszczalne wartości tego parametru to: godzina i minuta.</span><span class="sxs-lookup"><span data-stu-id="9ce28-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce28-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="9ce28-118">-ServiceType</span></span>
<span data-ttu-id="9ce28-119">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="9ce28-119">Specifies the storage service type.</span></span>
<span data-ttu-id="9ce28-120">To polecenie cmdlet pobiera właściwości metryk dla typu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9ce28-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="9ce28-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9ce28-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ce28-122">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="9ce28-122">Blob</span></span> 
- <span data-ttu-id="9ce28-123">Tworząc</span><span class="sxs-lookup"><span data-stu-id="9ce28-123">Table</span></span>
- <span data-ttu-id="9ce28-124">Wykonany</span><span class="sxs-lookup"><span data-stu-id="9ce28-124">Queue</span></span>
- <span data-ttu-id="9ce28-125">Plik</span><span class="sxs-lookup"><span data-stu-id="9ce28-125">File</span></span> 

<span data-ttu-id="9ce28-126">Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="9ce28-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="9ce28-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce28-127">CommonParameters</span></span>
<span data-ttu-id="9ce28-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce28-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce28-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ce28-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce28-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ce28-130">INPUTS</span></span>

### <span data-ttu-id="9ce28-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ce28-131">IStorageContext</span></span>

<span data-ttu-id="9ce28-132">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="9ce28-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="9ce28-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ce28-133">OUTPUTS</span></span>

### <span data-ttu-id="9ce28-134">Microsoft. platformy windowsazure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="9ce28-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="9ce28-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ce28-135">NOTES</span></span>

## <span data-ttu-id="9ce28-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ce28-136">RELATED LINKS</span></span>

[<span data-ttu-id="9ce28-137">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ce28-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9ce28-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9ce28-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


