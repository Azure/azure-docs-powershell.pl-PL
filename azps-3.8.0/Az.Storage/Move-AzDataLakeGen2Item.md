---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052119"
---
# <span data-ttu-id="f1f47-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1f47-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="f1f47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1f47-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f47-103">Przenoszenie pliku lub katalogu do innego pliku lub katalogu na tym samym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="f1f47-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="f1f47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1f47-104">SYNTAX</span></span>

### <span data-ttu-id="f1f47-105">ReceiveManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f1f47-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1f47-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="f1f47-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1f47-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f1f47-107">DESCRIPTION</span></span>
<span data-ttu-id="f1f47-108">Polecenie cmdlet **Move-AzDataLakeGen2Item** przenosi plik lub katalog do innego pliku lub katalogu na tym samym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="f1f47-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="f1f47-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu jest włączone hierarchiczne obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="f1f47-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="f1f47-110">Ten rodzaj konta można utworzyć, uruchamiając polecenie cmdlet "New-AzStorageAccount" z opcją "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="f1f47-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="f1f47-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1f47-111">EXAMPLES</span></span>

### <span data-ttu-id="f1f47-112">Przykład 1: przenoszenie składu w tym samym systemie plików</span><span class="sxs-lookup"><span data-stu-id="f1f47-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="f1f47-113">To polecenie Przenieś katalog "dir1" do katalogu "dir3" w tym samym systemie plików.</span><span class="sxs-lookup"><span data-stu-id="f1f47-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="f1f47-114">Przykład 2: przenoszenie pliku według rurociągu do innego systemu plików na tym samym koncie magazynu bez monitu</span><span class="sxs-lookup"><span data-stu-id="f1f47-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="f1f47-115">To polecenie Przenieś plik "dir1/plik1" w "filesystem1" do pliku "dir2/file2" w "filesystem2" na tym samym koncie magazynu bez monitowania.</span><span class="sxs-lookup"><span data-stu-id="f1f47-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="f1f47-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1f47-116">PARAMETERS</span></span>

### <span data-ttu-id="f1f47-117">-Context</span><span class="sxs-lookup"><span data-stu-id="f1f47-117">-Context</span></span>
<span data-ttu-id="f1f47-118">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="f1f47-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f1f47-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f47-119">-DefaultProfile</span></span>
<span data-ttu-id="f1f47-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1f47-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f47-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="f1f47-121">-DestFileSystem</span></span>
<span data-ttu-id="f1f47-122">Nazwa docelowego systemu plików</span><span class="sxs-lookup"><span data-stu-id="f1f47-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="f1f47-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="f1f47-123">-DestPath</span></span>
<span data-ttu-id="f1f47-124">Ścieżka docelowego obiektu BLOB</span><span class="sxs-lookup"><span data-stu-id="f1f47-124">Dest Blob path</span></span>

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

### <span data-ttu-id="f1f47-125">— System plików</span><span class="sxs-lookup"><span data-stu-id="f1f47-125">-FileSystem</span></span>
<span data-ttu-id="f1f47-126">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="f1f47-126">FileSystem name</span></span>

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

### <span data-ttu-id="f1f47-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f1f47-127">-Force</span></span>
<span data-ttu-id="f1f47-128">Wymuś przekroczenie miejsca docelowego.</span><span class="sxs-lookup"><span data-stu-id="f1f47-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="f1f47-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f1f47-129">-InputObject</span></span>
<span data-ttu-id="f1f47-130">Obiekt usługi Azure datalake Gen2, z którego można przechodzić.</span><span class="sxs-lookup"><span data-stu-id="f1f47-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="f1f47-131">-Path</span><span class="sxs-lookup"><span data-stu-id="f1f47-131">-Path</span></span>
<span data-ttu-id="f1f47-132">Ścieżka w określonym systemie plików, z której należy przechodzić.</span><span class="sxs-lookup"><span data-stu-id="f1f47-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="f1f47-133">Może to być plik lub katalog w formacie "Directory/file.txt" lub "directory1/Directory2/"</span><span class="sxs-lookup"><span data-stu-id="f1f47-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="f1f47-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1f47-134">-Confirm</span></span>
<span data-ttu-id="f1f47-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1f47-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1f47-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1f47-136">-WhatIf</span></span>
<span data-ttu-id="f1f47-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1f47-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1f47-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f1f47-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1f47-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f47-139">CommonParameters</span></span>
<span data-ttu-id="f1f47-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f47-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f47-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f47-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f47-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1f47-142">INPUTS</span></span>

### <span data-ttu-id="f1f47-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f1f47-143">System.String</span></span>

### <span data-ttu-id="f1f47-144">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1f47-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="f1f47-145">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1f47-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f1f47-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1f47-146">OUTPUTS</span></span>

### <span data-ttu-id="f1f47-147">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f1f47-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="f1f47-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1f47-148">NOTES</span></span>

## <span data-ttu-id="f1f47-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1f47-149">RELATED LINKS</span></span>
