---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: 28d38fd88bada5b1c73557ea0d85bacf8ab2b6c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893878"
---
# <span data-ttu-id="17ebe-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="17ebe-101">Add-AzVhd</span></span>

## <span data-ttu-id="17ebe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="17ebe-103">Umożliwia przekazywanie wirtualnego dysku twardego z lokalnej maszyny wirtualnej do obiektu BLOB na koncie magazynu w chmurze na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="17ebe-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="17ebe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17ebe-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17ebe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="17ebe-105">DESCRIPTION</span></span>
<span data-ttu-id="17ebe-106">Polecenie cmdlet **Add-AzVhd** umożliwia przekazywanie lokalnych wirtualnych dysków twardych w formacie pliku VHD do konta magazynu obiektów BLOB jako wirtualnych dysków twardych.</span><span class="sxs-lookup"><span data-stu-id="17ebe-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="17ebe-107">Możesz skonfigurować liczbę wątków przekazujący, które będą używane lub zastępować istniejący obiekt BLOB w określonym docelowym identyfikatorze URI.</span><span class="sxs-lookup"><span data-stu-id="17ebe-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="17ebe-108">Obsługiwane są również możliwości przekazywania wersji z poprawki do pliku VHD lokalnego.</span><span class="sxs-lookup"><span data-stu-id="17ebe-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="17ebe-109">Po przekazaniu podstawowego wirtualnego dysku twardego już można przekazać dyski różnicowe, które używają podstawowego obrazu jako elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="17ebe-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="17ebe-110">Jest obsługiwany także identyfikator URI (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="17ebe-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="17ebe-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17ebe-111">EXAMPLES</span></span>

### <span data-ttu-id="17ebe-112">Przykład 1: Dodawanie pliku VHD</span><span class="sxs-lookup"><span data-stu-id="17ebe-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="17ebe-113">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="17ebe-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="17ebe-114">Przykład 2: Dodawanie pliku VHD i zastępowanie miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="17ebe-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="17ebe-115">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="17ebe-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="17ebe-116">Polecenie zastępuje istniejący plik.</span><span class="sxs-lookup"><span data-stu-id="17ebe-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="17ebe-117">Przykład 3: Dodawanie pliku VHD i Określanie liczby wątków</span><span class="sxs-lookup"><span data-stu-id="17ebe-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="17ebe-118">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="17ebe-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="17ebe-119">Polecenie określa liczbę wątków, które mają być używane do przekazania pliku.</span><span class="sxs-lookup"><span data-stu-id="17ebe-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="17ebe-120">Przykład 4: Dodawanie pliku VHD i Określanie identyfikatora URI SAS</span><span class="sxs-lookup"><span data-stu-id="17ebe-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="17ebe-121">To polecenie umożliwia dodanie pliku VHD do konta magazynu i określenie identyfikatora URI SAS.</span><span class="sxs-lookup"><span data-stu-id="17ebe-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="17ebe-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17ebe-122">PARAMETERS</span></span>

### <span data-ttu-id="17ebe-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17ebe-123">-AsJob</span></span>
<span data-ttu-id="17ebe-124">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="17ebe-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="17ebe-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="17ebe-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="17ebe-126">Określa identyfikator URI podstawowego obiektu BLOB obrazu w usłudze Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="17ebe-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="17ebe-127">Jako wartość tego parametru można określić skojarzenia zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="17ebe-127">An SAS can be specified as the value for this parameter.</span></span>

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

### <span data-ttu-id="17ebe-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ebe-128">-DefaultProfile</span></span>
<span data-ttu-id="17ebe-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17ebe-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17ebe-130">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="17ebe-130">-Destination</span></span>
<span data-ttu-id="17ebe-131">Określa identyfikator URI obiektu BLOB w magazynie obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="17ebe-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="17ebe-132">Parametr obsługuje identyfikator URI SAS, chociaż miejsce docelowe scenariuszy poprawek nie może być identyfikatorem URI SAS.</span><span class="sxs-lookup"><span data-stu-id="17ebe-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

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

### <span data-ttu-id="17ebe-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="17ebe-133">-LocalFilePath</span></span>
<span data-ttu-id="17ebe-134">Określa ścieżkę lokalnego pliku VHD.</span><span class="sxs-lookup"><span data-stu-id="17ebe-134">Specifies the path of the local .vhd file.</span></span>

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

### <span data-ttu-id="17ebe-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="17ebe-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="17ebe-136">Określa liczbę wątków przekazujący, które mają być używane podczas przekazywania pliku VHD.</span><span class="sxs-lookup"><span data-stu-id="17ebe-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

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

### <span data-ttu-id="17ebe-137">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="17ebe-137">-OverWrite</span></span>
<span data-ttu-id="17ebe-138">Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB w określonym docelowym identyfikatorze URI, jeśli taki istnieje.</span><span class="sxs-lookup"><span data-stu-id="17ebe-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="17ebe-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ebe-139">-ResourceGroupName</span></span>
<span data-ttu-id="17ebe-140">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17ebe-140">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="17ebe-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ebe-141">CommonParameters</span></span>
<span data-ttu-id="17ebe-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17ebe-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ebe-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17ebe-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ebe-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17ebe-144">INPUTS</span></span>

### <span data-ttu-id="17ebe-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="17ebe-145">None</span></span>
<span data-ttu-id="17ebe-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="17ebe-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17ebe-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17ebe-147">OUTPUTS</span></span>

### <span data-ttu-id="17ebe-148">Microsoft. Azure. Commands. COMPUTE. models. VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="17ebe-148">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="17ebe-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17ebe-149">NOTES</span></span>

## <span data-ttu-id="17ebe-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17ebe-150">RELATED LINKS</span></span>

[<span data-ttu-id="17ebe-151">Zapisz — AzVhd</span><span class="sxs-lookup"><span data-stu-id="17ebe-151">Save-AzVhd</span></span>](./Save-AzVhd.md)


