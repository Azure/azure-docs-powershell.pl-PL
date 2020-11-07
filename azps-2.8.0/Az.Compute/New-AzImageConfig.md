---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: c76ccab31b3c5c11216a1a929e2a78df55713325
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706335"
---
# <span data-ttu-id="92d5b-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="92d5b-101">New-AzImageConfig</span></span>

## <span data-ttu-id="92d5b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="92d5b-103">Tworzy obiekt z obrazem konfigurowalnym.</span><span class="sxs-lookup"><span data-stu-id="92d5b-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="92d5b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92d5b-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92d5b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92d5b-105">DESCRIPTION</span></span>
<span data-ttu-id="92d5b-106">Polecenie cmdlet **New-AzImageConfig** tworzy obiekt z obrazem konfigurowalnym.</span><span class="sxs-lookup"><span data-stu-id="92d5b-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="92d5b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92d5b-107">EXAMPLES</span></span>

### <span data-ttu-id="92d5b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="92d5b-108">Example 1</span></span>
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

<span data-ttu-id="92d5b-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="92d5b-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="92d5b-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek do dysków systemu operacyjnego i dwóch dysków z danymi do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="92d5b-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="92d5b-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="92d5b-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="92d5b-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="92d5b-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="92d5b-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="92d5b-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="92d5b-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="92d5b-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="92d5b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92d5b-115">PARAMETERS</span></span>

### <span data-ttu-id="92d5b-116">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="92d5b-116">-DataDisk</span></span>
<span data-ttu-id="92d5b-117">Określa obiekt dysk danych.</span><span class="sxs-lookup"><span data-stu-id="92d5b-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="92d5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d5b-118">-DefaultProfile</span></span>
<span data-ttu-id="92d5b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92d5b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92d5b-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="92d5b-120">-HyperVGeneration</span></span>
<span data-ttu-id="92d5b-121">Określa typ HyperVGeneration maszyny wirtualnej utworzonej na podstawie obrazu.</span><span class="sxs-lookup"><span data-stu-id="92d5b-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="92d5b-122">Dozwolone wartości to V1 i v2.</span><span class="sxs-lookup"><span data-stu-id="92d5b-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="92d5b-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="92d5b-123">-Location</span></span>
<span data-ttu-id="92d5b-124">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="92d5b-124">Specifies a location.</span></span>

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

### <span data-ttu-id="92d5b-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="92d5b-125">-OsDisk</span></span>
<span data-ttu-id="92d5b-126">Określa dysk systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="92d5b-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="92d5b-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="92d5b-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="92d5b-128">Określa identyfikator źródłowego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="92d5b-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="92d5b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="92d5b-129">-Tag</span></span>
<span data-ttu-id="92d5b-130">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="92d5b-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="92d5b-131">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="92d5b-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="92d5b-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="92d5b-132">-ZoneResilient</span></span>
<span data-ttu-id="92d5b-133">Włączanie odporności na strefy</span><span class="sxs-lookup"><span data-stu-id="92d5b-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="92d5b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92d5b-134">-Confirm</span></span>
<span data-ttu-id="92d5b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92d5b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92d5b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92d5b-136">-WhatIf</span></span>
<span data-ttu-id="92d5b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92d5b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92d5b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92d5b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92d5b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d5b-139">CommonParameters</span></span>
<span data-ttu-id="92d5b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d5b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d5b-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92d5b-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d5b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92d5b-142">INPUTS</span></span>

### <span data-ttu-id="92d5b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="92d5b-143">System.String</span></span>

### <span data-ttu-id="92d5b-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="92d5b-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="92d5b-145">Microsoft. Azure. Management. COMPUTE. MODELES. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="92d5b-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="92d5b-146">Microsoft. Azure. Management. COMPUTE. MODELES. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="92d5b-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="92d5b-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92d5b-147">OUTPUTS</span></span>

### <span data-ttu-id="92d5b-148">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="92d5b-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="92d5b-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92d5b-149">NOTES</span></span>

## <span data-ttu-id="92d5b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92d5b-150">RELATED LINKS</span></span>