---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 7faa179ae8c8c43d750e4f042f7bc925b772f4e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544535"
---
# <span data-ttu-id="7366b-101">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="7366b-101">Add-AzureRmVhd</span></span>

## <span data-ttu-id="7366b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7366b-102">SYNOPSIS</span></span>
<span data-ttu-id="7366b-103">Umożliwia przekazywanie wirtualnego dysku twardego z lokalnej maszyny wirtualnej do obiektu BLOB na koncie magazynu w chmurze na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="7366b-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7366b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7366b-104">SYNTAX</span></span>

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [<CommonParameters>]
```

## <span data-ttu-id="7366b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7366b-105">DESCRIPTION</span></span>
<span data-ttu-id="7366b-106">Polecenie cmdlet **Add-AzureRmVhd** umożliwia przekazywanie lokalnych wirtualnych dysków twardych w formacie pliku VHD do konta magazynu obiektów BLOB jako wirtualnych dysków twardych.</span><span class="sxs-lookup"><span data-stu-id="7366b-106">The **Add-AzureRmVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="7366b-107">Możesz skonfigurować liczbę wątków przekazujący, które będą używane lub zastępować istniejący obiekt BLOB w określonym docelowym identyfikatorze URI.</span><span class="sxs-lookup"><span data-stu-id="7366b-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="7366b-108">Obsługiwane są również możliwości przekazywania wersji z poprawki do pliku VHD lokalnego.</span><span class="sxs-lookup"><span data-stu-id="7366b-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="7366b-109">Po przekazaniu podstawowego wirtualnego dysku twardego już można przekazać dyski różnicowe, które używają podstawowego obrazu jako elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="7366b-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="7366b-110">Jest obsługiwany także identyfikator URI (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="7366b-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="7366b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7366b-111">EXAMPLES</span></span>

### <span data-ttu-id="7366b-112">Przykład 1: Dodawanie pliku VHD</span><span class="sxs-lookup"><span data-stu-id="7366b-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="7366b-113">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7366b-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="7366b-114">Przykład 2: Dodawanie pliku VHD i zastępowanie miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="7366b-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="7366b-115">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7366b-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="7366b-116">Polecenie zastępuje istniejący plik.</span><span class="sxs-lookup"><span data-stu-id="7366b-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="7366b-117">Przykład 3: Dodawanie pliku VHD i Określanie liczby wątków</span><span class="sxs-lookup"><span data-stu-id="7366b-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="7366b-118">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="7366b-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="7366b-119">Polecenie określa liczbę wątków, które mają być używane do przekazania pliku.</span><span class="sxs-lookup"><span data-stu-id="7366b-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="7366b-120">Przykład 4: Dodawanie pliku VHD i Określanie identyfikatora URI SAS</span><span class="sxs-lookup"><span data-stu-id="7366b-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="7366b-121">To polecenie umożliwia dodanie pliku VHD do konta magazynu i określenie identyfikatora URI SAS.</span><span class="sxs-lookup"><span data-stu-id="7366b-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="7366b-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7366b-122">PARAMETERS</span></span>

### <span data-ttu-id="7366b-123">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="7366b-123">-BaseImageUriToPatch</span></span>
<span data-ttu-id="7366b-124">Określa identyfikator URI podstawowego obiektu BLOB obrazu w usłudze Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="7366b-124">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="7366b-125">Jako wartość tego parametru można określić skojarzenia zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="7366b-125">An SAS can be specified as the value for this parameter.</span></span>

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

### <span data-ttu-id="7366b-126">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="7366b-126">-Destination</span></span>
<span data-ttu-id="7366b-127">Określa identyfikator URI obiektu BLOB w magazynie obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="7366b-127">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="7366b-128">Parametr obsługuje identyfikator URI SAS, chociaż miejsce docelowe scenariuszy poprawek nie może być identyfikatorem URI SAS.</span><span class="sxs-lookup"><span data-stu-id="7366b-128">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

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

### <span data-ttu-id="7366b-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="7366b-129">-LocalFilePath</span></span>
<span data-ttu-id="7366b-130">Określa ścieżkę lokalnego pliku VHD.</span><span class="sxs-lookup"><span data-stu-id="7366b-130">Specifies the path of the local .vhd file.</span></span>

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

### <span data-ttu-id="7366b-131">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="7366b-131">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="7366b-132">Określa liczbę wątków przekazujący, które mają być używane podczas przekazywania pliku VHD.</span><span class="sxs-lookup"><span data-stu-id="7366b-132">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

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

### <span data-ttu-id="7366b-133">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="7366b-133">-OverWrite</span></span>
<span data-ttu-id="7366b-134">Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB w określonym docelowym identyfikatorze URI, jeśli taki istnieje.</span><span class="sxs-lookup"><span data-stu-id="7366b-134">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="7366b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7366b-135">-ResourceGroupName</span></span>
<span data-ttu-id="7366b-136">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7366b-136">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7366b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7366b-137">CommonParameters</span></span>
<span data-ttu-id="7366b-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7366b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7366b-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7366b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7366b-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7366b-140">INPUTS</span></span>

### <span data-ttu-id="7366b-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7366b-141">None</span></span>
<span data-ttu-id="7366b-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7366b-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7366b-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7366b-143">OUTPUTS</span></span>

## <span data-ttu-id="7366b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7366b-144">NOTES</span></span>

## <span data-ttu-id="7366b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7366b-145">RELATED LINKS</span></span>

[<span data-ttu-id="7366b-146">Zapisz — AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="7366b-146">Save-AzureRmVhd</span></span>](./Save-AzureRmVhd.md)


