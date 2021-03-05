---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: eff94aac5ac9a1a71a12f31be81a1eb4c89bf73b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981386"
---
# <span data-ttu-id="4f225-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4f225-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="4f225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f225-102">SYNOPSIS</span></span>
<span data-ttu-id="4f225-103">Pobiera właściwości usług magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4f225-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="4f225-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4f225-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f225-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4f225-105">DESCRIPTION</span></span>
<span data-ttu-id="4f225-106">Polecenie **cmdlet Get-AzStorageServiceProperty** otrzymuje właściwości usług magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4f225-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="4f225-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4f225-107">EXAMPLES</span></span>

### <span data-ttu-id="4f225-108">Przykład 1. Pobierz właściwość usług Azure Storage usługi blob</span><span class="sxs-lookup"><span data-stu-id="4f225-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="4f225-109">To polecenie pobiera właściwość DefaultServiceVersion usługi blob.</span><span class="sxs-lookup"><span data-stu-id="4f225-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="4f225-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f225-110">PARAMETERS</span></span>

### <span data-ttu-id="4f225-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="4f225-111">-Context</span></span>
<span data-ttu-id="4f225-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4f225-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4f225-113">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f225-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4f225-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f225-114">-DefaultProfile</span></span>
<span data-ttu-id="4f225-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f225-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f225-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4f225-116">-ServiceType</span></span>
<span data-ttu-id="4f225-117">Określa typ usługi magazynowania.</span><span class="sxs-lookup"><span data-stu-id="4f225-117">Specifies the storage service type.</span></span>
<span data-ttu-id="4f225-118">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4f225-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="4f225-119">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4f225-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f225-120">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="4f225-120">Blob</span></span> 
- <span data-ttu-id="4f225-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="4f225-121">Table</span></span>
- <span data-ttu-id="4f225-122">Kolejka</span><span class="sxs-lookup"><span data-stu-id="4f225-122">Queue</span></span>
- <span data-ttu-id="4f225-123">Plik</span><span class="sxs-lookup"><span data-stu-id="4f225-123">File</span></span>

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

### <span data-ttu-id="4f225-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f225-124">CommonParameters</span></span>
<span data-ttu-id="4f225-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f225-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f225-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f225-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f225-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f225-127">INPUTS</span></span>

### <span data-ttu-id="4f225-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f225-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4f225-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f225-129">OUTPUTS</span></span>

### <span data-ttu-id="4f225-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="4f225-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="4f225-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4f225-131">NOTES</span></span>

## <span data-ttu-id="4f225-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f225-132">RELATED LINKS</span></span>
