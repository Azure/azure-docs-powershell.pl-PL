---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370050"
---
# <span data-ttu-id="e8bde-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e8bde-101">Save-AzVMImage</span></span>

## <span data-ttu-id="e8bde-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8bde-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bde-103">Umożliwia zapisanie maszyny wirtualnej jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="e8bde-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="e8bde-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8bde-104">SYNTAX</span></span>

### <span data-ttu-id="e8bde-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8bde-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8bde-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e8bde-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8bde-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e8bde-107">DESCRIPTION</span></span>
<span data-ttu-id="e8bde-108">Polecenie cmdlet **Save-AzVMImage** umożliwia zapisanie maszyny wirtualnej jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="e8bde-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="e8bde-109">Przed utworzeniem obrazu maszyny wirtualnej Uruchom program Sysprep maszyny wirtualnej, a następnie Oznacz go jako uogólniony przy użyciu polecenia cmdlet Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="e8bde-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="e8bde-110">Wyjściem tego polecenia cmdlet jest szablon notacji kodu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e8bde-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="e8bde-111">Możesz wdrożyć maszyny wirtualne z poziomu przechwyconego obrazu.</span><span class="sxs-lookup"><span data-stu-id="e8bde-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="e8bde-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8bde-112">EXAMPLES</span></span>

### <span data-ttu-id="e8bde-113">Przykład 1: Przechwytywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e8bde-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="e8bde-114">Pierwsze polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="e8bde-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="e8bde-115">Drugie polecenie przechwytuje maszynę wirtualną o nazwie VirtualMachine07 jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="e8bde-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="e8bde-116">Właściwość **Output** zwraca szablon JSON.</span><span class="sxs-lookup"><span data-stu-id="e8bde-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="e8bde-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8bde-117">PARAMETERS</span></span>

### <span data-ttu-id="e8bde-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8bde-118">-AsJob</span></span>
<span data-ttu-id="e8bde-119">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="e8bde-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e8bde-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8bde-120">-DefaultProfile</span></span>
<span data-ttu-id="e8bde-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8bde-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8bde-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="e8bde-122">-DestinationContainerName</span></span>
<span data-ttu-id="e8bde-123">Określa nazwę kontenera w kontenerze "system", w którym mają być przechowywane obrazy.</span><span class="sxs-lookup"><span data-stu-id="e8bde-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="e8bde-124">Jeśli kontener nie istnieje, zostanie on utworzony.</span><span class="sxs-lookup"><span data-stu-id="e8bde-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="e8bde-125">Wirtualne dyski twarde (VHD), które tworzą VMImage, znajdują się w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e8bde-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="e8bde-126">Jeśli dyski VHD są rozłożone na wiele kont magazynu, to polecenie cmdlet utworzy jeden kontener o tej nazwie w każdym z kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="e8bde-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="e8bde-127">Adres URL zapisanego obrazu jest podobny do: https:// \<storageAccountName\> . blob.Core.Windows.NET/system/Microsoft.COMPUTE/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. VHD.</span><span class="sxs-lookup"><span data-stu-id="e8bde-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bde-128">-ID</span><span class="sxs-lookup"><span data-stu-id="e8bde-128">-Id</span></span>
<span data-ttu-id="e8bde-129">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8bde-129">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bde-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8bde-130">-Name</span></span>
<span data-ttu-id="e8bde-131">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="e8bde-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bde-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e8bde-132">-Overwrite</span></span>
<span data-ttu-id="e8bde-133">Wskazuje, że to polecenie cmdlet zastępuje wszystkie dyski VHD, które mają ten sam prefiks w kontenerze docelowym.</span><span class="sxs-lookup"><span data-stu-id="e8bde-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bde-134">-Path</span><span class="sxs-lookup"><span data-stu-id="e8bde-134">-Path</span></span>
<span data-ttu-id="e8bde-135">Ścieżka pliku, w którym jest przechowywany szablon przechwyconego obrazu.</span><span class="sxs-lookup"><span data-stu-id="e8bde-135">The file path in which the template of the captured image is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bde-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8bde-136">-ResourceGroupName</span></span>
<span data-ttu-id="e8bde-137">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8bde-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bde-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e8bde-138">-VHDNamePrefix</span></span>
<span data-ttu-id="e8bde-139">Określa prefiks w nazwie obiektów blob, które tworzą profil przechowywania VMImage.</span><span class="sxs-lookup"><span data-stu-id="e8bde-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="e8bde-140">Na przykład prefiks vhdPrefix dla dysku systemu operacyjnego powoduje wystąpienie nazwy vhdPrefix-OSDisk. \<guid\> . dysków.</span><span class="sxs-lookup"><span data-stu-id="e8bde-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bde-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bde-141">CommonParameters</span></span>
<span data-ttu-id="e8bde-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8bde-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bde-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8bde-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bde-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8bde-144">INPUTS</span></span>

### <span data-ttu-id="e8bde-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e8bde-145">System.String</span></span>

### <span data-ttu-id="e8bde-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e8bde-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e8bde-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8bde-147">OUTPUTS</span></span>

### <span data-ttu-id="e8bde-148">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e8bde-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="e8bde-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8bde-149">NOTES</span></span>

## <span data-ttu-id="e8bde-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8bde-150">RELATED LINKS</span></span>

[<span data-ttu-id="e8bde-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e8bde-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="e8bde-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e8bde-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="e8bde-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e8bde-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="e8bde-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e8bde-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="e8bde-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="e8bde-155">Set-AzVM</span></span>](./Set-AzVM.md)


