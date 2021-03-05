---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: d979e89583b19270dfd13bae85a3afe1505ed55e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998208"
---
# <span data-ttu-id="0157a-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0157a-101">Save-AzVMImage</span></span>

## <span data-ttu-id="0157a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0157a-102">SYNOPSIS</span></span>
<span data-ttu-id="0157a-103">Umożliwia zapisanie maszyny wirtualnej jako maszyny WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="0157a-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="0157a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0157a-104">SYNTAX</span></span>

### <span data-ttu-id="0157a-105">ResourceGroupNameParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0157a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0157a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0157a-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0157a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0157a-107">DESCRIPTION</span></span>
<span data-ttu-id="0157a-108">Polecenie **cmdlet Save-AzVMImage** umożliwia zapisanie maszyny wirtualnej jako maszyny WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="0157a-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="0157a-109">Przed utworzeniem obrazu maszyny wirtualnej należy ją sysprepować, a następnie oznaczyć jako uogólniony za pomocą Set-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0157a-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="0157a-110">Dane wyjściowe tego polecenia cmdlet to szablon JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="0157a-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="0157a-111">Możesz wdrożyć maszyny wirtualne z przechwyconego obrazu.</span><span class="sxs-lookup"><span data-stu-id="0157a-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="0157a-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0157a-112">EXAMPLES</span></span>

### <span data-ttu-id="0157a-113">Przykład 1. Przechwytywanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="0157a-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="0157a-114">Pierwsze polecenie oznacza maszynę wirtualną o nazwie VirtualMachine07 jako uogólnione.</span><span class="sxs-lookup"><span data-stu-id="0157a-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="0157a-115">Drugie polecenie przechwyci maszynę wirtualną o nazwie VirtualMachine07 jako obraz MASZYNY WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="0157a-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="0157a-116">Właściwość **Output** zwraca szablon JSON.</span><span class="sxs-lookup"><span data-stu-id="0157a-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="0157a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0157a-117">PARAMETERS</span></span>

### <span data-ttu-id="0157a-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0157a-118">-AsJob</span></span>
<span data-ttu-id="0157a-119">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="0157a-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0157a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0157a-120">-DefaultProfile</span></span>
<span data-ttu-id="0157a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0157a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0157a-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="0157a-122">-DestinationContainerName</span></span>
<span data-ttu-id="0157a-123">Określa nazwę kontenera w kontenerze "systemowym", który ma zawierać obrazy.</span><span class="sxs-lookup"><span data-stu-id="0157a-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="0157a-124">Jeśli kontener nie istnieje, zostanie utworzony za Ciebie.</span><span class="sxs-lookup"><span data-stu-id="0157a-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="0157a-125">Wirtualne dyskietki twarde (VHDS), które stanowią dysk WIRTUALNEJ pamięci, znajdują się w kontenerze, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0157a-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="0157a-126">Jeśli identyfikatory VHD są rozłożone między wiele kont magazynu, to polecenie cmdlet tworzy jeden kontener o tej nazwie na każdym koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="0157a-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="0157a-127">Adres URL zapisanego obrazu jest podobny do: https:// \<storageAccountName\> .blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> .xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span><span class="sxs-lookup"><span data-stu-id="0157a-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="0157a-128">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="0157a-128">-Id</span></span>
<span data-ttu-id="0157a-129">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0157a-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="0157a-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0157a-130">-Name</span></span>
<span data-ttu-id="0157a-131">Określa nazwę.</span><span class="sxs-lookup"><span data-stu-id="0157a-131">Specifies a name.</span></span>

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

### <span data-ttu-id="0157a-132">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="0157a-132">-Overwrite</span></span>
<span data-ttu-id="0157a-133">Wskazuje, że to polecenie cmdlet zastępuje wszystkie identyfikatory VHD, które mają ten sam prefiks w kontenerze docelowym.</span><span class="sxs-lookup"><span data-stu-id="0157a-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="0157a-134">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="0157a-134">-Path</span></span>
<span data-ttu-id="0157a-135">Ścieżka pliku, w której jest przechowywany szablon przechwyconego obrazu.</span><span class="sxs-lookup"><span data-stu-id="0157a-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="0157a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0157a-136">-ResourceGroupName</span></span>
<span data-ttu-id="0157a-137">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0157a-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0157a-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="0157a-138">-VHDNamePrefix</span></span>
<span data-ttu-id="0157a-139">Określa prefiks w nazwie obiektów blob, które stanowią profil magazynu maszyny WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="0157a-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="0157a-140">Na przykład prefiks vhdPrefix dla dysku systemu operacyjnego powoduje nadaną nazwę vhdPrefix-osfix. \<guid\> vhd.</span><span class="sxs-lookup"><span data-stu-id="0157a-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="0157a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0157a-141">CommonParameters</span></span>
<span data-ttu-id="0157a-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0157a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0157a-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0157a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0157a-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0157a-144">INPUTS</span></span>

### <span data-ttu-id="0157a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0157a-145">System.String</span></span>

### <span data-ttu-id="0157a-146">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="0157a-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0157a-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0157a-147">OUTPUTS</span></span>

### <span data-ttu-id="0157a-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="0157a-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="0157a-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0157a-149">NOTES</span></span>

## <span data-ttu-id="0157a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0157a-150">RELATED LINKS</span></span>

[<span data-ttu-id="0157a-151">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0157a-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="0157a-152">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="0157a-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="0157a-153">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0157a-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="0157a-154">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0157a-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="0157a-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="0157a-155">Set-AzVM</span></span>](./Set-AzVM.md)


