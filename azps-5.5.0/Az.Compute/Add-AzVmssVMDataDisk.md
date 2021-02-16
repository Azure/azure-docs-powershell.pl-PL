---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195091"
---
# <span data-ttu-id="75a99-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="75a99-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="75a99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a99-102">SYNOPSIS</span></span>
<span data-ttu-id="75a99-103">Dodaje dysk danych do maszyny wirtualnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75a99-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="75a99-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75a99-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a99-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="75a99-105">DESCRIPTION</span></span>
<span data-ttu-id="75a99-106">Polecenie **cmdlet AzVmssVMDataData Add-AzVmssVMDataData Umożliwia** dodanie dysku danych do maszyny wirtualnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75a99-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="75a99-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75a99-107">EXAMPLES</span></span>

### <span data-ttu-id="75a99-108">Przykład 1. Dodawanie zarządzanego dysku danych do maszyny wirtualnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75a99-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="75a99-109">Pierwsze polecenie otrzymuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="75a99-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="75a99-110">Następne polecenie pobiera istniejącą maszynę wirtualnej maszyny wirtualnej, która jest podana przez nazwę grupy zasobów, nazwę maszyny wirtualnej i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="75a99-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="75a99-111">Następne polecenie dodaje dysk zarządzany do maszyny wirtualnej maszyny wirtualnej przechowywanej lokalnie w $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="75a99-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="75a99-112">Końcowe polecenie aktualizuje maszynę wirtualnej maszyny wirtualnej o dodany dysk danych.</span><span class="sxs-lookup"><span data-stu-id="75a99-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="75a99-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75a99-113">PARAMETERS</span></span>

### <span data-ttu-id="75a99-114">— buforowanie</span><span class="sxs-lookup"><span data-stu-id="75a99-114">-Caching</span></span>
<span data-ttu-id="75a99-115">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="75a99-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="75a99-116">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="75a99-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75a99-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="75a99-117">ReadOnly</span></span>
- <span data-ttu-id="75a99-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="75a99-118">ReadWrite</span></span>
- <span data-ttu-id="75a99-119">Brak Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="75a99-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="75a99-120">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75a99-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="75a99-121">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="75a99-121">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a99-122">— CreateOption</span><span class="sxs-lookup"><span data-stu-id="75a99-122">-CreateOption</span></span>
<span data-ttu-id="75a99-123">Określa, czy to polecenie cmdlet tworzy dysk na komputerze wirtualnym z platformy lub obrazu użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="75a99-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="75a99-124">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="75a99-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75a99-125">Dołącz.</span><span class="sxs-lookup"><span data-stu-id="75a99-125">Attach.</span></span>
<span data-ttu-id="75a99-126">Określ tę opcję, aby utworzyć maszynę wirtualną na dysku specjalistycznym.</span><span class="sxs-lookup"><span data-stu-id="75a99-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="75a99-127">Po określeniu tej opcji nie należy określać *parametru SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="75a99-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="75a99-128">*VhdUri* to wszystko, co jest potrzebne, aby poinformować platformę Azure o lokalizacji wirtualnego dysku twardego (VHD) w celu dołączenia go jako dysku danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75a99-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="75a99-129">Puste.</span><span class="sxs-lookup"><span data-stu-id="75a99-129">Empty.</span></span>
<span data-ttu-id="75a99-130">Określ tę wartość, aby utworzyć pusty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="75a99-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="75a99-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="75a99-131">FromImage.</span></span>
<span data-ttu-id="75a99-132">Określ tę opcję, aby utworzyć maszynę wirtualną na dysku lub obrazie ogólnym.</span><span class="sxs-lookup"><span data-stu-id="75a99-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="75a99-133">Podczas określania tej opcji musisz określić parametr *SourceImageUri,* aby wskazać platformie Azure lokalizację pliku VHD do dołączenia jako dysku danych.</span><span class="sxs-lookup"><span data-stu-id="75a99-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="75a99-134">Parametr *VhdUri* jest używany jako lokalizacja identyfikująca miejsce przechowywania dysku danych VHD, gdy będzie używany przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="75a99-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="75a99-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a99-135">-DefaultProfile</span></span>
<span data-ttu-id="75a99-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="75a99-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a99-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="75a99-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="75a99-138">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanych przez klienta.</span><span class="sxs-lookup"><span data-stu-id="75a99-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="75a99-139">Tę wartość można określić tylko dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="75a99-139">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a99-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="75a99-140">-DiskSizeInGB</span></span>
<span data-ttu-id="75a99-141">Określa w gigabajtach rozmiar pustego dysku do dołączenia do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75a99-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a99-142">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="75a99-142">-Lun</span></span>
<span data-ttu-id="75a99-143">Określa numer jednostki logicznej (OWĄ) dla dysku danych.</span><span class="sxs-lookup"><span data-stu-id="75a99-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a99-144">-Managed Jednakid</span><span class="sxs-lookup"><span data-stu-id="75a99-144">-ManagedDiskId</span></span>
<span data-ttu-id="75a99-145">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="75a99-145">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75a99-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="75a99-146">-StorageAccountType</span></span>
<span data-ttu-id="75a99-147">Określa typ konta magazynu zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="75a99-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="75a99-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="75a99-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="75a99-149">Określa lokalny obiekt skalowania maszyny wirtualnej, do którego ma być dodać dysk danych.</span><span class="sxs-lookup"><span data-stu-id="75a99-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="75a99-150">Możesz użyć polecenia cmdlet **Get-AzVmssVM,** aby uzyskać obiekt ZESTAWU SKALA MASZYNY WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="75a99-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75a99-151">- WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="75a99-151">-WriteAccelerator</span></span>
<span data-ttu-id="75a99-152">Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na zarządzanym dysku danych.</span><span class="sxs-lookup"><span data-stu-id="75a99-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="75a99-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a99-153">CommonParameters</span></span>
<span data-ttu-id="75a99-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a99-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a99-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75a99-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a99-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75a99-156">INPUTS</span></span>

### <span data-ttu-id="75a99-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="75a99-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="75a99-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="75a99-158">System.Int32</span></span>

### <span data-ttu-id="75a99-159">System.String</span><span class="sxs-lookup"><span data-stu-id="75a99-159">System.String</span></span>

### <span data-ttu-id="75a99-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="75a99-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="75a99-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75a99-161">OUTPUTS</span></span>

### <span data-ttu-id="75a99-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="75a99-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="75a99-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75a99-163">NOTES</span></span>

## <span data-ttu-id="75a99-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75a99-164">RELATED LINKS</span></span>
