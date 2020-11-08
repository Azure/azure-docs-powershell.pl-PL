---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054427"
---
# <span data-ttu-id="31de0-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="31de0-101">Save-AzureVhd</span></span>

## <span data-ttu-id="31de0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31de0-102">SYNOPSIS</span></span>
<span data-ttu-id="31de0-103">Umożliwia pobieranie obrazów VHD.</span><span class="sxs-lookup"><span data-stu-id="31de0-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="31de0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31de0-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="31de0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31de0-105">DESCRIPTION</span></span>
<span data-ttu-id="31de0-106">Polecenie cmdlet **Save-AzureVhd** umożliwia pobieranie obrazów VHD z obiektu BLOB, w którym są one przechowywane do pliku.</span><span class="sxs-lookup"><span data-stu-id="31de0-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="31de0-107">Zawiera parametry konfigurowania procesu pobierania przez określenie liczby używanych lub zastępowania plików, które już istnieją w określonej ścieżce pliku.</span><span class="sxs-lookup"><span data-stu-id="31de0-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="31de0-108">Funkcja **Save-AzureVhd** nie wykonuje żadnej konwersji formatu VHD, a obiekt BLOB jest pobierany.</span><span class="sxs-lookup"><span data-stu-id="31de0-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="31de0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31de0-109">EXAMPLES</span></span>

### <span data-ttu-id="31de0-110">Przykład 1: Pobieranie pliku VHD</span><span class="sxs-lookup"><span data-stu-id="31de0-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="31de0-111">To polecenie pobiera plik VHD.</span><span class="sxs-lookup"><span data-stu-id="31de0-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="31de0-112">Przykład 2: Pobieranie pliku VHD i zastępowanie pliku lokalnego</span><span class="sxs-lookup"><span data-stu-id="31de0-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="31de0-113">To polecenie pobiera plik VHD i zastępuje dowolny plik w ścieżce docelowej.</span><span class="sxs-lookup"><span data-stu-id="31de0-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="31de0-114">Przykład 3: Pobieranie pliku VHD i Określanie liczby wątków</span><span class="sxs-lookup"><span data-stu-id="31de0-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="31de0-115">To polecenie pobiera plik VHD i określa liczbę wątków.</span><span class="sxs-lookup"><span data-stu-id="31de0-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="31de0-116">Przykład 4: Pobieranie pliku VHD i określanie klucza magazynu</span><span class="sxs-lookup"><span data-stu-id="31de0-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="31de0-117">To polecenie umożliwia pobranie pliku VHD i określenie klucza magazynu.</span><span class="sxs-lookup"><span data-stu-id="31de0-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="31de0-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31de0-118">PARAMETERS</span></span>

### <span data-ttu-id="31de0-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="31de0-119">-InformationAction</span></span>
<span data-ttu-id="31de0-120">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="31de0-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="31de0-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="31de0-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31de0-122">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="31de0-122">Continue</span></span>
- <span data-ttu-id="31de0-123">Ignorować</span><span class="sxs-lookup"><span data-stu-id="31de0-123">Ignore</span></span>
- <span data-ttu-id="31de0-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="31de0-124">Inquire</span></span>
- <span data-ttu-id="31de0-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="31de0-125">SilentlyContinue</span></span>
- <span data-ttu-id="31de0-126">Przestaw</span><span class="sxs-lookup"><span data-stu-id="31de0-126">Stop</span></span>
- <span data-ttu-id="31de0-127">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="31de0-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31de0-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="31de0-128">-InformationVariable</span></span>
<span data-ttu-id="31de0-129">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="31de0-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31de0-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="31de0-130">-LocalFilePath</span></span>
<span data-ttu-id="31de0-131">Określa ścieżkę pliku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="31de0-131">Specifies the local file path.</span></span>

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

### <span data-ttu-id="31de0-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="31de0-132">-NumberOfThreads</span></span>
<span data-ttu-id="31de0-133">Określa liczbę wątków pobierania, które są używane podczas pobierania tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31de0-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="31de0-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="31de0-134">-OverWrite</span></span>
<span data-ttu-id="31de0-135">Określa, że to polecenie cmdlet usunie plik określony przez plik *LocalFilePath* , jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="31de0-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31de0-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="31de0-136">-Profile</span></span>
<span data-ttu-id="31de0-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31de0-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31de0-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="31de0-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31de0-139">-Source</span><span class="sxs-lookup"><span data-stu-id="31de0-139">-Source</span></span>
<span data-ttu-id="31de0-140">Określa identyfikator URI (Uniform Resource Identifier) do obiektu BLOB `Azure` .</span><span class="sxs-lookup"><span data-stu-id="31de0-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31de0-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="31de0-141">-StorageKey</span></span>
<span data-ttu-id="31de0-142">Określa klucz magazynu konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="31de0-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="31de0-143">Jeśli nie jest podany, usługa **Save-AzureVhd** próbuje określić klucz magazynu konta w usłudze *SourceUri* na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="31de0-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31de0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31de0-144">CommonParameters</span></span>
<span data-ttu-id="31de0-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31de0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31de0-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31de0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31de0-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31de0-147">INPUTS</span></span>

## <span data-ttu-id="31de0-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31de0-148">OUTPUTS</span></span>

## <span data-ttu-id="31de0-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31de0-149">NOTES</span></span>

## <span data-ttu-id="31de0-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31de0-150">RELATED LINKS</span></span>

[<span data-ttu-id="31de0-151">Dodaj-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="31de0-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


