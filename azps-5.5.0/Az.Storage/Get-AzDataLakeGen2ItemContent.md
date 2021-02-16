---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178267"
---
# <span data-ttu-id="b0f9a-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="b0f9a-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="b0f9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f9a-103">Pobierz plik.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-103">Download a file.</span></span>

## <span data-ttu-id="b0f9a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0f9a-104">SYNTAX</span></span>

### <span data-ttu-id="b0f9a-105">ReceiveManual (Default)</span><span class="sxs-lookup"><span data-stu-id="b0f9a-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0f9a-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="b0f9a-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0f9a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0f9a-107">DESCRIPTION</span></span>
<span data-ttu-id="b0f9a-108">Polecenie **cmdlet Get-AzDataLakeGen2ItemContent** pobiera plik z systemu plików na koncie magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="b0f9a-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu włączono hierarchiczną przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="b0f9a-110">Tego rodzaju konto można utworzyć za pomocą polecenia cmdlet "New-AzStorageAccount" z poleceniem "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="b0f9a-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="b0f9a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0f9a-111">EXAMPLES</span></span>

### <span data-ttu-id="b0f9a-112">Przykład 1. Pobieranie pliku bez monitu</span><span class="sxs-lookup"><span data-stu-id="b0f9a-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="b0f9a-113">To polecenie pobiera plik do pliku lokalnego bez monitu.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="b0f9a-114">Przykład 2. Pobieranie pliku, a następnie potok pobierania pliku do pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="b0f9a-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="b0f9a-115">To polecenie najpierw pobiera plik, a następnie potok pobierania pliku do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="b0f9a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0f9a-116">PARAMETERS</span></span>

### <span data-ttu-id="b0f9a-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b0f9a-117">-AsJob</span></span>
<span data-ttu-id="b0f9a-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b0f9a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0f9a-119">— CheckMd5</span><span class="sxs-lookup"><span data-stu-id="b0f9a-119">-CheckMd5</span></span>
<span data-ttu-id="b0f9a-120">sprawdzanie md5sum</span><span class="sxs-lookup"><span data-stu-id="b0f9a-120">check the md5sum</span></span>

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

### <span data-ttu-id="b0f9a-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b0f9a-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b0f9a-122">Całkowita ilość jednoczesnych zadań synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="b0f9a-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-123">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f9a-124">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b0f9a-124">-Context</span></span>
<span data-ttu-id="b0f9a-125">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b0f9a-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b0f9a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f9a-126">-DefaultProfile</span></span>
<span data-ttu-id="b0f9a-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f9a-128">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="b0f9a-128">-Destination</span></span>
<span data-ttu-id="b0f9a-129">Docelowa ścieżka pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-129">Destination local file path.</span></span>

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

### <span data-ttu-id="b0f9a-130">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b0f9a-130">-FileSystem</span></span>
<span data-ttu-id="b0f9a-131">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="b0f9a-131">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f9a-132">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b0f9a-132">-Force</span></span>
<span data-ttu-id="b0f9a-133">Wymuszanie zastąpienia istniejącego obiektu blob lub pliku</span><span class="sxs-lookup"><span data-stu-id="b0f9a-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="b0f9a-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0f9a-134">-InputObject</span></span>
<span data-ttu-id="b0f9a-135">Obiekt elementu Platformy Azure Datalake Gen2 do pobrania.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-135">Azure Datalake Gen2 Item Object to download.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f9a-136">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="b0f9a-136">-Path</span></span>
<span data-ttu-id="b0f9a-137">Ścieżka w określonym systemie plików, która powinna zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="b0f9a-138">Może być plikiem lub katalogiem w formacie "katalog/file.txt" lub "katalog1/katalog2/"</span><span class="sxs-lookup"><span data-stu-id="b0f9a-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0f9a-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0f9a-139">-Confirm</span></span>
<span data-ttu-id="b0f9a-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0f9a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0f9a-141">-WhatIf</span></span>
<span data-ttu-id="b0f9a-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0f9a-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0f9a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f9a-144">CommonParameters</span></span>
<span data-ttu-id="b0f9a-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f9a-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0f9a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f9a-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0f9a-147">INPUTS</span></span>

### <span data-ttu-id="b0f9a-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b0f9a-148">System.String</span></span>

### <span data-ttu-id="b0f9a-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b0f9a-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="b0f9a-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b0f9a-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b0f9a-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0f9a-151">OUTPUTS</span></span>

### <span data-ttu-id="b0f9a-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="b0f9a-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="b0f9a-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0f9a-153">NOTES</span></span>

## <span data-ttu-id="b0f9a-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0f9a-154">RELATED LINKS</span></span>
