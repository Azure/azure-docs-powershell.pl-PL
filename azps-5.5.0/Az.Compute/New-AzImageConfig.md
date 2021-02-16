---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199242"
---
# <span data-ttu-id="5559a-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="5559a-101">New-AzImageConfig</span></span>

## <span data-ttu-id="5559a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5559a-102">SYNOPSIS</span></span>
<span data-ttu-id="5559a-103">Tworzy konfigurowalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="5559a-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="5559a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5559a-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5559a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5559a-105">DESCRIPTION</span></span>
<span data-ttu-id="5559a-106">Polecenie **cmdlet New-AzImageConfig** tworzy konfigurowalny obiekt obrazu.</span><span class="sxs-lookup"><span data-stu-id="5559a-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="5559a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5559a-107">EXAMPLES</span></span>

### <span data-ttu-id="5559a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5559a-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="5559a-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w $imageConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="5559a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="5559a-110">Następne trzy polecenia przypiszą ścieżki dysku systemu operacyjnego i dwie dyskietki danych do zmiennych $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="5559a-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="5559a-111">Ta metoda ma na celu tylko czytelność następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="5559a-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="5559a-112">Następne trzy polecenia dodają dysk systemu operacyjnego i dwa dyski dla danych do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="5559a-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="5559a-113">Dane URI każdego dysku są przechowywane w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="5559a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="5559a-114">Końcowe polecenie tworzy obraz o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5559a-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5559a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5559a-115">PARAMETERS</span></span>

### <span data-ttu-id="5559a-116">-DataDrive</span><span class="sxs-lookup"><span data-stu-id="5559a-116">-DataDisk</span></span>
<span data-ttu-id="5559a-117">Określa obiekt dysku danych.</span><span class="sxs-lookup"><span data-stu-id="5559a-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5559a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5559a-118">-DefaultProfile</span></span>
<span data-ttu-id="5559a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5559a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5559a-120">—HyperV Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="5559a-120">-HyperVGeneration</span></span>
<span data-ttu-id="5559a-121">Określa typ hipervgeneracji dla maszyny wirtualnej utworzonej na podstawie obrazu.</span><span class="sxs-lookup"><span data-stu-id="5559a-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="5559a-122">Dozwolone wartości to V1 i V2.</span><span class="sxs-lookup"><span data-stu-id="5559a-122">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5559a-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5559a-123">-Location</span></span>
<span data-ttu-id="5559a-124">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="5559a-124">Specifies a location.</span></span>

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

### <span data-ttu-id="5559a-125">-Os Jednakowy</span><span class="sxs-lookup"><span data-stu-id="5559a-125">-OsDisk</span></span>
<span data-ttu-id="5559a-126">Określa dysk systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="5559a-126">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5559a-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5559a-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="5559a-128">Określa identyfikator źródłowej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5559a-128">Specifies the source virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5559a-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="5559a-129">-Tag</span></span>
<span data-ttu-id="5559a-130">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="5559a-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5559a-131">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5559a-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5559a-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="5559a-132">-ZoneResilient</span></span>
<span data-ttu-id="5559a-133">Włącz odporność na strefy</span><span class="sxs-lookup"><span data-stu-id="5559a-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="5559a-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5559a-134">-Confirm</span></span>
<span data-ttu-id="5559a-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5559a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5559a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5559a-136">-WhatIf</span></span>
<span data-ttu-id="5559a-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5559a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5559a-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5559a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5559a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5559a-139">CommonParameters</span></span>
<span data-ttu-id="5559a-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5559a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5559a-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5559a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5559a-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5559a-142">INPUTS</span></span>

### <span data-ttu-id="5559a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5559a-143">System.String</span></span>

### <span data-ttu-id="5559a-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5559a-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5559a-145">Microsoft.Azure.Management.Compute.Models.ImageOSGrafii</span><span class="sxs-lookup"><span data-stu-id="5559a-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="5559a-146">Microsoft.Azure.Management.Compute.Models.ImageDataData[]</span><span class="sxs-lookup"><span data-stu-id="5559a-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="5559a-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5559a-147">OUTPUTS</span></span>

### <span data-ttu-id="5559a-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="5559a-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="5559a-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5559a-149">NOTES</span></span>

## <span data-ttu-id="5559a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5559a-150">RELATED LINKS</span></span>
