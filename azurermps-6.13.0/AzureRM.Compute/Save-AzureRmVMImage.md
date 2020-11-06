---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: b6d8d21eea863683912e204403ebe5a75ac40fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524537"
---
# <span data-ttu-id="377db-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="377db-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="377db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="377db-102">SYNOPSIS</span></span>
<span data-ttu-id="377db-103">Umożliwia zapisanie maszyny wirtualnej jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="377db-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="377db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="377db-104">SYNTAX</span></span>

### <span data-ttu-id="377db-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="377db-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="377db-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="377db-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="377db-107">Opis</span><span class="sxs-lookup"><span data-stu-id="377db-107">DESCRIPTION</span></span>
<span data-ttu-id="377db-108">Polecenie cmdlet **Save-AzureRmVMImage** umożliwia zapisanie maszyny wirtualnej jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="377db-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="377db-109">Przed utworzeniem obrazu maszyny wirtualnej Uruchom program Sysprep maszyny wirtualnej, a następnie Oznacz go jako uogólniony przy użyciu polecenia cmdlet Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="377db-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="377db-110">Wyjściem tego polecenia cmdlet jest szablon notacji kodu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="377db-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="377db-111">Możesz wdrożyć maszyny wirtualne z poziomu przechwyconego obrazu.</span><span class="sxs-lookup"><span data-stu-id="377db-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="377db-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="377db-112">EXAMPLES</span></span>

### <span data-ttu-id="377db-113">Przykład 1: Przechwytywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="377db-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="377db-114">Pierwsze polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnioną.</span><span class="sxs-lookup"><span data-stu-id="377db-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="377db-115">Drugie polecenie przechwytuje maszynę wirtualną o nazwie VirtualMachine07 jako VMImage.</span><span class="sxs-lookup"><span data-stu-id="377db-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="377db-116">Właściwość **Output** zwraca szablon JSON.</span><span class="sxs-lookup"><span data-stu-id="377db-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="377db-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="377db-117">PARAMETERS</span></span>

### <span data-ttu-id="377db-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="377db-118">-AsJob</span></span>
<span data-ttu-id="377db-119">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="377db-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="377db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377db-120">-DefaultProfile</span></span>
<span data-ttu-id="377db-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="377db-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="377db-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="377db-122">-DestinationContainerName</span></span>
<span data-ttu-id="377db-123">Określa nazwę kontenera w kontenerze "system", w którym mają być przechowywane obrazy.</span><span class="sxs-lookup"><span data-stu-id="377db-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="377db-124">Jeśli kontener nie istnieje, zostanie on utworzony.</span><span class="sxs-lookup"><span data-stu-id="377db-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="377db-125">Wirtualne dyski twarde (VHD), które tworzą VMImage, znajdują się w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="377db-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="377db-126">Jeśli dyski VHD są rozłożone na wiele kont magazynu, to polecenie cmdlet utworzy jeden kontener o tej nazwie w każdym z kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="377db-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="377db-127">Adres URL zapisanego obrazu jest podobny do: https:// \<storageAccountName\> . blob.Core.Windows.NET/system/Microsoft.COMPUTE/images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. VHD.</span><span class="sxs-lookup"><span data-stu-id="377db-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="377db-128">-ID</span><span class="sxs-lookup"><span data-stu-id="377db-128">-Id</span></span>
<span data-ttu-id="377db-129">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="377db-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="377db-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="377db-130">-Name</span></span>
<span data-ttu-id="377db-131">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="377db-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="377db-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="377db-132">-Overwrite</span></span>
<span data-ttu-id="377db-133">Wskazuje, że to polecenie cmdlet zastępuje wszystkie dyski VHD, które mają ten sam prefiks w kontenerze docelowym.</span><span class="sxs-lookup"><span data-stu-id="377db-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="377db-134">-Path</span><span class="sxs-lookup"><span data-stu-id="377db-134">-Path</span></span>
<span data-ttu-id="377db-135">Ścieżka pliku, w którym jest przechowywany szablon przechwyconego obrazu.</span><span class="sxs-lookup"><span data-stu-id="377db-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="377db-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="377db-136">-ResourceGroupName</span></span>
<span data-ttu-id="377db-137">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="377db-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="377db-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="377db-138">-VHDNamePrefix</span></span>
<span data-ttu-id="377db-139">Określa prefiks w nazwie obiektów blob, które tworzą profil przechowywania VMImage.</span><span class="sxs-lookup"><span data-stu-id="377db-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="377db-140">Na przykład prefiks vhdPrefix dla dysku systemu operacyjnego powoduje wystąpienie nazwy vhdPrefix-OSDisk. \<guid\> . dysków.</span><span class="sxs-lookup"><span data-stu-id="377db-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="377db-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377db-141">CommonParameters</span></span>
<span data-ttu-id="377db-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="377db-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377db-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="377db-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377db-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="377db-144">INPUTS</span></span>

### <span data-ttu-id="377db-145">System. String</span><span class="sxs-lookup"><span data-stu-id="377db-145">System.String</span></span>

### <span data-ttu-id="377db-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="377db-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="377db-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="377db-147">OUTPUTS</span></span>

### <span data-ttu-id="377db-148">Microsoft. Azure. Commands. COMPUTE. models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="377db-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="377db-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="377db-149">NOTES</span></span>

## <span data-ttu-id="377db-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="377db-150">RELATED LINKS</span></span>

[<span data-ttu-id="377db-151">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="377db-151">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="377db-152">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="377db-152">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="377db-153">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="377db-153">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="377db-154">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="377db-154">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="377db-155">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="377db-155">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


