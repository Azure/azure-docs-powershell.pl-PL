---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 7bca28da7b4729a414fafc5268bc4e0e02ee3c72
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892210"
---
# <span data-ttu-id="a2d9e-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a2d9e-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="a2d9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d9e-103">Pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="a2d9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2d9e-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2d9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a2d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="a2d9e-106">Polecenie cmdlet **Get-AzStorageServiceMetricsProperty** pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="a2d9e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2d9e-107">EXAMPLES</span></span>

### <span data-ttu-id="a2d9e-108">Przykład 1: uzyskiwanie właściwości metryk dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="a2d9e-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="a2d9e-109">To polecenie pobiera właściwości metryk magazynu obiektów BLOB dla typu metryki godzinowych.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="a2d9e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2d9e-110">PARAMETERS</span></span>

### <span data-ttu-id="a2d9e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a2d9e-111">-Context</span></span>
<span data-ttu-id="a2d9e-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a2d9e-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a2d9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d9e-114">-DefaultProfile</span></span>
<span data-ttu-id="a2d9e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2d9e-116">-Metryki</span><span class="sxs-lookup"><span data-stu-id="a2d9e-116">-MetricsType</span></span>
<span data-ttu-id="a2d9e-117">Określa typ metryk.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-117">Specifies a metrics type.</span></span>
<span data-ttu-id="a2d9e-118">To polecenie cmdlet umożliwia pobieranie właściwości metryki usługi Azure Storage dla typu metryki, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="a2d9e-119">Dopuszczalne wartości tego parametru to: godzina i minuta.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="a2d9e-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a2d9e-120">-ServiceType</span></span>
<span data-ttu-id="a2d9e-121">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-121">Specifies the storage service type.</span></span>
<span data-ttu-id="a2d9e-122">To polecenie cmdlet pobiera właściwości metryk dla typu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="a2d9e-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a2d9e-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a2d9e-124">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="a2d9e-124">Blob</span></span> 
- <span data-ttu-id="a2d9e-125">Tworząc</span><span class="sxs-lookup"><span data-stu-id="a2d9e-125">Table</span></span>
- <span data-ttu-id="a2d9e-126">Wykonany</span><span class="sxs-lookup"><span data-stu-id="a2d9e-126">Queue</span></span>
- <span data-ttu-id="a2d9e-127">Plik wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="a2d9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d9e-128">CommonParameters</span></span>
<span data-ttu-id="a2d9e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d9e-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d9e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d9e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2d9e-131">INPUTS</span></span>

### <span data-ttu-id="a2d9e-132">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2d9e-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a2d9e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2d9e-133">OUTPUTS</span></span>

### <span data-ttu-id="a2d9e-134">Microsoft. WindowsAz. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="a2d9e-134">Microsoft.WindowsAz.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="a2d9e-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2d9e-135">NOTES</span></span>

## <span data-ttu-id="a2d9e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2d9e-136">RELATED LINKS</span></span>

[<span data-ttu-id="a2d9e-137">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2d9e-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a2d9e-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a2d9e-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


