---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349762"
---
# <span data-ttu-id="293d5-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="293d5-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="293d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="293d5-102">SYNOPSIS</span></span>
<span data-ttu-id="293d5-103">Pobieranie pliku.</span><span class="sxs-lookup"><span data-stu-id="293d5-103">Download a file.</span></span>

## <span data-ttu-id="293d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="293d5-104">SYNTAX</span></span>

### <span data-ttu-id="293d5-105">ReceiveManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="293d5-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="293d5-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="293d5-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="293d5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="293d5-107">DESCRIPTION</span></span>
<span data-ttu-id="293d5-108">Polecenie cmdlet **Get-AzDataLakeGen2ItemContent** pobiera plik w systemie plików na koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="293d5-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="293d5-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu jest włączone hierarchiczne obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="293d5-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="293d5-110">Ten rodzaj konta można utworzyć, uruchamiając polecenie cmdlet "New-AzStorageAccount" z opcją "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="293d5-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="293d5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="293d5-111">EXAMPLES</span></span>

### <span data-ttu-id="293d5-112">Przykład 1: Pobieranie pliku bez monitu</span><span class="sxs-lookup"><span data-stu-id="293d5-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="293d5-113">To polecenie pobiera plik do pliku lokalnego bez monitowania.</span><span class="sxs-lookup"><span data-stu-id="293d5-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="293d5-114">Przykład 2: uzyskiwanie pliku, a następnie planowane pobranie pliku do pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="293d5-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="293d5-115">To polecenie po raz pierwszy pobiera plik, a następnie tworzy go w celu pobrania pliku do pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="293d5-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="293d5-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="293d5-116">PARAMETERS</span></span>

### <span data-ttu-id="293d5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="293d5-117">-AsJob</span></span>
<span data-ttu-id="293d5-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="293d5-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="293d5-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="293d5-119">-CheckMd5</span></span>
<span data-ttu-id="293d5-120">Sprawdź md5sum</span><span class="sxs-lookup"><span data-stu-id="293d5-120">check the md5sum</span></span>

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

### <span data-ttu-id="293d5-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="293d5-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="293d5-122">Całkowita liczba współbieżnych zadań asynchronicznych.</span><span class="sxs-lookup"><span data-stu-id="293d5-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="293d5-123">Wartość domyślna to 10.</span><span class="sxs-lookup"><span data-stu-id="293d5-123">The default value is 10.</span></span>

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

### <span data-ttu-id="293d5-124">-Context</span><span class="sxs-lookup"><span data-stu-id="293d5-124">-Context</span></span>
<span data-ttu-id="293d5-125">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="293d5-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="293d5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293d5-126">-DefaultProfile</span></span>
<span data-ttu-id="293d5-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="293d5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="293d5-128">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="293d5-128">-Destination</span></span>
<span data-ttu-id="293d5-129">Ścieżka lokalnego pliku docelowego.</span><span class="sxs-lookup"><span data-stu-id="293d5-129">Destination local file path.</span></span>

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

### <span data-ttu-id="293d5-130">— System plików</span><span class="sxs-lookup"><span data-stu-id="293d5-130">-FileSystem</span></span>
<span data-ttu-id="293d5-131">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="293d5-131">FileSystem name</span></span>

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

### <span data-ttu-id="293d5-132">-Force</span><span class="sxs-lookup"><span data-stu-id="293d5-132">-Force</span></span>
<span data-ttu-id="293d5-133">Wymuś zastąpienie istniejącego obiektu BLOB lub pliku</span><span class="sxs-lookup"><span data-stu-id="293d5-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="293d5-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="293d5-134">-InputObject</span></span>
<span data-ttu-id="293d5-135">Obiekt usługi Azure datalake Gen2 do pobrania.</span><span class="sxs-lookup"><span data-stu-id="293d5-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="293d5-136">-Path</span><span class="sxs-lookup"><span data-stu-id="293d5-136">-Path</span></span>
<span data-ttu-id="293d5-137">Ścieżka w określonym systemie plików, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="293d5-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="293d5-138">Może to być plik lub katalog w formacie "Directory/file.txt" lub "directory1/Directory2/"</span><span class="sxs-lookup"><span data-stu-id="293d5-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="293d5-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="293d5-139">-Confirm</span></span>
<span data-ttu-id="293d5-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="293d5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="293d5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="293d5-141">-WhatIf</span></span>
<span data-ttu-id="293d5-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="293d5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="293d5-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="293d5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="293d5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293d5-144">CommonParameters</span></span>
<span data-ttu-id="293d5-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293d5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293d5-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293d5-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293d5-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="293d5-147">INPUTS</span></span>

### <span data-ttu-id="293d5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="293d5-148">System.String</span></span>

### <span data-ttu-id="293d5-149">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="293d5-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="293d5-150">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="293d5-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="293d5-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="293d5-151">OUTPUTS</span></span>

### <span data-ttu-id="293d5-152">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="293d5-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="293d5-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="293d5-153">NOTES</span></span>

## <span data-ttu-id="293d5-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="293d5-154">RELATED LINKS</span></span>
