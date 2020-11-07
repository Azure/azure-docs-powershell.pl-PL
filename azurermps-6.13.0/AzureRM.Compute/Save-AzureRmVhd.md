---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: db2148be139130f5963214c5e66809a3e66a22ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548827"
---
# <span data-ttu-id="98e64-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="98e64-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="98e64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98e64-102">SYNOPSIS</span></span>
<span data-ttu-id="98e64-103">Zapisuje pobrane obrazy VHD lokalnie.</span><span class="sxs-lookup"><span data-stu-id="98e64-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98e64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98e64-104">SYNTAX</span></span>

### <span data-ttu-id="98e64-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="98e64-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98e64-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="98e64-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98e64-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98e64-107">DESCRIPTION</span></span>
<span data-ttu-id="98e64-108">Polecenie cmdlet **Save-AzureRmVhd** zapisuje obrazy VHD z obiektu BLOB, w którym są one przechowywane do pliku.</span><span class="sxs-lookup"><span data-stu-id="98e64-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="98e64-109">Możesz określić liczbę wątków programu do pobierania plików, których używa proces, oraz czy zamienić plik, który już istnieje.</span><span class="sxs-lookup"><span data-stu-id="98e64-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="98e64-110">To polecenie cmdlet pobiera zawartość w taki sposób.</span><span class="sxs-lookup"><span data-stu-id="98e64-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="98e64-111">Nie dotyczy żadnych konwersji formatu wirtualnego dysku twardego (VHD).</span><span class="sxs-lookup"><span data-stu-id="98e64-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="98e64-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98e64-112">EXAMPLES</span></span>

### <span data-ttu-id="98e64-113">Przykład 1: Pobieranie obrazu</span><span class="sxs-lookup"><span data-stu-id="98e64-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="98e64-114">To polecenie pobiera plik VHD i przechowuje go w ścieżce lokalnej C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="98e64-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="98e64-115">Przykład 2: Pobieranie obrazu i zastępowanie pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="98e64-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="98e64-116">To polecenie umożliwia pobranie pliku VHD i zapisanie go w ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="98e64-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="98e64-117">Polecenie zawiera parametr *Zastąp* .</span><span class="sxs-lookup"><span data-stu-id="98e64-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="98e64-118">Dlatego jeśli C:\vhd\Win7Image.vhd już istnieje, to polecenie zastępuje je.</span><span class="sxs-lookup"><span data-stu-id="98e64-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="98e64-119">Przykład 3: Pobieranie obrazu przy użyciu określonej liczby wątków</span><span class="sxs-lookup"><span data-stu-id="98e64-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="98e64-120">To polecenie umożliwia pobranie pliku VHD i zapisanie go w ścieżce lokalnej.</span><span class="sxs-lookup"><span data-stu-id="98e64-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="98e64-121">Polecenie określa wartość 32 dla parametru *NumberOfThreads* .</span><span class="sxs-lookup"><span data-stu-id="98e64-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="98e64-122">Polecenie cmdlet używa więc wątków 32 dla tej akcji.</span><span class="sxs-lookup"><span data-stu-id="98e64-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="98e64-123">Przykład 4: Pobieranie obrazu i określanie klucza magazynu</span><span class="sxs-lookup"><span data-stu-id="98e64-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="98e64-124">To polecenie umożliwia pobranie pliku VHD i określenie klucza magazynu.</span><span class="sxs-lookup"><span data-stu-id="98e64-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="98e64-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98e64-125">PARAMETERS</span></span>

### <span data-ttu-id="98e64-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98e64-126">-AsJob</span></span>
<span data-ttu-id="98e64-127">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="98e64-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="98e64-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e64-128">-DefaultProfile</span></span>
<span data-ttu-id="98e64-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98e64-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e64-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="98e64-130">-LocalFilePath</span></span>
<span data-ttu-id="98e64-131">Określa ścieżkę lokalnego pliku zapisanego obrazu.</span><span class="sxs-lookup"><span data-stu-id="98e64-131">Specifies the local file path of the saved image.</span></span>

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

### <span data-ttu-id="98e64-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="98e64-132">-NumberOfThreads</span></span>
<span data-ttu-id="98e64-133">Określa liczbę wątków pobierania, które są używane podczas pobierania tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98e64-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="98e64-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="98e64-134">-OverWrite</span></span>
<span data-ttu-id="98e64-135">Wskazuje, że to polecenie cmdlet zastępuje plik określony przez plik *LocalFilePath* , jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="98e64-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="98e64-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98e64-136">-ResourceGroupName</span></span>
<span data-ttu-id="98e64-137">Określa nazwę grupy zasobów konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="98e64-137">Specifies the name of the resource group of the storage account.</span></span>

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

### <span data-ttu-id="98e64-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="98e64-138">-SourceUri</span></span>
<span data-ttu-id="98e64-139">Określa identyfikator URI (Uniform Resource Identifier) obiektu BLOB `Azure` .</span><span class="sxs-lookup"><span data-stu-id="98e64-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

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

### <span data-ttu-id="98e64-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="98e64-140">-StorageKey</span></span>
<span data-ttu-id="98e64-141">Określa klucz magazynu konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="98e64-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="98e64-142">Jeśli nie podano klucza, to polecenie cmdlet próbuje ustalić klucz magazynu konta w usłudze *SourceUri* na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="98e64-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

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

### <span data-ttu-id="98e64-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e64-143">CommonParameters</span></span>
<span data-ttu-id="98e64-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98e64-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e64-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98e64-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e64-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98e64-146">INPUTS</span></span>

### <span data-ttu-id="98e64-147">System. String</span><span class="sxs-lookup"><span data-stu-id="98e64-147">System.String</span></span>

### <span data-ttu-id="98e64-148">System. URI</span><span class="sxs-lookup"><span data-stu-id="98e64-148">System.Uri</span></span>

## <span data-ttu-id="98e64-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98e64-149">OUTPUTS</span></span>

### <span data-ttu-id="98e64-150">Microsoft. Azure. Commands. COMPUTE. models. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="98e64-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="98e64-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98e64-151">NOTES</span></span>

## <span data-ttu-id="98e64-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98e64-152">RELATED LINKS</span></span>

[<span data-ttu-id="98e64-153">Dodaj-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="98e64-153">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)

