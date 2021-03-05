---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 46fff0df9eddc417f823aa7b0243824befb974e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973281"
---
# <span data-ttu-id="b9ee8-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b9ee8-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="b9ee8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ee8-103">Modyfikuje właściwości usługi dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b9ee8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b9ee8-104">SYNTAX</span></span>

### <span data-ttu-id="b9ee8-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="b9ee8-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ee8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b9ee8-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ee8-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="b9ee8-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9ee8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b9ee8-108">DESCRIPTION</span></span>
<span data-ttu-id="b9ee8-109">Polecenie **cmdlet Update-AzStorageBlobServiceProperty** modyfikuje właściwości usługi dla usługi obiektów blob magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b9ee8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b9ee8-110">EXAMPLES</span></span>

### <span data-ttu-id="b9ee8-111">Przykład 1. Ustawianie usługi obiektów blob DefaultServiceVersion na 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="b9ee8-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
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

<span data-ttu-id="b9ee8-112">To polecenie ustawia wartość DefaultServiceVersion usługi obiektów blob na 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="b9ee8-113">Przykład 2. Włączanie kanału zmiany w usłudze blob konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b9ee8-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
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

<span data-ttu-id="b9ee8-114">To polecenie umożliwia usłudze Changefeed w usłudze blob konta magazynu obsługa kanału zmiany w magazynie obiektów blob platformy Azure działa przez słuchanie konta magazynu protokołu GPv2 lub magazynu obiektów blob dla dowolnego zdarzenia tworzenia, modyfikowania lub usuwania na poziomie obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="b9ee8-115">Następnie wyprowadza uporządkowany dziennik zdarzeń dla obiektów blob przechowywanych w $blobchangefeed w ramach konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="b9ee8-116">Zmiany serializowane są zachowywane jako plik Avro i mogą być przetwarzane asynchronicznie i stopniowo.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="b9ee8-117">Przykład 3. Włączanie przechowywania wersji w usłudze blob konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b9ee8-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
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

<span data-ttu-id="b9ee8-118">To polecenie umożliwia przechowywanie wersji w usłudze blob konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b9ee8-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="b9ee8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9ee8-119">PARAMETERS</span></span>

### <span data-ttu-id="b9ee8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ee8-120">-DefaultProfile</span></span>
<span data-ttu-id="b9ee8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9ee8-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="b9ee8-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="b9ee8-123">Domyślna wersja usługi do ustawienia</span><span class="sxs-lookup"><span data-stu-id="b9ee8-123">Default Service Version to Set</span></span>

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

### <span data-ttu-id="b9ee8-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="b9ee8-124">-EnableChangeFeed</span></span>
<span data-ttu-id="b9ee8-125">Włącz rejestrowanie kanałów zmian dla konta magazynu, ustawiaując dla $true wyłącz rejestrowanie kanału zmian, ustawiaując dla $false.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

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

### <span data-ttu-id="b9ee8-126">-IsVersioningEnabled</span><span class="sxs-lookup"><span data-stu-id="b9ee8-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="b9ee8-127">Pobiera lub ustawia obsługę wersji, jeśli ustawiono wartość prawda.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-127">Gets or sets versioning is enabled if set to true.</span></span>

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

### <span data-ttu-id="b9ee8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ee8-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9ee8-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b9ee8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9ee8-130">-ResourceId</span></span>
<span data-ttu-id="b9ee8-131">Wprowadź identyfikator zasobu konta magazynu lub identyfikator zasobu właściwości usługi obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="b9ee8-132">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9ee8-132">-StorageAccount</span></span>
<span data-ttu-id="b9ee8-133">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b9ee8-133">Storage account object</span></span>

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

### <span data-ttu-id="b9ee8-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b9ee8-134">-StorageAccountName</span></span>
<span data-ttu-id="b9ee8-135">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="b9ee8-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9ee8-136">-Confirm</span></span>
<span data-ttu-id="b9ee8-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ee8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ee8-138">-WhatIf</span></span>
<span data-ttu-id="b9ee8-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9ee8-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ee8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ee8-141">CommonParameters</span></span>
<span data-ttu-id="b9ee8-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ee8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ee8-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9ee8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ee8-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9ee8-144">INPUTS</span></span>

### <span data-ttu-id="b9ee8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b9ee8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b9ee8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b9ee8-146">System.String</span></span>

## <span data-ttu-id="b9ee8-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9ee8-147">OUTPUTS</span></span>

### <span data-ttu-id="b9ee8-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="b9ee8-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="b9ee8-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b9ee8-149">NOTES</span></span>

## <span data-ttu-id="b9ee8-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9ee8-150">RELATED LINKS</span></span>
