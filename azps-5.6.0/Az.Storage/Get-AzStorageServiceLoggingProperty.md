---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 4d956dfd49e541751003d28c31285722616ab640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997053"
---
# <span data-ttu-id="27845-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="27845-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="27845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27845-102">SYNOPSIS</span></span>
<span data-ttu-id="27845-103">Pobiera właściwości rejestrowania dla usług magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="27845-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="27845-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="27845-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27845-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="27845-105">DESCRIPTION</span></span>
<span data-ttu-id="27845-106">Polecenie **cmdlet Get-AzStorageServiceLoggingProperty** pobiera właściwości rejestrowania dla usług magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="27845-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="27845-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="27845-107">EXAMPLES</span></span>

### <span data-ttu-id="27845-108">Przykład 1. Uzyskiwanie właściwości rejestrowania dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="27845-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="27845-109">To polecenie pobiera właściwości rejestrowania dla magazynu obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="27845-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="27845-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27845-110">PARAMETERS</span></span>

### <span data-ttu-id="27845-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="27845-111">-Context</span></span>
<span data-ttu-id="27845-112">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="27845-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="27845-113">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27845-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="27845-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27845-114">-DefaultProfile</span></span>
<span data-ttu-id="27845-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="27845-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27845-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="27845-116">-ServiceType</span></span>
<span data-ttu-id="27845-117">Określa typ usługi magazynowania.</span><span class="sxs-lookup"><span data-stu-id="27845-117">Specifies the storage service type.</span></span>
<span data-ttu-id="27845-118">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="27845-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="27845-119">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="27845-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27845-120">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="27845-120">Blob</span></span> 
- <span data-ttu-id="27845-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="27845-121">Table</span></span>
- <span data-ttu-id="27845-122">Kolejka</span><span class="sxs-lookup"><span data-stu-id="27845-122">Queue</span></span>
- <span data-ttu-id="27845-123">Plik Wartość Pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="27845-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="27845-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27845-124">CommonParameters</span></span>
<span data-ttu-id="27845-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27845-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27845-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27845-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27845-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27845-127">INPUTS</span></span>

### <span data-ttu-id="27845-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="27845-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="27845-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27845-129">OUTPUTS</span></span>

### <span data-ttu-id="27845-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="27845-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="27845-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="27845-131">NOTES</span></span>

## <span data-ttu-id="27845-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27845-132">RELATED LINKS</span></span>

[<span data-ttu-id="27845-133">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="27845-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="27845-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="27845-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


