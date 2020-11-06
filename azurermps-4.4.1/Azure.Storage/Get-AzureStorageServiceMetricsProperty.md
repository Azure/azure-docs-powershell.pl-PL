---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f3930216e93f13004d7d2e8b149867cf511e3708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525865"
---
# <span data-ttu-id="6a62c-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6a62c-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="6a62c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a62c-102">SYNOPSIS</span></span>
<span data-ttu-id="6a62c-103">Pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6a62c-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a62c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a62c-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="6a62c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a62c-105">DESCRIPTION</span></span>
<span data-ttu-id="6a62c-106">Polecenie cmdlet **Get-AzureStorageServiceMetricsProperty** pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6a62c-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="6a62c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a62c-107">EXAMPLES</span></span>

### <span data-ttu-id="6a62c-108">Przykład 1: uzyskiwanie właściwości metryk dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="6a62c-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="6a62c-109">To polecenie pobiera właściwości metryk magazynu obiektów BLOB dla typu metryki godzinowych.</span><span class="sxs-lookup"><span data-stu-id="6a62c-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="6a62c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a62c-110">PARAMETERS</span></span>

### <span data-ttu-id="6a62c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6a62c-111">-Context</span></span>
<span data-ttu-id="6a62c-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6a62c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6a62c-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6a62c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6a62c-114">-Metryki</span><span class="sxs-lookup"><span data-stu-id="6a62c-114">-MetricsType</span></span>
<span data-ttu-id="6a62c-115">Określa typ metryk.</span><span class="sxs-lookup"><span data-stu-id="6a62c-115">Specifies a metrics type.</span></span>
<span data-ttu-id="6a62c-116">To polecenie cmdlet umożliwia pobieranie właściwości metryki usługi Azure Storage dla typu metryki, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6a62c-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="6a62c-117">Dopuszczalne wartości tego parametru to: godzina i minuta.</span><span class="sxs-lookup"><span data-stu-id="6a62c-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="6a62c-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6a62c-118">-ServiceType</span></span>
<span data-ttu-id="6a62c-119">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="6a62c-119">Specifies the storage service type.</span></span>
<span data-ttu-id="6a62c-120">To polecenie cmdlet pobiera właściwości metryk dla typu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6a62c-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="6a62c-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6a62c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a62c-122">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="6a62c-122">Blob</span></span> 
- <span data-ttu-id="6a62c-123">Tworząc</span><span class="sxs-lookup"><span data-stu-id="6a62c-123">Table</span></span>
- <span data-ttu-id="6a62c-124">Wykonany</span><span class="sxs-lookup"><span data-stu-id="6a62c-124">Queue</span></span>
- <span data-ttu-id="6a62c-125">Plik</span><span class="sxs-lookup"><span data-stu-id="6a62c-125">File</span></span> 

<span data-ttu-id="6a62c-126">Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="6a62c-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="6a62c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a62c-127">CommonParameters</span></span>
<span data-ttu-id="6a62c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a62c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a62c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a62c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a62c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a62c-130">INPUTS</span></span>

### <span data-ttu-id="6a62c-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6a62c-131">IStorageContext</span></span>

<span data-ttu-id="6a62c-132">Parametr "context" przyjmuje wartość typu "IStorageContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="6a62c-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="6a62c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a62c-133">OUTPUTS</span></span>

### <span data-ttu-id="6a62c-134">Microsoft. platformy windowsazure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="6a62c-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="6a62c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a62c-135">NOTES</span></span>

## <span data-ttu-id="6a62c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a62c-136">RELATED LINKS</span></span>

[<span data-ttu-id="6a62c-137">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="6a62c-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="6a62c-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6a62c-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


