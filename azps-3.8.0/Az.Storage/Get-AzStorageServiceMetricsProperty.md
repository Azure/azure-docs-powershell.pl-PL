---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051248"
---
# <span data-ttu-id="9937c-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9937c-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="9937c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9937c-102">SYNOPSIS</span></span>
<span data-ttu-id="9937c-103">Pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9937c-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="9937c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9937c-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9937c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9937c-105">DESCRIPTION</span></span>
<span data-ttu-id="9937c-106">Polecenie cmdlet **Get-AzStorageServiceMetricsProperty** pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9937c-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="9937c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9937c-107">EXAMPLES</span></span>

### <span data-ttu-id="9937c-108">Przykład 1: uzyskiwanie właściwości metryk dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="9937c-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="9937c-109">To polecenie pobiera właściwości metryk magazynu obiektów BLOB dla typu metryki godzinowych.</span><span class="sxs-lookup"><span data-stu-id="9937c-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="9937c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9937c-110">PARAMETERS</span></span>

### <span data-ttu-id="9937c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9937c-111">-Context</span></span>
<span data-ttu-id="9937c-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9937c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9937c-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9937c-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9937c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9937c-114">-DefaultProfile</span></span>
<span data-ttu-id="9937c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9937c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9937c-116">-Metryki</span><span class="sxs-lookup"><span data-stu-id="9937c-116">-MetricsType</span></span>
<span data-ttu-id="9937c-117">Określa typ metryk.</span><span class="sxs-lookup"><span data-stu-id="9937c-117">Specifies a metrics type.</span></span>
<span data-ttu-id="9937c-118">To polecenie cmdlet umożliwia pobieranie właściwości metryki usługi Azure Storage dla typu metryki, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9937c-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="9937c-119">Dopuszczalne wartości tego parametru to: godzina i minuta.</span><span class="sxs-lookup"><span data-stu-id="9937c-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9937c-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="9937c-120">-ServiceType</span></span>
<span data-ttu-id="9937c-121">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="9937c-121">Specifies the storage service type.</span></span>
<span data-ttu-id="9937c-122">To polecenie cmdlet pobiera właściwości metryk dla typu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9937c-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="9937c-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9937c-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9937c-124">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="9937c-124">Blob</span></span> 
- <span data-ttu-id="9937c-125">Tworząc</span><span class="sxs-lookup"><span data-stu-id="9937c-125">Table</span></span>
- <span data-ttu-id="9937c-126">Wykonany</span><span class="sxs-lookup"><span data-stu-id="9937c-126">Queue</span></span>
- <span data-ttu-id="9937c-127">Plik wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="9937c-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="9937c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9937c-128">CommonParameters</span></span>
<span data-ttu-id="9937c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9937c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9937c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9937c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9937c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9937c-131">INPUTS</span></span>

### <span data-ttu-id="9937c-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9937c-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9937c-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9937c-133">OUTPUTS</span></span>

### <span data-ttu-id="9937c-134">Microsoft. Azure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="9937c-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="9937c-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9937c-135">NOTES</span></span>

## <span data-ttu-id="9937c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9937c-136">RELATED LINKS</span></span>

[<span data-ttu-id="9937c-137">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9937c-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="9937c-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9937c-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


