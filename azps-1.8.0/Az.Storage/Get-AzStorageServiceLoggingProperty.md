---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: ba82dcc5cae9b0ea8fa8bfa097c10da95cd91b15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707621"
---
# <span data-ttu-id="987df-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="987df-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="987df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="987df-102">SYNOPSIS</span></span>
<span data-ttu-id="987df-103">Pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="987df-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="987df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="987df-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="987df-105">Opis</span><span class="sxs-lookup"><span data-stu-id="987df-105">DESCRIPTION</span></span>
<span data-ttu-id="987df-106">Polecenie cmdlet **Get-AzStorageServiceLoggingProperty** pobiera właściwości rejestrowania usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="987df-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="987df-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="987df-107">EXAMPLES</span></span>

### <span data-ttu-id="987df-108">Przykład 1: uzyskiwanie właściwości rejestrowania dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="987df-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="987df-109">To polecenie pobiera właściwości rejestrowania dla magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="987df-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="987df-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="987df-110">PARAMETERS</span></span>

### <span data-ttu-id="987df-111">-Context</span><span class="sxs-lookup"><span data-stu-id="987df-111">-Context</span></span>
<span data-ttu-id="987df-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="987df-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="987df-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="987df-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="987df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987df-114">-DefaultProfile</span></span>
<span data-ttu-id="987df-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="987df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="987df-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="987df-116">-ServiceType</span></span>
<span data-ttu-id="987df-117">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="987df-117">Specifies the storage service type.</span></span>
<span data-ttu-id="987df-118">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="987df-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="987df-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="987df-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="987df-120">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="987df-120">Blob</span></span> 
- <span data-ttu-id="987df-121">Tworząc</span><span class="sxs-lookup"><span data-stu-id="987df-121">Table</span></span>
- <span data-ttu-id="987df-122">Wykonany</span><span class="sxs-lookup"><span data-stu-id="987df-122">Queue</span></span>
- <span data-ttu-id="987df-123">Plik wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="987df-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="987df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987df-124">CommonParameters</span></span>
<span data-ttu-id="987df-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987df-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="987df-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987df-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="987df-127">INPUTS</span></span>

### <span data-ttu-id="987df-128">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="987df-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="987df-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="987df-129">OUTPUTS</span></span>

### <span data-ttu-id="987df-130">Microsoft. platformy windowsazure. Storage. Shared. Protocol. LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="987df-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="987df-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="987df-131">NOTES</span></span>

## <span data-ttu-id="987df-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="987df-132">RELATED LINKS</span></span>

[<span data-ttu-id="987df-133">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="987df-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="987df-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="987df-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


