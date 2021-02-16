---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178187"
---
# <span data-ttu-id="d1978-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d1978-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="d1978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1978-102">SYNOPSIS</span></span>
<span data-ttu-id="d1978-103">Pobiera właściwości usług magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1978-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="d1978-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1978-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1978-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1978-105">DESCRIPTION</span></span>
<span data-ttu-id="d1978-106">Polecenie **cmdlet Get-AzStorageServiceProperty** otrzymuje właściwości usług magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1978-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="d1978-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1978-107">EXAMPLES</span></span>

### <span data-ttu-id="d1978-108">Przykład 1. Pobierz właściwość usług Azure Storage usługi blob</span><span class="sxs-lookup"><span data-stu-id="d1978-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="d1978-109">To polecenie pobiera właściwość DefaultServiceVersion usługi blob.</span><span class="sxs-lookup"><span data-stu-id="d1978-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="d1978-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1978-110">PARAMETERS</span></span>

### <span data-ttu-id="d1978-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d1978-111">-Context</span></span>
<span data-ttu-id="d1978-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d1978-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d1978-113">Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1978-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d1978-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1978-114">-DefaultProfile</span></span>
<span data-ttu-id="d1978-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1978-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1978-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d1978-116">-ServiceType</span></span>
<span data-ttu-id="d1978-117">Określa typ usługi magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d1978-117">Specifies the storage service type.</span></span>
<span data-ttu-id="d1978-118">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d1978-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="d1978-119">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d1978-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d1978-120">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="d1978-120">Blob</span></span> 
- <span data-ttu-id="d1978-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="d1978-121">Table</span></span>
- <span data-ttu-id="d1978-122">Kolejka</span><span class="sxs-lookup"><span data-stu-id="d1978-122">Queue</span></span>
- <span data-ttu-id="d1978-123">Plik</span><span class="sxs-lookup"><span data-stu-id="d1978-123">File</span></span>

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

### <span data-ttu-id="d1978-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1978-124">CommonParameters</span></span>
<span data-ttu-id="d1978-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1978-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1978-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1978-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1978-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1978-127">INPUTS</span></span>

### <span data-ttu-id="d1978-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1978-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1978-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1978-129">OUTPUTS</span></span>

### <span data-ttu-id="d1978-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="d1978-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="d1978-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1978-131">NOTES</span></span>

## <span data-ttu-id="d1978-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1978-132">RELATED LINKS</span></span>
