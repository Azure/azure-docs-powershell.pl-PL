---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/copy-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
ms.openlocfilehash: 76e89c90da10e8e232a564fb5fb7e5f8cc807327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988758"
---
# <span data-ttu-id="efea6-101">Copy-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="efea6-101">Copy-AzStorageBlob</span></span>

## <span data-ttu-id="efea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efea6-102">SYNOPSIS</span></span>
<span data-ttu-id="efea6-103">Kopiowanie obiektu blob synchronicznie.</span><span class="sxs-lookup"><span data-stu-id="efea6-103">Copy a blob synchronously.</span></span>

## <span data-ttu-id="efea6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="efea6-104">SYNTAX</span></span>

### <span data-ttu-id="efea6-105">ContainerName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="efea6-105">ContainerName (Default)</span></span>
```
Copy-AzStorageBlob [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efea6-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="efea6-106">BlobInstance</span></span>
```
Copy-AzStorageBlob [-BlobBaseClient <BlobBaseClient>] -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efea6-107">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="efea6-107">UriPipeline</span></span>
```
Copy-AzStorageBlob -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efea6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="efea6-108">DESCRIPTION</span></span>
<span data-ttu-id="efea6-109">Polecenie **cmdlet Copy-AzStorageBlob** kopiuje obiekt blob synchronicznie, obecnie obsługuje tylko obiekt blob bloku.</span><span class="sxs-lookup"><span data-stu-id="efea6-109">The **Copy-AzStorageBlob** cmdlet copies a blob synchronously, currently only support block blob.</span></span>

## <span data-ttu-id="efea6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="efea6-110">EXAMPLES</span></span>

### <span data-ttu-id="efea6-111">Przykład 1. Kopiowanie nazwanego obiektu blob do innego obiektu blob</span><span class="sxs-lookup"><span data-stu-id="efea6-111">Example 1: Copy a named blob to another</span></span>
```
C:\PS> $destBlob = Copy-AzStorageBlob -SrcContainer "sourcecontainername" -SrcBlob "srcblobname" -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="efea6-112">To polecenie kopiuje obiekt blob z kontenera źródłowego do kontenera docelowego z nową nazwą obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="efea6-112">This command copies a blob from source container to the destination container with a new blob name.</span></span> 

### <span data-ttu-id="efea6-113">Przykład 2. Kopiowanie obiektu blob z obiektu blob</span><span class="sxs-lookup"><span data-stu-id="efea6-113">Example 2: Copy blob from a blob object</span></span>
```
C:\PS> $srcBlob = Get-AzStorageBlob -Container $containerName -Blob $blobName  -Context $ctx 
C:\PS> $destBlob =  $srcBlob | Copy-AzStorageBlob  -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="efea6-114">To polecenie kopiuje obiekt blob ze źródłowego obiektu blob do kontenera docelowego z nową nazwą obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="efea6-114">This command copies a blob from source blob object to the destination container with a new blob name.</span></span>

### <span data-ttu-id="efea6-115">Przykład 3. Kopiowanie obiektu blob z obiektu blob Uri</span><span class="sxs-lookup"><span data-stu-id="efea6-115">Example 3: Copy blob from a blob Uri</span></span>
```
C:\PS> $srcBlobUri = New-AzStorageBlobSASToken -Container $srcContainerName -Blob $srcBlobName -Permission rt -ExpiryTime (Get-Date).AddDays(7) -FullUri 
C:\PS> $destBlob = Copy-AzStorageBlob -AbsoluteUri $srcBlobUri -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="efea6-116">Pierwsze polecenie tworzy obiekt blob Uri źródłowego obiektu blob z tokenem sas uprawnień "rt".</span><span class="sxs-lookup"><span data-stu-id="efea6-116">The first command creates a blob Uri of the source blob, with sas token of permission "rt".</span></span> <span data-ttu-id="efea6-117">Drugie polecenie kopiuje ze źródłowego obiektu blob Uri do docelowego obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="efea6-117">The second command copies from source blob Uri to the destination blob.</span></span>

### <span data-ttu-id="efea6-118">Przykład 4. Aktualizowanie zakresu szyfrowania obiektów blob blokowych</span><span class="sxs-lookup"><span data-stu-id="efea6-118">Example 4: Update a block blob encryption scope</span></span>
```
C:\PS> $blob = Copy-AzStorageBlob -SrcContainer $containerName -SrcBlob $blobname -DestContainer $containername -EncryptionScope $newScopeName -Force
```

<span data-ttu-id="efea6-119">To polecenie aktualizuje zakres szyfrowania obiektów blob bloku, kopiując go do siebie z nowym zakresem szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="efea6-119">This command update a block blob encryption scope by copy it to itself with a new encryption scope.</span></span>

## <span data-ttu-id="efea6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efea6-120">PARAMETERS</span></span>

### <span data-ttu-id="efea6-121">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="efea6-121">-AbsoluteUri</span></span>
<span data-ttu-id="efea6-122">Źródłowy kod uri obiektów blob</span><span class="sxs-lookup"><span data-stu-id="efea6-122">Source blob uri</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-123">— AsJob</span><span class="sxs-lookup"><span data-stu-id="efea6-123">-AsJob</span></span>
<span data-ttu-id="efea6-124">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="efea6-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efea6-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="efea6-125">-BlobBaseClient</span></span>
<span data-ttu-id="efea6-126">Obiekt BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="efea6-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-127">— kontekst</span><span class="sxs-lookup"><span data-stu-id="efea6-127">-Context</span></span>
<span data-ttu-id="efea6-128">Źródłowy obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="efea6-128">Source Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efea6-129">-DefaultProfile</span></span>
<span data-ttu-id="efea6-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="efea6-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efea6-131">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="efea6-131">-DestBlob</span></span>
<span data-ttu-id="efea6-132">Nazwa obiektu blob miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="efea6-132">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-133">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="efea6-133">-DestContainer</span></span>
<span data-ttu-id="efea6-134">Nazwa kontenera docelowego</span><span class="sxs-lookup"><span data-stu-id="efea6-134">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-135">-DestContext</span><span class="sxs-lookup"><span data-stu-id="efea6-135">-DestContext</span></span>
<span data-ttu-id="efea6-136">Obiekt kontekstowy magazynu docelowego</span><span class="sxs-lookup"><span data-stu-id="efea6-136">Destination Storage context object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-137">- EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="efea6-137">-EncryptionScope</span></span>
<span data-ttu-id="efea6-138">Zakres szyfrowania, który ma być używany podczas żądania do obiektu blob dest.</span><span class="sxs-lookup"><span data-stu-id="efea6-138">Encryption scope to be used when making requests to the dest blob.</span></span>

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

### <span data-ttu-id="efea6-139">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="efea6-139">-Force</span></span>
<span data-ttu-id="efea6-140">Wymuszanie zastąpienia istniejącego obiektu blob lub pliku</span><span class="sxs-lookup"><span data-stu-id="efea6-140">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="efea6-141">-RepatatePriority</span><span class="sxs-lookup"><span data-stu-id="efea6-141">-RehydratePriority</span></span>
<span data-ttu-id="efea6-142">Zablokuj ponowną dzierżawę obiektu blob.</span><span class="sxs-lookup"><span data-stu-id="efea6-142">Block Blob RehydratePriority.</span></span>
<span data-ttu-id="efea6-143">Wskazuje priorytet, z którym ma być ponownie wynoszony zarchiwizowane obiekty blob.</span><span class="sxs-lookup"><span data-stu-id="efea6-143">Indicates the priority with which to rehydrate an archived blob.</span></span>
<span data-ttu-id="efea6-144">Prawidłowe wartości to wysoka/standardowa wartość.</span><span class="sxs-lookup"><span data-stu-id="efea6-144">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-145">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="efea6-145">-SrcBlob</span></span>
<span data-ttu-id="efea6-146">Nazwa obiektu blob</span><span class="sxs-lookup"><span data-stu-id="efea6-146">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-147">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="efea6-147">-SrcContainer</span></span>
<span data-ttu-id="efea6-148">Nazwa kontenera źródłowego</span><span class="sxs-lookup"><span data-stu-id="efea6-148">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-149">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="efea6-149">-StandardBlobTier</span></span>
<span data-ttu-id="efea6-150">Blokuj warstwę obiektów blob, prawidłowe wartości to hot/cool/archive.</span><span class="sxs-lookup"><span data-stu-id="efea6-150">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="efea6-151">Zobacz szczegóły w https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="efea6-151">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efea6-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efea6-152">-Confirm</span></span>
<span data-ttu-id="efea6-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="efea6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efea6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efea6-154">-WhatIf</span></span>
<span data-ttu-id="efea6-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efea6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efea6-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="efea6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efea6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efea6-157">CommonParameters</span></span>
<span data-ttu-id="efea6-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efea6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efea6-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efea6-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efea6-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efea6-160">INPUTS</span></span>

### <span data-ttu-id="efea6-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="efea6-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="efea6-162">System.String</span><span class="sxs-lookup"><span data-stu-id="efea6-162">System.String</span></span>

### <span data-ttu-id="efea6-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="efea6-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="efea6-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efea6-164">OUTPUTS</span></span>

### <span data-ttu-id="efea6-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="efea6-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="efea6-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="efea6-166">NOTES</span></span>

## <span data-ttu-id="efea6-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efea6-167">RELATED LINKS</span></span>
