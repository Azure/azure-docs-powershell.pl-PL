---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: 7c0f89d9c33dca961b822de62c05158a53195767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552996"
---
# <span data-ttu-id="f9173-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="f9173-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="f9173-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9173-102">SYNOPSIS</span></span>
<span data-ttu-id="f9173-103">Tworzy obiekt z obrazem konfigurowalnym.</span><span class="sxs-lookup"><span data-stu-id="f9173-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9173-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9173-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9173-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9173-105">DESCRIPTION</span></span>
<span data-ttu-id="f9173-106">Polecenie cmdlet **New-AzureRmImageConfig** tworzy obiekt z obrazem konfigurowalnym.</span><span class="sxs-lookup"><span data-stu-id="f9173-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="f9173-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9173-107">EXAMPLES</span></span>

### <span data-ttu-id="f9173-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9173-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="f9173-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="f9173-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="f9173-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek do dysków systemu operacyjnego i dwóch dysków z danymi do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="f9173-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="f9173-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="f9173-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="f9173-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="f9173-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="f9173-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="f9173-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="f9173-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f9173-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f9173-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9173-115">PARAMETERS</span></span>

### <span data-ttu-id="f9173-116">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="f9173-116">-DataDisk</span></span>
<span data-ttu-id="f9173-117">Określa obiekt dysk danych.</span><span class="sxs-lookup"><span data-stu-id="f9173-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9173-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f9173-118">-Location</span></span>
<span data-ttu-id="f9173-119">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="f9173-119">Specifies a location.</span></span>

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

### <span data-ttu-id="f9173-120">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="f9173-120">-OsDisk</span></span>
<span data-ttu-id="f9173-121">Określa dysk systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="f9173-121">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9173-122">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f9173-122">-SourceVirtualMachineId</span></span>
<span data-ttu-id="f9173-123">Określa identyfikator źródłowego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f9173-123">Specifies the source virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9173-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9173-124">-Tag</span></span>
<span data-ttu-id="f9173-125">Określa, że zasoby i grupy zasobów mogą być znakowane za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="f9173-125">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9173-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9173-126">-Confirm</span></span>
<span data-ttu-id="f9173-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9173-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9173-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9173-128">-WhatIf</span></span>
<span data-ttu-id="f9173-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9173-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9173-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9173-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9173-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9173-131">CommonParameters</span></span>
<span data-ttu-id="f9173-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9173-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9173-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9173-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9173-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9173-134">INPUTS</span></span>

### <span data-ttu-id="f9173-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f9173-135">System.String</span></span>
<span data-ttu-id="f9173-136">System. Collections. Hashtable Microsoft. Azure. Management. COMPUTE. models. ImageOSDisk Microsoft. Azure. Management. COMPUTE. models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="f9173-136">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="f9173-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9173-137">OUTPUTS</span></span>

### <span data-ttu-id="f9173-138">Microsoft. Azure. Management. COMPUTE. models. Image</span><span class="sxs-lookup"><span data-stu-id="f9173-138">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="f9173-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9173-139">NOTES</span></span>

## <span data-ttu-id="f9173-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9173-140">RELATED LINKS</span></span>

