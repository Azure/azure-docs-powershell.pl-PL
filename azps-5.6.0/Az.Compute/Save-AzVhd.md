---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: 4a88fe1e4bc18aaa31222b2f5d8e2a90629984d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972097"
---
# <span data-ttu-id="7d8d6-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="7d8d6-101">Save-AzVhd</span></span>

## <span data-ttu-id="7d8d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8d6-103">Zapisuje pobrane obrazy vhd lokalnie.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="7d8d6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7d8d6-104">SYNTAX</span></span>

### <span data-ttu-id="7d8d6-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7d8d6-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d8d6-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7d8d6-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d8d6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7d8d6-107">DESCRIPTION</span></span>
<span data-ttu-id="7d8d6-108">Polecenie **cmdlet Save-AzVhd** zapisuje obrazy vhd z obiektu blob, w którym są przechowywane w pliku.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="7d8d6-109">Możesz określić liczbę wątków pobieracza, które są używane w procesie, oraz określić, czy zamienić już istnieje plik.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="7d8d6-110">To polecenie cmdlet pobiera zawartość w takiej, w jaka jest.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="7d8d6-111">Nie ma zastosowania konwersji w formacie wirtualnego dysku twardego (VHD).</span><span class="sxs-lookup"><span data-stu-id="7d8d6-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="7d8d6-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7d8d6-112">EXAMPLES</span></span>

### <span data-ttu-id="7d8d6-113">Przykład 1. Pobieranie obrazu</span><span class="sxs-lookup"><span data-stu-id="7d8d6-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="7d8d6-114">To polecenie pobiera plik vhd i zapisuje go w ścieżce lokalnej C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="7d8d6-115">Przykład 2. Pobieranie obrazu i zastępowanie pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="7d8d6-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="7d8d6-116">To polecenie pobiera plik vhd i zapisuje go w ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="7d8d6-117">To polecenie zawiera parametr *Zastąp.*</span><span class="sxs-lookup"><span data-stu-id="7d8d6-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="7d8d6-118">Dlatego jeśli C:\vhd\Win7Image.vhd już istnieje, to polecenie zastępuje je.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="7d8d6-119">Przykład 3. Pobieranie obrazu przy użyciu określonej liczby wątków</span><span class="sxs-lookup"><span data-stu-id="7d8d6-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="7d8d6-120">To polecenie pobiera plik vhd i zapisuje go w ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="7d8d6-121">To polecenie określa wartość 32 dla *parametru NumberOfThreads.*</span><span class="sxs-lookup"><span data-stu-id="7d8d6-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="7d8d6-122">Dlatego polecenie cmdlet używa 32 wątków dla tej akcji.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="7d8d6-123">Przykład 4. Pobieranie obrazu i określanie klucza magazynu</span><span class="sxs-lookup"><span data-stu-id="7d8d6-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="7d8d6-124">To polecenie powoduje pobranie pliku vhd i określenie klucza magazynu.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="7d8d6-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d8d6-125">PARAMETERS</span></span>

### <span data-ttu-id="7d8d6-126">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7d8d6-126">-AsJob</span></span>
<span data-ttu-id="7d8d6-127">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7d8d6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8d6-128">-DefaultProfile</span></span>
<span data-ttu-id="7d8d6-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d8d6-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="7d8d6-130">-LocalFilePath</span></span>
<span data-ttu-id="7d8d6-131">Określa lokalną ścieżkę pliku zapisanego obrazu.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d6-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="7d8d6-132">-NumberOfThreads</span></span>
<span data-ttu-id="7d8d6-133">Określa liczbę wątków pobierania, których używa to polecenie cmdlet podczas pobierania.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d6-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="7d8d6-134">-OverWrite</span></span>
<span data-ttu-id="7d8d6-135">Wskazuje, że to polecenie cmdlet zastępuje plik określony przez plik *LocalFilePath,* jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8d6-136">-ResourceGroupName</span></span>
<span data-ttu-id="7d8d6-137">Określa nazwę grupy zasobów konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d6-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="7d8d6-138">-SourceUri</span></span>
<span data-ttu-id="7d8d6-139">Określa identyfikator URI obiektu blob `Azure` w.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d6-140">- KluczDazydzydów</span><span class="sxs-lookup"><span data-stu-id="7d8d6-140">-StorageKey</span></span>
<span data-ttu-id="7d8d6-141">Określa klucz magazynu konta magazynu obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="7d8d6-142">Jeśli nie określisz klucza, to polecenie cmdlet podejmie próbę określenia klucza magazynu konta w *sourceuri* na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8d6-143">CommonParameters</span></span>
<span data-ttu-id="7d8d6-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8d6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8d6-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d8d6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8d6-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d8d6-146">INPUTS</span></span>

### <span data-ttu-id="7d8d6-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7d8d6-147">System.String</span></span>

### <span data-ttu-id="7d8d6-148">System.Uri</span><span class="sxs-lookup"><span data-stu-id="7d8d6-148">System.Uri</span></span>

## <span data-ttu-id="7d8d6-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d8d6-149">OUTPUTS</span></span>

### <span data-ttu-id="7d8d6-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="7d8d6-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="7d8d6-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7d8d6-151">NOTES</span></span>

## <span data-ttu-id="7d8d6-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d8d6-152">RELATED LINKS</span></span>

[<span data-ttu-id="7d8d6-153">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="7d8d6-153">Add-AzVhd</span></span>](./Add-AzVhd.md)


