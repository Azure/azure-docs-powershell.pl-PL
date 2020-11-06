---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: 7036f12b4ab47043b69fe4164ac567f4355a51ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550732"
---
# <span data-ttu-id="2065d-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2065d-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="2065d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2065d-102">SYNOPSIS</span></span>
<span data-ttu-id="2065d-103">Modyfikuje właściwości usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2065d-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2065d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2065d-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2065d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2065d-105">DESCRIPTION</span></span>
<span data-ttu-id="2065d-106">Polecenie cmdlet **Update-AzureStorageServiceProperty** modyfikuje właściwości usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2065d-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="2065d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2065d-107">EXAMPLES</span></span>

### <span data-ttu-id="2065d-108">Przykład 1: Ustawianie DefaultServiceVersion usługi BLOB na 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="2065d-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="2065d-109">To polecenie ustawia DefaultServiceVersion usługi BLOB równą 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="2065d-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="2065d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2065d-110">PARAMETERS</span></span>

### <span data-ttu-id="2065d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2065d-111">-Context</span></span>
<span data-ttu-id="2065d-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2065d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2065d-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2065d-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2065d-114">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="2065d-114">-DefaultServiceVersion</span></span>
<span data-ttu-id="2065d-115">DefaultServiceVersion wskazuje domyślną wersję, która ma być używana dla żądań w usłudze BLOB, jeśli nie została określona wersja żądania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="2065d-115">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="2065d-116">Możliwe wartości to: wersja 2008-10-27 i wszystkie nowsze wersje.</span><span class="sxs-lookup"><span data-stu-id="2065d-116">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="2065d-117">Zobacz więcej szczegółów w https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="2065d-117">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2065d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2065d-118">-PassThru</span></span>
<span data-ttu-id="2065d-119">Wyświetlanie właściwości serviceproperties</span><span class="sxs-lookup"><span data-stu-id="2065d-119">Display ServiceProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2065d-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="2065d-120">-ServiceType</span></span>
<span data-ttu-id="2065d-121">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="2065d-121">Specifies the storage service type.</span></span>
<span data-ttu-id="2065d-122">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="2065d-122">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="2065d-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2065d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2065d-124">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="2065d-124">Blob</span></span> 
- <span data-ttu-id="2065d-125">Tworząc</span><span class="sxs-lookup"><span data-stu-id="2065d-125">Table</span></span>
- <span data-ttu-id="2065d-126">Wykonany</span><span class="sxs-lookup"><span data-stu-id="2065d-126">Queue</span></span>
- <span data-ttu-id="2065d-127">Plik</span><span class="sxs-lookup"><span data-stu-id="2065d-127">File</span></span>

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

### <span data-ttu-id="2065d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2065d-128">-Confirm</span></span>
<span data-ttu-id="2065d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2065d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2065d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2065d-130">-WhatIf</span></span>
<span data-ttu-id="2065d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2065d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2065d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2065d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2065d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2065d-133">CommonParameters</span></span>
<span data-ttu-id="2065d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2065d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2065d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2065d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2065d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2065d-136">INPUTS</span></span>

### <span data-ttu-id="2065d-137">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2065d-137">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2065d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2065d-138">OUTPUTS</span></span>

### <span data-ttu-id="2065d-139">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="2065d-139">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="2065d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2065d-140">NOTES</span></span>

## <span data-ttu-id="2065d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2065d-141">RELATED LINKS</span></span>

