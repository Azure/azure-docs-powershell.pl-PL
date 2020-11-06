---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524009"
---
# <span data-ttu-id="bb97f-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="bb97f-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="bb97f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb97f-102">SYNOPSIS</span></span>
<span data-ttu-id="bb97f-103">Pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bb97f-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="bb97f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb97f-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="bb97f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb97f-105">DESCRIPTION</span></span>
<span data-ttu-id="bb97f-106">Polecenie cmdlet **Get-AzureStorageServiceMetricsProperty** pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bb97f-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="bb97f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb97f-107">EXAMPLES</span></span>

### <span data-ttu-id="bb97f-108">Przykład 1: uzyskiwanie właściwości metryk dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="bb97f-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="bb97f-109">To polecenie pobiera właściwości metryk magazynu obiektów BLOB dla typu metryki godzinowych.</span><span class="sxs-lookup"><span data-stu-id="bb97f-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="bb97f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb97f-110">PARAMETERS</span></span>

### <span data-ttu-id="bb97f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="bb97f-111">-Context</span></span>
<span data-ttu-id="bb97f-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="bb97f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bb97f-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bb97f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bb97f-114">-Metryki</span><span class="sxs-lookup"><span data-stu-id="bb97f-114">-MetricsType</span></span>
<span data-ttu-id="bb97f-115">Określa typ metryk.</span><span class="sxs-lookup"><span data-stu-id="bb97f-115">Specifies a metrics type.</span></span>
<span data-ttu-id="bb97f-116">To polecenie cmdlet umożliwia pobieranie właściwości metryki usługi Azure Storage dla typu metryki, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="bb97f-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="bb97f-117">Dopuszczalne wartości tego parametru to: godzina i minuta.</span><span class="sxs-lookup"><span data-stu-id="bb97f-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="bb97f-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bb97f-118">-ServiceType</span></span>
<span data-ttu-id="bb97f-119">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="bb97f-119">Specifies the storage service type.</span></span>
<span data-ttu-id="bb97f-120">To polecenie cmdlet pobiera właściwości metryk dla typu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bb97f-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="bb97f-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bb97f-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bb97f-122">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="bb97f-122">Blob</span></span> 
- <span data-ttu-id="bb97f-123">Tworząc</span><span class="sxs-lookup"><span data-stu-id="bb97f-123">Table</span></span>
- <span data-ttu-id="bb97f-124">Wykonany</span><span class="sxs-lookup"><span data-stu-id="bb97f-124">Queue</span></span>
- <span data-ttu-id="bb97f-125">Plik</span><span class="sxs-lookup"><span data-stu-id="bb97f-125">File</span></span> 

<span data-ttu-id="bb97f-126">Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="bb97f-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="bb97f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb97f-127">CommonParameters</span></span>
<span data-ttu-id="bb97f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb97f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb97f-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb97f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb97f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb97f-130">INPUTS</span></span>

## <span data-ttu-id="bb97f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb97f-131">OUTPUTS</span></span>

## <span data-ttu-id="bb97f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb97f-132">NOTES</span></span>

## <span data-ttu-id="bb97f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb97f-133">RELATED LINKS</span></span>

[<span data-ttu-id="bb97f-134">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bb97f-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bb97f-135">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="bb97f-135">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


