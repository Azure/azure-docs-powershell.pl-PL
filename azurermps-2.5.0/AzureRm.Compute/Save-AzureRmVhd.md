---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
ms.openlocfilehash: 86a4cdb4fc0d6709d6cb9311d243f12dcb65e5de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899369"
---
# <span data-ttu-id="9fc79-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="9fc79-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="9fc79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fc79-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc79-103">Zapisuje pobrane obrazy VHD lokalnie.</span><span class="sxs-lookup"><span data-stu-id="9fc79-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fc79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fc79-104">SYNTAX</span></span>

### <span data-ttu-id="9fc79-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9fc79-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fc79-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9fc79-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fc79-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9fc79-107">DESCRIPTION</span></span>
<span data-ttu-id="9fc79-108">Polecenie cmdlet **Save-AzureRmVhd** zapisuje obrazy VHD z obiektu BLOB, w którym są one przechowywane do pliku.</span><span class="sxs-lookup"><span data-stu-id="9fc79-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="9fc79-109">Możesz określić liczbę wątków programu do pobierania plików, których używa proces, oraz czy zamienić plik, który już istnieje.</span><span class="sxs-lookup"><span data-stu-id="9fc79-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="9fc79-110">To polecenie cmdlet pobiera zawartość w taki sposób.</span><span class="sxs-lookup"><span data-stu-id="9fc79-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="9fc79-111">Nie dotyczy żadnych konwersji formatu wirtualnego dysku twardego (VHD).</span><span class="sxs-lookup"><span data-stu-id="9fc79-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="9fc79-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fc79-112">EXAMPLES</span></span>

### <span data-ttu-id="9fc79-113">Przykład 1: Pobieranie obrazu</span><span class="sxs-lookup"><span data-stu-id="9fc79-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="9fc79-114">To polecenie pobiera plik VHD i przechowuje go w ścieżce lokalnej C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="9fc79-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="9fc79-115">Przykład 2: Pobieranie obrazu i zastępowanie pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="9fc79-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="9fc79-116">To polecenie umożliwia pobranie pliku VHD i zapisanie go w ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="9fc79-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="9fc79-117">Polecenie zawiera parametr *Zastąp* .</span><span class="sxs-lookup"><span data-stu-id="9fc79-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="9fc79-118">Dlatego jeśli C:\vhd\Win7Image.vhd już istnieje, to polecenie zastępuje je.</span><span class="sxs-lookup"><span data-stu-id="9fc79-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="9fc79-119">Przykład 3: Pobieranie obrazu przy użyciu określonej liczby wątków</span><span class="sxs-lookup"><span data-stu-id="9fc79-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="9fc79-120">To polecenie umożliwia pobranie pliku VHD i zapisanie go w ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="9fc79-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="9fc79-121">Polecenie określa wartość 32 dla parametru *NumberOfThreads* .</span><span class="sxs-lookup"><span data-stu-id="9fc79-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="9fc79-122">Polecenie cmdlet używa więc wątków 32 dla tej akcji.</span><span class="sxs-lookup"><span data-stu-id="9fc79-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="9fc79-123">Przykład 4: Pobieranie obrazu i określanie klucza magazynu</span><span class="sxs-lookup"><span data-stu-id="9fc79-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="9fc79-124">To polecenie umożliwia pobranie pliku VHD i określenie klucza magazynu.</span><span class="sxs-lookup"><span data-stu-id="9fc79-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="9fc79-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fc79-125">PARAMETERS</span></span>

### <span data-ttu-id="9fc79-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fc79-126">-AsJob</span></span>
<span data-ttu-id="9fc79-127">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="9fc79-127">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc79-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc79-128">-DefaultProfile</span></span>
<span data-ttu-id="9fc79-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc79-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc79-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="9fc79-130">-LocalFilePath</span></span>
<span data-ttu-id="9fc79-131">Określa ścieżkę lokalnego pliku zapisanego obrazu.</span><span class="sxs-lookup"><span data-stu-id="9fc79-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc79-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="9fc79-132">-NumberOfThreads</span></span>
<span data-ttu-id="9fc79-133">Określa liczbę wątków pobierania, które są używane podczas pobierania tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc79-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc79-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="9fc79-134">-OverWrite</span></span>
<span data-ttu-id="9fc79-135">Wskazuje, że to polecenie cmdlet zastępuje plik określony przez plik *LocalFilePath* , jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="9fc79-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc79-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc79-136">-ResourceGroupName</span></span>
<span data-ttu-id="9fc79-137">Określa nazwę grupy zasobów konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9fc79-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fc79-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="9fc79-138">-SourceUri</span></span>
<span data-ttu-id="9fc79-139">Określa identyfikator URI (Uniform Resource Identifier) obiektu BLOB `Azure` .</span><span class="sxs-lookup"><span data-stu-id="9fc79-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fc79-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="9fc79-140">-StorageKey</span></span>
<span data-ttu-id="9fc79-141">Określa klucz magazynu konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="9fc79-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="9fc79-142">Jeśli nie podano klucza, to polecenie cmdlet próbuje ustalić klucz magazynu konta w usłudze *SourceUri* na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc79-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc79-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc79-143">CommonParameters</span></span>
<span data-ttu-id="9fc79-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc79-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc79-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fc79-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc79-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fc79-146">INPUTS</span></span>

### <span data-ttu-id="9fc79-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9fc79-147">None</span></span>
<span data-ttu-id="9fc79-148">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9fc79-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fc79-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fc79-149">OUTPUTS</span></span>

### <span data-ttu-id="9fc79-150">Microsoft. Azure. Commands. COMPUTE. models. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="9fc79-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="9fc79-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fc79-151">NOTES</span></span>

## <span data-ttu-id="9fc79-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fc79-152">RELATED LINKS</span></span>

[<span data-ttu-id="9fc79-153">Dodaj-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="9fc79-153">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)


