---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: f7f2a9ee7119b54722862b3796e9a5372b9b1d09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710278"
---
# <span data-ttu-id="fbe01-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="fbe01-101">New-AzImageConfig</span></span>

## <span data-ttu-id="fbe01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbe01-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe01-103">Tworzy obiekt z obrazem konfigurowalnym.</span><span class="sxs-lookup"><span data-stu-id="fbe01-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="fbe01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbe01-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe01-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbe01-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe01-106">Polecenie cmdlet **New-AzImageConfig** tworzy obiekt z obrazem konfigurowalnym.</span><span class="sxs-lookup"><span data-stu-id="fbe01-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="fbe01-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbe01-107">EXAMPLES</span></span>

### <span data-ttu-id="fbe01-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fbe01-108">Example 1</span></span>
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

<span data-ttu-id="fbe01-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="fbe01-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="fbe01-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek do dysków systemu operacyjnego i dwóch dysków z danymi do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="fbe01-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="fbe01-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="fbe01-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="fbe01-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="fbe01-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="fbe01-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="fbe01-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="fbe01-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fbe01-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fbe01-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbe01-115">PARAMETERS</span></span>

### <span data-ttu-id="fbe01-116">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="fbe01-116">-DataDisk</span></span>
<span data-ttu-id="fbe01-117">Określa obiekt dysk danych.</span><span class="sxs-lookup"><span data-stu-id="fbe01-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="fbe01-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe01-118">-DefaultProfile</span></span>
<span data-ttu-id="fbe01-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe01-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbe01-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fbe01-120">-Location</span></span>
<span data-ttu-id="fbe01-121">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="fbe01-121">Specifies a location.</span></span>

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

### <span data-ttu-id="fbe01-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="fbe01-122">-OsDisk</span></span>
<span data-ttu-id="fbe01-123">Określa dysk systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="fbe01-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="fbe01-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="fbe01-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="fbe01-125">Określa identyfikator źródłowego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fbe01-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="fbe01-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="fbe01-126">-Tag</span></span>
<span data-ttu-id="fbe01-127">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="fbe01-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fbe01-128">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="fbe01-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fbe01-129">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="fbe01-129">-ZoneResilient</span></span>
<span data-ttu-id="fbe01-130">Włączanie odporności na strefy</span><span class="sxs-lookup"><span data-stu-id="fbe01-130">Enable zone resilient</span></span>

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

### <span data-ttu-id="fbe01-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbe01-131">-Confirm</span></span>
<span data-ttu-id="fbe01-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbe01-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe01-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe01-133">-WhatIf</span></span>
<span data-ttu-id="fbe01-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbe01-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbe01-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fbe01-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe01-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe01-136">CommonParameters</span></span>
<span data-ttu-id="fbe01-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe01-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe01-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe01-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe01-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbe01-139">INPUTS</span></span>

### <span data-ttu-id="fbe01-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fbe01-140">System.String</span></span>

### <span data-ttu-id="fbe01-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbe01-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fbe01-142">Microsoft. Azure. Management. COMPUTE. MODELES. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="fbe01-142">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="fbe01-143">Microsoft. Azure. Management. COMPUTE. MODELES. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="fbe01-143">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="fbe01-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbe01-144">OUTPUTS</span></span>

### <span data-ttu-id="fbe01-145">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="fbe01-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="fbe01-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbe01-146">NOTES</span></span>

## <span data-ttu-id="fbe01-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbe01-147">RELATED LINKS</span></span>
