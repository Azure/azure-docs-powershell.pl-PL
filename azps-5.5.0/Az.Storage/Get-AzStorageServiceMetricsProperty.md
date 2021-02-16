---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176610"
---
# <span data-ttu-id="e9985-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e9985-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="e9985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9985-102">SYNOPSIS</span></span>
<span data-ttu-id="e9985-103">Pobiera właściwości metryk dla usługi magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9985-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="e9985-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e9985-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9985-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e9985-105">DESCRIPTION</span></span>
<span data-ttu-id="e9985-106">Polecenie **cmdlet Get-AzStorageServiceMetricsProperty** pobiera właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e9985-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="e9985-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e9985-107">EXAMPLES</span></span>

### <span data-ttu-id="e9985-108">Przykład 1. Uzyskiwanie właściwości metryk dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="e9985-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="e9985-109">To polecenie pobiera właściwości metryk dla magazynu obiektów blob dla typu metryk Godzina.</span><span class="sxs-lookup"><span data-stu-id="e9985-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="e9985-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9985-110">PARAMETERS</span></span>

### <span data-ttu-id="e9985-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e9985-111">-Context</span></span>
<span data-ttu-id="e9985-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9985-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e9985-113">Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9985-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e9985-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9985-114">-DefaultProfile</span></span>
<span data-ttu-id="e9985-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9985-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9985-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="e9985-116">-MetricsType</span></span>
<span data-ttu-id="e9985-117">Określa typ metryki.</span><span class="sxs-lookup"><span data-stu-id="e9985-117">Specifies a metrics type.</span></span>
<span data-ttu-id="e9985-118">To polecenie cmdlet pobiera właściwości metryk usługi Azure Storage dla typu metryk, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e9985-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="e9985-119">Dopuszczalne wartości dla tego parametru to: Godzina i Minuta.</span><span class="sxs-lookup"><span data-stu-id="e9985-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="e9985-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e9985-120">-ServiceType</span></span>
<span data-ttu-id="e9985-121">Określa typ usługi magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e9985-121">Specifies the storage service type.</span></span>
<span data-ttu-id="e9985-122">To polecenie cmdlet pobiera właściwości metryk dla typu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e9985-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="e9985-123">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e9985-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e9985-124">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="e9985-124">Blob</span></span> 
- <span data-ttu-id="e9985-125">Tabela</span><span class="sxs-lookup"><span data-stu-id="e9985-125">Table</span></span>
- <span data-ttu-id="e9985-126">Kolejka</span><span class="sxs-lookup"><span data-stu-id="e9985-126">Queue</span></span>
- <span data-ttu-id="e9985-127">Plik Wartość Pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="e9985-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="e9985-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9985-128">CommonParameters</span></span>
<span data-ttu-id="e9985-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9985-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9985-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9985-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9985-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9985-131">INPUTS</span></span>

### <span data-ttu-id="e9985-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9985-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e9985-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9985-133">OUTPUTS</span></span>

### <span data-ttu-id="e9985-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="e9985-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="e9985-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e9985-135">NOTES</span></span>

## <span data-ttu-id="e9985-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9985-136">RELATED LINKS</span></span>

[<span data-ttu-id="e9985-137">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9985-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="e9985-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e9985-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


