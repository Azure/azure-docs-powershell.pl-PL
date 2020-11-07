---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
ms.openlocfilehash: ef9fc830b59568ad039b265fb182dbbdbd13a00d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897674"
---
# <span data-ttu-id="efa8d-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="efa8d-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="efa8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="efa8d-102">SYNOPSIS</span></span>
<span data-ttu-id="efa8d-103">Tworzy obiekt z obrazem konfigurowalnym.</span><span class="sxs-lookup"><span data-stu-id="efa8d-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efa8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="efa8d-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efa8d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="efa8d-105">DESCRIPTION</span></span>
<span data-ttu-id="efa8d-106">Polecenie cmdlet **New-AzureRmImageConfig** tworzy obiekt z obrazem konfigurowalnym.</span><span class="sxs-lookup"><span data-stu-id="efa8d-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="efa8d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="efa8d-107">EXAMPLES</span></span>

### <span data-ttu-id="efa8d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="efa8d-108">Example 1</span></span>
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

<span data-ttu-id="efa8d-109">Pierwsze polecenie tworzy obiekt obrazu, a następnie zapisuje go w zmiennej $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="efa8d-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="efa8d-110">Kolejne trzy polecenia umożliwiają przypisanie ścieżek do dysków systemu operacyjnego i dwóch dysków z danymi do $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="efa8d-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="efa8d-111">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="efa8d-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="efa8d-112">Kolejne trzy polecenia umożliwiają dodanie dysku systemu operacyjnego i dwóch dysków z danymi do obrazu przechowywanego w $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="efa8d-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="efa8d-113">Identyfikator URI każdego dysku jest przechowywany w $osDiskVhdUri, $dataDiskVhdUri 1 i $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="efa8d-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="efa8d-114">Polecenie ostatnie powoduje utworzenie obrazu o nazwie "ImageName01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="efa8d-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="efa8d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="efa8d-115">PARAMETERS</span></span>

### <span data-ttu-id="efa8d-116">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="efa8d-116">-DataDisk</span></span>
<span data-ttu-id="efa8d-117">Określa obiekt dysk danych.</span><span class="sxs-lookup"><span data-stu-id="efa8d-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="efa8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa8d-118">-DefaultProfile</span></span>
<span data-ttu-id="efa8d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="efa8d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efa8d-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="efa8d-120">-Location</span></span>
<span data-ttu-id="efa8d-121">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="efa8d-121">Specifies a location.</span></span>

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

### <span data-ttu-id="efa8d-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="efa8d-122">-OsDisk</span></span>
<span data-ttu-id="efa8d-123">Określa dysk systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="efa8d-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="efa8d-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="efa8d-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="efa8d-125">Określa identyfikator źródłowego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="efa8d-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="efa8d-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="efa8d-126">-Tag</span></span>
<span data-ttu-id="efa8d-127">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="efa8d-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="efa8d-128">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="efa8d-128">For example:</span></span>

<span data-ttu-id="efa8d-129">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="efa8d-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="efa8d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efa8d-130">-Confirm</span></span>
<span data-ttu-id="efa8d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efa8d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efa8d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa8d-132">-WhatIf</span></span>
<span data-ttu-id="efa8d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efa8d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efa8d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="efa8d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efa8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa8d-135">CommonParameters</span></span>
<span data-ttu-id="efa8d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa8d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efa8d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa8d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efa8d-138">INPUTS</span></span>

### <span data-ttu-id="efa8d-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="efa8d-139">None</span></span>
<span data-ttu-id="efa8d-140">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="efa8d-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="efa8d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="efa8d-141">OUTPUTS</span></span>

### <span data-ttu-id="efa8d-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSImage</span><span class="sxs-lookup"><span data-stu-id="efa8d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="efa8d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="efa8d-143">NOTES</span></span>

## <span data-ttu-id="efa8d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efa8d-144">RELATED LINKS</span></span>

