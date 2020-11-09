---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316890"
---
# <span data-ttu-id="6ed6c-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6ed6c-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="6ed6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ed6c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed6c-103">Modyfikuje właściwości usługi dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="6ed6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ed6c-104">SYNTAX</span></span>

### <span data-ttu-id="6ed6c-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6ed6c-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ed6c-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="6ed6c-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ed6c-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="6ed6c-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ed6c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ed6c-108">DESCRIPTION</span></span>
<span data-ttu-id="6ed6c-109">Polecenie cmdlet **Update-AzStorageBlobServiceProperty** modyfikuje właściwości usługi dla usługi blob magazynu Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="6ed6c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ed6c-110">EXAMPLES</span></span>

### <span data-ttu-id="6ed6c-111">Przykład 1: Ustawianie DefaultServiceVersion usługi BLOB na 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="6ed6c-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

<span data-ttu-id="6ed6c-112">To polecenie ustawia DefaultServiceVersion usługi BLOB na 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="6ed6c-113">Przykład 2: Włączanie Changefeed w usłudze BLOB na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="6ed6c-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

<span data-ttu-id="6ed6c-114">To polecenie włącza Changefeed w ramach usługi BLOB na koncie magazynu z obsługą podawania zmian w magazynie obiektów blob, ponieważ umożliwia nasłuchiwanie zdarzeń tworzenia, modyfikowania lub usuwania na poziomie obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="6ed6c-115">Następnie zapisuje uporządkowany dziennik zdarzeń dla obiektów BLOB przechowywanych w kontenerze $blobchangefeed na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="6ed6c-116">Serializowane zmiany są zachowywane jako plik programu Apache Avro i mogą być przetwarzane asynchronicznie i stopniowo.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="6ed6c-117">Przykład 3: Włączanie przechowywania wersji w usłudze BLOB na koncie magazynu</span><span class="sxs-lookup"><span data-stu-id="6ed6c-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

<span data-ttu-id="6ed6c-118">To polecenie umożliwia włączenie przechowywania wersji w usłudze BLOB konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6ed6c-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="6ed6c-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ed6c-119">PARAMETERS</span></span>

### <span data-ttu-id="6ed6c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed6c-120">-DefaultProfile</span></span>
<span data-ttu-id="6ed6c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed6c-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="6ed6c-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="6ed6c-123">Domyślna wersja usługi do ustawienia</span><span class="sxs-lookup"><span data-stu-id="6ed6c-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="6ed6c-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="6ed6c-124">-EnableChangeFeed</span></span>
<span data-ttu-id="6ed6c-125">Włącz rejestrowanie źródeł zmian dla konta magazynu, korzystając z ustawienia $true, Wyłącz rejestrowanie źródeł zmian przez ustawienie w $false.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed6c-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="6ed6c-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="6ed6c-127">Pobiera lub ustawia przechowywanie wersji jest włączone, jeśli ustawiono wartość PRAWDA.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-127">Gets or sets versioning is enabled if set to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed6c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ed6c-128">-ResourceGroupName</span></span>
<span data-ttu-id="6ed6c-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed6c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ed6c-130">-ResourceId</span></span>
<span data-ttu-id="6ed6c-131">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed6c-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ed6c-132">-StorageAccount</span></span>
<span data-ttu-id="6ed6c-133">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6ed6c-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed6c-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6ed6c-134">-StorageAccountName</span></span>
<span data-ttu-id="6ed6c-135">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ed6c-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ed6c-136">-Confirm</span></span>
<span data-ttu-id="6ed6c-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ed6c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ed6c-138">-WhatIf</span></span>
<span data-ttu-id="6ed6c-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ed6c-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ed6c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed6c-141">CommonParameters</span></span>
<span data-ttu-id="6ed6c-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ed6c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed6c-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ed6c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed6c-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ed6c-144">INPUTS</span></span>

### <span data-ttu-id="6ed6c-145">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ed6c-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6ed6c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6ed6c-146">System.String</span></span>

## <span data-ttu-id="6ed6c-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ed6c-147">OUTPUTS</span></span>

### <span data-ttu-id="6ed6c-148">Microsoft. Azure. Commands. Management. Storage. models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="6ed6c-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="6ed6c-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ed6c-149">NOTES</span></span>

## <span data-ttu-id="6ed6c-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ed6c-150">RELATED LINKS</span></span>
