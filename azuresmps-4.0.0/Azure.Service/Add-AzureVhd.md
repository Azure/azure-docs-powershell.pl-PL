---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054684"
---
# <span data-ttu-id="0a3dd-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="0a3dd-101">Add-AzureVhd</span></span>

## <span data-ttu-id="0a3dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a3dd-103">Umożliwia przekazywanie pliku VHD z komputera lokalnego do obiektu BLOB na koncie magazynu w chmurze na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="0a3dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a3dd-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0a3dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a3dd-105">DESCRIPTION</span></span>
<span data-ttu-id="0a3dd-106">Polecenie cmdlet **Add-AzureVhd** umożliwia przekazywanie danych z lokalnego obrazu wirtualnego dysku twardego (VHD) na konto magazynu obiektów BLOB jako naprawione obrazy VHD.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="0a3dd-107">Zawiera parametry umożliwiające skonfigurowanie procesu przekazywania, takie jak określenie liczby wątków przekazujący, które będą używane lub zastępowaniem obiektu BLOB, który już istnieje w określonym docelowym identyfikatorze URI.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="0a3dd-108">W przypadku obrazów lokalnego dysku VHD scenariusz poprawiania jest również obsługiwany, aby można było przekazać różnicowe obrazy dysków bez konieczności przekazywania już przekazanych obrazów podstawowych.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="0a3dd-109">Jest też obsługiwany identyfikator URI (Shared Access Signature, SAS).</span><span class="sxs-lookup"><span data-stu-id="0a3dd-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="0a3dd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a3dd-110">EXAMPLES</span></span>

### <span data-ttu-id="0a3dd-111">Przykład 1: Dodawanie pliku VHD</span><span class="sxs-lookup"><span data-stu-id="0a3dd-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="0a3dd-112">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="0a3dd-113">Przykład 2: Dodawanie pliku VHD i zastępowanie miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="0a3dd-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="0a3dd-114">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="0a3dd-115">Przykład 3: Dodawanie pliku VHD i Określanie liczby wątków</span><span class="sxs-lookup"><span data-stu-id="0a3dd-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="0a3dd-116">To polecenie umożliwia dodanie pliku VHD do konta magazynu i określenie liczby wątków, które mają zostać użyte do przekazania pliku.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="0a3dd-117">Przykład 4: Dodawanie pliku VHD i Określanie identyfikatora URI SAS</span><span class="sxs-lookup"><span data-stu-id="0a3dd-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="0a3dd-118">To polecenie umożliwia dodanie pliku VHD do konta magazynu i określenie identyfikatora URI SAS.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="0a3dd-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a3dd-119">PARAMETERS</span></span>

### <span data-ttu-id="0a3dd-120">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="0a3dd-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="0a3dd-121">Określa identyfikator URI podstawowego obiektu BLOB obrazu w usłudze Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="0a3dd-122">Obsługiwane są również skojarzenia zabezpieczeń w danych wejściowych URI.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-122">SAS in URI input is supported as well.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a3dd-123">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="0a3dd-123">-Destination</span></span>
<span data-ttu-id="0a3dd-124">Określa identyfikator URI do obiektu BLOB w magazynie obiektów blob platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="0a3dd-125">Obsługiwane są skojarzenia zabezpieczeń w wejściowych identyfikatorze URI.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="0a3dd-126">Jednak w scenariuszach poprawiania lokalizacja docelowa nie może być identyfikatorem URI SAS.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a3dd-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0a3dd-127">-InformationAction</span></span>
<span data-ttu-id="0a3dd-128">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0a3dd-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0a3dd-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a3dd-130">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="0a3dd-130">Continue</span></span>
- <span data-ttu-id="0a3dd-131">Ignorować</span><span class="sxs-lookup"><span data-stu-id="0a3dd-131">Ignore</span></span>
- <span data-ttu-id="0a3dd-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="0a3dd-132">Inquire</span></span>
- <span data-ttu-id="0a3dd-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0a3dd-133">SilentlyContinue</span></span>
- <span data-ttu-id="0a3dd-134">Przestaw</span><span class="sxs-lookup"><span data-stu-id="0a3dd-134">Stop</span></span>
- <span data-ttu-id="0a3dd-135">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="0a3dd-135">Suspend</span></span>

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

### <span data-ttu-id="0a3dd-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0a3dd-136">-InformationVariable</span></span>
<span data-ttu-id="0a3dd-137">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0a3dd-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="0a3dd-138">-LocalFilePath</span></span>
<span data-ttu-id="0a3dd-139">Gatunek ścieżka pliku lokalnego pliku VHD.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-139">Species the file path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a3dd-140">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="0a3dd-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="0a3dd-141">Określa liczbę wątków, które mają być używane do przekazywania.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-141">Specifies the number of threads to use for upload.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a3dd-142">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="0a3dd-142">-OverWrite</span></span>
<span data-ttu-id="0a3dd-143">Określa, że to polecenie cmdlet usuwa istniejący obiekt BLOB w określonym docelowym identyfikatorze URI, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

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

### <span data-ttu-id="0a3dd-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="0a3dd-144">-Profile</span></span>
<span data-ttu-id="0a3dd-145">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0a3dd-146">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0a3dd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a3dd-147">CommonParameters</span></span>
<span data-ttu-id="0a3dd-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a3dd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a3dd-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a3dd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a3dd-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a3dd-150">INPUTS</span></span>

## <span data-ttu-id="0a3dd-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a3dd-151">OUTPUTS</span></span>

## <span data-ttu-id="0a3dd-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a3dd-152">NOTES</span></span>

## <span data-ttu-id="0a3dd-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a3dd-153">RELATED LINKS</span></span>

[<span data-ttu-id="0a3dd-154">Zapisz — AzureVhd</span><span class="sxs-lookup"><span data-stu-id="0a3dd-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


