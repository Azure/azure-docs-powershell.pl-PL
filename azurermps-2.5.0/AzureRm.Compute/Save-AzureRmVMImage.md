---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
ms.openlocfilehash: b781023b424dd23d3d0874893b724744ecb33bda
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899371"
---
# <span data-ttu-id="1d6c6-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1d6c6-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="1d6c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d6c6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d6c6-103">Umożliwia zapisanie maszyny wirtualnej jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d6c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d6c6-104">SYNTAX</span></span>

### <span data-ttu-id="1d6c6-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1d6c6-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d6c6-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1d6c6-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d6c6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1d6c6-107">DESCRIPTION</span></span>
<span data-ttu-id="1d6c6-108">Polecenie cmdlet **Save-AzureRmVMImage** umożliwia zapisanie maszyny wirtualnej jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="1d6c6-109">Przed utworzeniem obrazu maszyny wirtualnej Uruchom program Sysprep maszyny wirtualnej, a następnie Oznacz go jako uogólniony przy użyciu polecenia cmdlet Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="1d6c6-110">Wyjściem tego polecenia cmdlet jest szablon notacji kodu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="1d6c6-111">Możesz wdrożyć maszyny wirtualne z poziomu przechwyconego obrazu.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="1d6c6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d6c6-112">EXAMPLES</span></span>

### <span data-ttu-id="1d6c6-113">Przykład 1: Przechwytywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1d6c6-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="1d6c6-114">Pierwsze polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="1d6c6-115">Drugie polecenie przechwytuje maszynę wirtualną o nazwie VirtualMachine07 jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="1d6c6-116">Właściwość **Output** zwraca szablon JSON.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="1d6c6-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d6c6-117">PARAMETERS</span></span>

### <span data-ttu-id="1d6c6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d6c6-118">-AsJob</span></span>
<span data-ttu-id="1d6c6-119">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1d6c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d6c6-120">-DefaultProfile</span></span>
<span data-ttu-id="1d6c6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d6c6-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="1d6c6-122">-DestinationContainerName</span></span>
<span data-ttu-id="1d6c6-123">Określa nazwę kontenera w kontenerze "system", w którym mają być przechowywane obrazy.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="1d6c6-124">Jeśli kontener nie istnieje, zostanie on utworzony.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="1d6c6-125">Wirtualne dyski twarde (VHD), które tworzą VMImage, znajdują się w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="1d6c6-126">Jeśli dyski VHD są rozłożone na wiele kont magazynu, to polecenie cmdlet utworzy jeden kontener o tej nazwie w każdym z kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="1d6c6-127">Adres URL zapisanego obrazu jest podobny do:</span><span class="sxs-lookup"><span data-stu-id="1d6c6-127">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="1d6c6-128"> https:// \<storageAccountName\> . blob.Core.Windows.NET/system/Microsoft.COMPUTE/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. VHD.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-128">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="1d6c6-129">-ID</span><span class="sxs-lookup"><span data-stu-id="1d6c6-129">-Id</span></span>
<span data-ttu-id="1d6c6-130">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-130">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="1d6c6-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d6c6-131">-Name</span></span>
<span data-ttu-id="1d6c6-132">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-132">Specifies a name.</span></span>

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

### <span data-ttu-id="1d6c6-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="1d6c6-133">-Overwrite</span></span>
<span data-ttu-id="1d6c6-134">Wskazuje, że to polecenie cmdlet zastępuje wszystkie dyski VHD, które mają ten sam prefiks w kontenerze docelowym.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-134">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="1d6c6-135">-Path</span><span class="sxs-lookup"><span data-stu-id="1d6c6-135">-Path</span></span>
<span data-ttu-id="1d6c6-136">Określa ścieżkę dysku VHD.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-136">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="1d6c6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d6c6-137">-ResourceGroupName</span></span>
<span data-ttu-id="1d6c6-138">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-138">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1d6c6-139">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="1d6c6-139">-VHDNamePrefix</span></span>
<span data-ttu-id="1d6c6-140">Określa prefiks w nazwie obiektów blob, które tworzą profil przechowywania VMImage.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-140">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="1d6c6-141">Na przykład prefiks vhdPrefix dla dysku systemu operacyjnego powoduje wystąpienie nazwy vhdPrefix-OSDisk. \<guid\> . dysków.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-141">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="1d6c6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d6c6-142">CommonParameters</span></span>
<span data-ttu-id="1d6c6-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d6c6-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d6c6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d6c6-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d6c6-145">INPUTS</span></span>

### <span data-ttu-id="1d6c6-146">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1d6c6-146">None</span></span>
<span data-ttu-id="1d6c6-147">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1d6c6-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d6c6-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d6c6-148">OUTPUTS</span></span>

### <span data-ttu-id="1d6c6-149">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="1d6c6-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="1d6c6-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d6c6-150">NOTES</span></span>

## <span data-ttu-id="1d6c6-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d6c6-151">RELATED LINKS</span></span>

[<span data-ttu-id="1d6c6-152">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="1d6c6-152">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="1d6c6-153">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="1d6c6-153">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="1d6c6-154">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1d6c6-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="1d6c6-155">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1d6c6-155">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="1d6c6-156">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1d6c6-156">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


