---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221541"
---
# <span data-ttu-id="faa26-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="faa26-101">Add-AzVhd</span></span>

## <span data-ttu-id="faa26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="faa26-102">SYNOPSIS</span></span>
<span data-ttu-id="faa26-103">Umożliwia przekazywanie wirtualnego dysku twardego z lokalnej maszyny wirtualnej do obiektu BLOB na koncie magazynu w chmurze na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="faa26-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="faa26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="faa26-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faa26-105">Opis</span><span class="sxs-lookup"><span data-stu-id="faa26-105">DESCRIPTION</span></span>
<span data-ttu-id="faa26-106">Polecenie cmdlet **Add-AzVhd** umożliwia przekazywanie lokalnych wirtualnych dysków twardych w formacie pliku VHD do konta magazynu obiektów BLOB jako wirtualnych dysków twardych.</span><span class="sxs-lookup"><span data-stu-id="faa26-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="faa26-107">Możesz skonfigurować liczbę wątków przekazujący, które będą używane lub zastępować istniejący obiekt BLOB w określonym docelowym identyfikatorze URI.</span><span class="sxs-lookup"><span data-stu-id="faa26-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="faa26-108">Obsługiwane są również możliwości przekazywania wersji z poprawki do pliku VHD lokalnego.</span><span class="sxs-lookup"><span data-stu-id="faa26-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="faa26-109">Po przekazaniu podstawowego wirtualnego dysku twardego już można przekazać dyski różnicowe, które używają podstawowego obrazu jako elementu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="faa26-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="faa26-110">Jest obsługiwany także identyfikator URI (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="faa26-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="faa26-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="faa26-111">EXAMPLES</span></span>

### <span data-ttu-id="faa26-112">Przykład 1: Dodawanie pliku VHD</span><span class="sxs-lookup"><span data-stu-id="faa26-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="faa26-113">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="faa26-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="faa26-114">Przykład 2: Dodawanie pliku VHD i zastępowanie miejsca docelowego</span><span class="sxs-lookup"><span data-stu-id="faa26-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="faa26-115">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="faa26-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="faa26-116">Polecenie zastępuje istniejący plik.</span><span class="sxs-lookup"><span data-stu-id="faa26-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="faa26-117">Przykład 3: Dodawanie pliku VHD i Określanie liczby wątków</span><span class="sxs-lookup"><span data-stu-id="faa26-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="faa26-118">To polecenie powoduje dodanie pliku VHD do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="faa26-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="faa26-119">Polecenie określa liczbę wątków, które mają być używane do przekazania pliku.</span><span class="sxs-lookup"><span data-stu-id="faa26-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="faa26-120">Przykład 4: Dodawanie pliku VHD i Określanie identyfikatora URI SAS</span><span class="sxs-lookup"><span data-stu-id="faa26-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="faa26-121">To polecenie umożliwia dodanie pliku VHD do konta magazynu i określenie identyfikatora URI SAS.</span><span class="sxs-lookup"><span data-stu-id="faa26-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="faa26-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="faa26-122">PARAMETERS</span></span>

### <span data-ttu-id="faa26-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="faa26-123">-AsJob</span></span>
<span data-ttu-id="faa26-124">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="faa26-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="faa26-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="faa26-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="faa26-126">Określa identyfikator URI podstawowego obiektu BLOB obrazu w usłudze Azure Blob Storage.</span><span class="sxs-lookup"><span data-stu-id="faa26-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="faa26-127">Jako wartość tego parametru można określić skojarzenia zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="faa26-127">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faa26-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa26-128">-DefaultProfile</span></span>
<span data-ttu-id="faa26-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="faa26-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faa26-130">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="faa26-130">-Destination</span></span>
<span data-ttu-id="faa26-131">Określa identyfikator URI obiektu BLOB w magazynie obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="faa26-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="faa26-132">Parametr obsługuje identyfikator URI SAS, chociaż miejsce docelowe scenariuszy poprawek nie może być identyfikatorem URI SAS.</span><span class="sxs-lookup"><span data-stu-id="faa26-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faa26-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="faa26-133">-LocalFilePath</span></span>
<span data-ttu-id="faa26-134">Określa ścieżkę lokalnego pliku VHD.</span><span class="sxs-lookup"><span data-stu-id="faa26-134">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faa26-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="faa26-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="faa26-136">Określa liczbę wątków przekazujący, które mają być używane podczas przekazywania pliku VHD.</span><span class="sxs-lookup"><span data-stu-id="faa26-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faa26-137">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="faa26-137">-OverWrite</span></span>
<span data-ttu-id="faa26-138">Wskazuje, że to polecenie cmdlet zastąpi istniejący obiekt BLOB w określonym docelowym identyfikatorze URI, jeśli taki istnieje.</span><span class="sxs-lookup"><span data-stu-id="faa26-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faa26-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa26-139">-ResourceGroupName</span></span>
<span data-ttu-id="faa26-140">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="faa26-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faa26-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa26-141">CommonParameters</span></span>
<span data-ttu-id="faa26-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa26-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa26-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faa26-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa26-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="faa26-144">INPUTS</span></span>

### <span data-ttu-id="faa26-145">System. String</span><span class="sxs-lookup"><span data-stu-id="faa26-145">System.String</span></span>

### <span data-ttu-id="faa26-146">System. URI</span><span class="sxs-lookup"><span data-stu-id="faa26-146">System.Uri</span></span>

### <span data-ttu-id="faa26-147">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="faa26-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="faa26-148">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="faa26-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="faa26-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="faa26-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="faa26-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="faa26-150">OUTPUTS</span></span>

### <span data-ttu-id="faa26-151">Microsoft. Azure. Commands. COMPUTE. models. VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="faa26-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="faa26-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="faa26-152">NOTES</span></span>

## <span data-ttu-id="faa26-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="faa26-153">RELATED LINKS</span></span>

[<span data-ttu-id="faa26-154">Zapisz — AzVhd</span><span class="sxs-lookup"><span data-stu-id="faa26-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


