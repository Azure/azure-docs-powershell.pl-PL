---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318301"
---
# <span data-ttu-id="c4907-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c4907-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="c4907-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4907-102">SYNOPSIS</span></span>
<span data-ttu-id="c4907-103">Modyfikuje właściwości usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c4907-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c4907-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4907-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4907-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c4907-105">DESCRIPTION</span></span>
<span data-ttu-id="c4907-106">Polecenie cmdlet **Update-AzStorageServiceProperty** modyfikuje właściwości usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c4907-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="c4907-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4907-107">EXAMPLES</span></span>

### <span data-ttu-id="c4907-108">Przykład 1: Ustawianie DefaultServiceVersion usługi BLOB na 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="c4907-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="c4907-109">To polecenie ustawia DefaultServiceVersion usługi BLOB równą 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="c4907-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="c4907-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4907-110">PARAMETERS</span></span>

### <span data-ttu-id="c4907-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c4907-111">-Context</span></span>
<span data-ttu-id="c4907-112">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c4907-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c4907-113">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c4907-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c4907-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4907-114">-DefaultProfile</span></span>
<span data-ttu-id="c4907-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4907-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4907-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="c4907-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="c4907-117">DefaultServiceVersion wskazuje domyślną wersję, która ma być używana dla żądań w usłudze BLOB, jeśli nie została określona wersja żądania przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="c4907-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="c4907-118">Możliwe wartości to: wersja 2008-10-27 i wszystkie nowsze wersje.</span><span class="sxs-lookup"><span data-stu-id="c4907-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="c4907-119">Zobacz więcej szczegółów w https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="c4907-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="c4907-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4907-120">-PassThru</span></span>
<span data-ttu-id="c4907-121">Wyświetlanie właściwości serviceproperties</span><span class="sxs-lookup"><span data-stu-id="c4907-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="c4907-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c4907-122">-ServiceType</span></span>
<span data-ttu-id="c4907-123">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="c4907-123">Specifies the storage service type.</span></span>
<span data-ttu-id="c4907-124">To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="c4907-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c4907-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c4907-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4907-126">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="c4907-126">Blob</span></span> 
- <span data-ttu-id="c4907-127">Tworząc</span><span class="sxs-lookup"><span data-stu-id="c4907-127">Table</span></span>
- <span data-ttu-id="c4907-128">Wykonany</span><span class="sxs-lookup"><span data-stu-id="c4907-128">Queue</span></span>
- <span data-ttu-id="c4907-129">Plik</span><span class="sxs-lookup"><span data-stu-id="c4907-129">File</span></span>

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

### <span data-ttu-id="c4907-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4907-130">-Confirm</span></span>
<span data-ttu-id="c4907-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4907-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4907-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4907-132">-WhatIf</span></span>
<span data-ttu-id="c4907-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4907-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4907-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4907-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4907-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4907-135">CommonParameters</span></span>
<span data-ttu-id="c4907-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4907-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4907-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4907-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4907-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4907-138">INPUTS</span></span>

### <span data-ttu-id="c4907-139">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c4907-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c4907-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4907-140">OUTPUTS</span></span>

### <span data-ttu-id="c4907-141">Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="c4907-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="c4907-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4907-142">NOTES</span></span>

## <span data-ttu-id="c4907-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4907-143">RELATED LINKS</span></span>
