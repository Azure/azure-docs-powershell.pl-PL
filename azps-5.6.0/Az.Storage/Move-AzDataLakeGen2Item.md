---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: 203e7a246c16345631da290645b356392c165bad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979185"
---
# <span data-ttu-id="f59d8-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f59d8-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="f59d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f59d8-102">SYNOPSIS</span></span>
<span data-ttu-id="f59d8-103">Przenoszenie pliku lub katalogu do innego pliku lub katalogu na tym samym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="f59d8-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="f59d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f59d8-104">SYNTAX</span></span>

### <span data-ttu-id="f59d8-105">ReceiveManual (Default)</span><span class="sxs-lookup"><span data-stu-id="f59d8-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f59d8-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="f59d8-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f59d8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f59d8-107">DESCRIPTION</span></span>
<span data-ttu-id="f59d8-108">Polecenie **cmdlet Move-AzDataLakeGen2Item** przenosi plik lub katalog do innego pliku lub katalogu na tym samym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="f59d8-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="f59d8-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu włączono hierarchiczną przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="f59d8-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="f59d8-110">Tego rodzaju konto można utworzyć, uruchamiam polecenie cmdlet "New-AzStorageAccount" z poleceniem "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="f59d8-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="f59d8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f59d8-111">EXAMPLES</span></span>

### <span data-ttu-id="f59d8-112">Przykład 1. Przenoszenie zgięć w tym samym systemie plików</span><span class="sxs-lookup"><span data-stu-id="f59d8-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="f59d8-113">To polecenie przenosi katalog 'dir1' do katalogu 'dir3' w tym samym systemie plików.</span><span class="sxs-lookup"><span data-stu-id="f59d8-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="f59d8-114">Przykład 2. Przenoszenie pliku według potoku do innego systemu plików na tym samym koncie magazynu bez monitu</span><span class="sxs-lookup"><span data-stu-id="f59d8-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="f59d8-115">To polecenie przenosi plik 'dir1/file1' w 'filesystem1' do pliku 'dir2/file2' w 'filesystem2' na tym samym koncie magazynu bez monitu.</span><span class="sxs-lookup"><span data-stu-id="f59d8-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="f59d8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f59d8-116">PARAMETERS</span></span>

### <span data-ttu-id="f59d8-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="f59d8-117">-Context</span></span>
<span data-ttu-id="f59d8-118">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f59d8-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f59d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59d8-119">-DefaultProfile</span></span>
<span data-ttu-id="f59d8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f59d8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f59d8-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="f59d8-121">-DestFileSystem</span></span>
<span data-ttu-id="f59d8-122">Nazwa dest FileSystem</span><span class="sxs-lookup"><span data-stu-id="f59d8-122">Dest FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59d8-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="f59d8-123">-DestPath</span></span>
<span data-ttu-id="f59d8-124">Ścieżka obiektu blob Dest</span><span class="sxs-lookup"><span data-stu-id="f59d8-124">Dest Blob path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59d8-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="f59d8-125">-FileSystem</span></span>
<span data-ttu-id="f59d8-126">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="f59d8-126">FileSystem name</span></span>

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

### <span data-ttu-id="f59d8-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f59d8-127">-Force</span></span>
<span data-ttu-id="f59d8-128">Wymuszanie napisania miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="f59d8-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="f59d8-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f59d8-129">-InputObject</span></span>
<span data-ttu-id="f59d8-130">Obiekt elementu Platformy Azure Datalake Gen2 do przenoszenia się.</span><span class="sxs-lookup"><span data-stu-id="f59d8-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="f59d8-131">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="f59d8-131">-Path</span></span>
<span data-ttu-id="f59d8-132">Ścieżka w określonym systemie plików, z których należy się przenieść.</span><span class="sxs-lookup"><span data-stu-id="f59d8-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="f59d8-133">Może być plikiem lub katalogiem w formacie "katalog/file.txt" lub "katalog1/katalog2/"</span><span class="sxs-lookup"><span data-stu-id="f59d8-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="f59d8-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f59d8-134">-Confirm</span></span>
<span data-ttu-id="f59d8-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f59d8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f59d8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59d8-136">-WhatIf</span></span>
<span data-ttu-id="f59d8-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f59d8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f59d8-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f59d8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f59d8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59d8-139">CommonParameters</span></span>
<span data-ttu-id="f59d8-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59d8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59d8-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f59d8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59d8-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f59d8-142">INPUTS</span></span>

### <span data-ttu-id="f59d8-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f59d8-143">System.String</span></span>

### <span data-ttu-id="f59d8-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f59d8-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="f59d8-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f59d8-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f59d8-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f59d8-146">OUTPUTS</span></span>

### <span data-ttu-id="f59d8-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f59d8-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="f59d8-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f59d8-148">NOTES</span></span>

## <span data-ttu-id="f59d8-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f59d8-149">RELATED LINKS</span></span>
