---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: 8f3aebe1e9e79423d7251fa79084d6fa85407b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552987"
---
# <span data-ttu-id="0a602-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0a602-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="0a602-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a602-102">SYNOPSIS</span></span>
<span data-ttu-id="0a602-103">Umożliwia zapisanie maszyny wirtualnej jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="0a602-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a602-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a602-104">SYNTAX</span></span>

### <span data-ttu-id="0a602-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0a602-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [<CommonParameters>]
```

### <span data-ttu-id="0a602-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0a602-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="0a602-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0a602-107">DESCRIPTION</span></span>
<span data-ttu-id="0a602-108">Polecenie cmdlet **Save-AzureRmVMImage** umożliwia zapisanie maszyny wirtualnej jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="0a602-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="0a602-109">Przed utworzeniem obrazu maszyny wirtualnej Uruchom program Sysprep maszyny wirtualnej, a następnie Oznacz go jako uogólniony przy użyciu polecenia cmdlet Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="0a602-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="0a602-110">Wyjściem tego polecenia cmdlet jest szablon notacji kodu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a602-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="0a602-111">Możesz wdrożyć maszyny wirtualne z poziomu przechwyconego obrazu.</span><span class="sxs-lookup"><span data-stu-id="0a602-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="0a602-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a602-112">EXAMPLES</span></span>

### <span data-ttu-id="0a602-113">Przykład 1: Przechwytywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0a602-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="0a602-114">Pierwsze polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="0a602-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="0a602-115">Drugie polecenie przechwytuje maszynę wirtualną o nazwie VirtualMachine07 jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="0a602-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="0a602-116">Właściwość **Output** zwraca szablon JSON.</span><span class="sxs-lookup"><span data-stu-id="0a602-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="0a602-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a602-117">PARAMETERS</span></span>

### <span data-ttu-id="0a602-118">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="0a602-118">-DestinationContainerName</span></span>
<span data-ttu-id="0a602-119">Określa nazwę kontenera w kontenerze "system", w którym mają być przechowywane obrazy.</span><span class="sxs-lookup"><span data-stu-id="0a602-119">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="0a602-120">Jeśli kontener nie istnieje, zostanie on utworzony.</span><span class="sxs-lookup"><span data-stu-id="0a602-120">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="0a602-121">Wirtualne dyski twarde (VHD), które tworzą VMImage, znajdują się w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0a602-121">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="0a602-122">Jeśli dyski VHD są rozłożone na wiele kont magazynu, to polecenie cmdlet utworzy jeden kontener o tej nazwie w każdym z kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="0a602-122">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="0a602-123">Adres URL zapisanego obrazu jest podobny do:</span><span class="sxs-lookup"><span data-stu-id="0a602-123">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="0a602-124"> https:// \<storageAccountName\> . blob.Core.Windows.NET/system/Microsoft.COMPUTE/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. VHD.</span><span class="sxs-lookup"><span data-stu-id="0a602-124">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a602-125">-ID</span><span class="sxs-lookup"><span data-stu-id="0a602-125">-Id</span></span>
<span data-ttu-id="0a602-126">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0a602-126">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a602-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a602-127">-Name</span></span>
<span data-ttu-id="0a602-128">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="0a602-128">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a602-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="0a602-129">-Overwrite</span></span>
<span data-ttu-id="0a602-130">Wskazuje, że to polecenie cmdlet zastępuje wszystkie dyski VHD, które mają ten sam prefiks w kontenerze docelowym.</span><span class="sxs-lookup"><span data-stu-id="0a602-130">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a602-131">-Path</span><span class="sxs-lookup"><span data-stu-id="0a602-131">-Path</span></span>
<span data-ttu-id="0a602-132">Określa ścieżkę dysku VHD.</span><span class="sxs-lookup"><span data-stu-id="0a602-132">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a602-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a602-133">-ResourceGroupName</span></span>
<span data-ttu-id="0a602-134">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0a602-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a602-135">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="0a602-135">-VHDNamePrefix</span></span>
<span data-ttu-id="0a602-136">Określa prefiks w nazwie obiektów blob, które tworzą profil przechowywania VMImage.</span><span class="sxs-lookup"><span data-stu-id="0a602-136">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="0a602-137">Na przykład prefiks vhdPrefix dla dysku systemu operacyjnego powoduje wystąpienie nazwy vhdPrefix-OSDisk. \<guid\> . dysków.</span><span class="sxs-lookup"><span data-stu-id="0a602-137">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a602-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a602-138">CommonParameters</span></span>
<span data-ttu-id="0a602-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a602-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a602-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a602-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a602-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a602-141">INPUTS</span></span>

### <span data-ttu-id="0a602-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0a602-142">None</span></span>
<span data-ttu-id="0a602-143">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0a602-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a602-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a602-144">OUTPUTS</span></span>

## <span data-ttu-id="0a602-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a602-145">NOTES</span></span>

## <span data-ttu-id="0a602-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a602-146">RELATED LINKS</span></span>

[<span data-ttu-id="0a602-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0a602-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="0a602-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0a602-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="0a602-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0a602-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="0a602-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0a602-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="0a602-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0a602-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


