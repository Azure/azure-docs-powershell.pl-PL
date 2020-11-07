---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
ms.openlocfilehash: 2f0c59acba56fb80a12df0c5df6c8168ebc91000
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899149"
---
# <span data-ttu-id="8fdb2-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8fdb2-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="8fdb2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8fdb2-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdb2-103">Modyfikuje właściwości usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fdb2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8fdb2-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fdb2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8fdb2-105">DESCRIPTION</span></span>
<span data-ttu-id="8fdb2-106">Polecenie cmdlet **Update-AzureStorageServiceProperty** modyfikuje właściwości usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="8fdb2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8fdb2-107">EXAMPLES</span></span>

### <span data-ttu-id="8fdb2-108">Przykład 1: Ustawianie DefaultServiceVersion usługi BLOB na 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="8fdb2-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="8fdb2-109">To polecenie ustawia DefaultServiceVersion usługi BLOB równą 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="8fdb2-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="8fdb2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8fdb2-110">PARAMETERS</span></span>

### <span data-ttu-id="8fdb2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8fdb2-111">-Context</span></span>
<span data-ttu-id="8fdb2-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8fdb2-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8fdb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdb2-114">-DefaultProfile</span></span>
<span data-ttu-id="8fdb2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fdb2-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="8fdb2-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="8fdb2-117">DefaultServiceVersion wskazuje domyślną wersję, która ma być używana dla żądań w usłudze BLOB, jeśli nie została określona wersja żądania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="8fdb2-118">Możliwe wartości to: wersja 2008-10-27 i wszystkie nowsze wersje.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="8fdb2-119">Zobacz więcej szczegółów w https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="8fdb2-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdb2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fdb2-120">-PassThru</span></span>
<span data-ttu-id="8fdb2-121">Wyświetlanie właściwości serviceproperties</span><span class="sxs-lookup"><span data-stu-id="8fdb2-121">Display ServiceProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdb2-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="8fdb2-122">-ServiceType</span></span>
<span data-ttu-id="8fdb2-123">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-123">Specifies the storage service type.</span></span>
<span data-ttu-id="8fdb2-124">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="8fdb2-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8fdb2-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8fdb2-126">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="8fdb2-126">Blob</span></span> 
- <span data-ttu-id="8fdb2-127">Tworząc</span><span class="sxs-lookup"><span data-stu-id="8fdb2-127">Table</span></span>
- <span data-ttu-id="8fdb2-128">Wykonany</span><span class="sxs-lookup"><span data-stu-id="8fdb2-128">Queue</span></span>
- <span data-ttu-id="8fdb2-129">Plik</span><span class="sxs-lookup"><span data-stu-id="8fdb2-129">File</span></span>

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

### <span data-ttu-id="8fdb2-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8fdb2-130">-Confirm</span></span>
<span data-ttu-id="8fdb2-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdb2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fdb2-132">-WhatIf</span></span>
<span data-ttu-id="8fdb2-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fdb2-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdb2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdb2-135">CommonParameters</span></span>
<span data-ttu-id="8fdb2-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fdb2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdb2-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fdb2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdb2-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fdb2-138">INPUTS</span></span>

### <span data-ttu-id="8fdb2-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8fdb2-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8fdb2-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8fdb2-140">OUTPUTS</span></span>

### <span data-ttu-id="8fdb2-141">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="8fdb2-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="8fdb2-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8fdb2-142">NOTES</span></span>

## <span data-ttu-id="8fdb2-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fdb2-143">RELATED LINKS</span></span>
