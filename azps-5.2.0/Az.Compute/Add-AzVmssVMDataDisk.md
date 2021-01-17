---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370041"
---
# <span data-ttu-id="06b9c-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="06b9c-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="06b9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="06b9c-103">Dodaje dysk danych do maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="06b9c-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="06b9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06b9c-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06b9c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="06b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="06b9c-106">Polecenie cmdlet **Add-AzVmssVMDataDisk** umożliwia dodanie dysku z danymi do VMSS maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="06b9c-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="06b9c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06b9c-107">EXAMPLES</span></span>

### <span data-ttu-id="06b9c-108">Przykład 1: dodanie zarządzanego dysku danych do maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="06b9c-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="06b9c-109">Pierwsze polecenie uzyskuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="06b9c-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="06b9c-110">Następne polecenie pobiera istniejącą maszynę wirtualną VMSS określoną przez nazwę grupy zasobów, nazwę VMSS i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="06b9c-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="06b9c-111">Polecenie Next (następne) dodaje dysk zarządzany do maszyny wirtualnej VMSS zapisanej lokalnie w $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="06b9c-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="06b9c-112">W ostatnim poleceniu zostanie zaktualizowana maszyna wirtualna VMSS z dodanym dyskiem danych.</span><span class="sxs-lookup"><span data-stu-id="06b9c-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="06b9c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06b9c-113">PARAMETERS</span></span>

### <span data-ttu-id="06b9c-114">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="06b9c-114">-Caching</span></span>
<span data-ttu-id="06b9c-115">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="06b9c-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="06b9c-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="06b9c-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06b9c-117">Odczytu</span><span class="sxs-lookup"><span data-stu-id="06b9c-117">ReadOnly</span></span>
- <span data-ttu-id="06b9c-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="06b9c-118">ReadWrite</span></span>
- <span data-ttu-id="06b9c-119">Żadna wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="06b9c-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="06b9c-120">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="06b9c-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="06b9c-121">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="06b9c-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="06b9c-122">-Opcja</span><span class="sxs-lookup"><span data-stu-id="06b9c-122">-CreateOption</span></span>
<span data-ttu-id="06b9c-123">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="06b9c-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="06b9c-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="06b9c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06b9c-125">Ponowne.</span><span class="sxs-lookup"><span data-stu-id="06b9c-125">Attach.</span></span>
<span data-ttu-id="06b9c-126">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie specjalistycznego dysku.</span><span class="sxs-lookup"><span data-stu-id="06b9c-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="06b9c-127">Po określeniu tej opcji nie określaj parametru *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="06b9c-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="06b9c-128">*VhdUri* to wszystko, co jest potrzebne, aby poinformować platformę Azure o lokalizacji wirtualnego dysku twardego (VHD), który ma zostać dołączony jako dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="06b9c-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="06b9c-129">Wolnego.</span><span class="sxs-lookup"><span data-stu-id="06b9c-129">Empty.</span></span>
<span data-ttu-id="06b9c-130">Określ, czy chcesz utworzyć pusty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="06b9c-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="06b9c-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="06b9c-131">FromImage.</span></span>
<span data-ttu-id="06b9c-132">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie uogólnionego obrazu lub dysku.</span><span class="sxs-lookup"><span data-stu-id="06b9c-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="06b9c-133">Po określeniu tej opcji należy określić również parametr *SourceImageUri* , aby wskazać platformę Azure lokalizację dysku VHD, który ma zostać dołączony jako dysk danych.</span><span class="sxs-lookup"><span data-stu-id="06b9c-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="06b9c-134">Parametr *VhdUri* jest wykorzystywany jako lokalizacja identyfikująca lokalizację, w której dysk VHD z danymi będzie przechowywany, gdy jest on wykorzystywany przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="06b9c-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="06b9c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b9c-135">-DefaultProfile</span></span>
<span data-ttu-id="06b9c-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06b9c-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06b9c-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="06b9c-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="06b9c-138">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanego przez klienta.</span><span class="sxs-lookup"><span data-stu-id="06b9c-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="06b9c-139">Ten parametr może być określony tylko dla dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="06b9c-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="06b9c-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="06b9c-140">-DiskSizeInGB</span></span>
<span data-ttu-id="06b9c-141">Określa rozmiar, w gigabajtach, pustego dysku, który ma zostać dołączony do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="06b9c-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="06b9c-142">-LUN</span><span class="sxs-lookup"><span data-stu-id="06b9c-142">-Lun</span></span>
<span data-ttu-id="06b9c-143">Określa logiczny numer jednostki (LUN) dla dysku danych.</span><span class="sxs-lookup"><span data-stu-id="06b9c-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="06b9c-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="06b9c-144">-ManagedDiskId</span></span>
<span data-ttu-id="06b9c-145">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="06b9c-145">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="06b9c-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="06b9c-146">-StorageAccountType</span></span>
<span data-ttu-id="06b9c-147">Określa typ konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="06b9c-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="06b9c-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="06b9c-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="06b9c-149">Określa obiekt maszyny wirtualnej w lokalnej skali maszyny wirtualnej, do którego ma zostać dodany dysk danych.</span><span class="sxs-lookup"><span data-stu-id="06b9c-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="06b9c-150">Za pomocą polecenia cmdlet **Get-AzVmssVM** można uzyskać obiekt maszyny wirtualnej w skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="06b9c-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="06b9c-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="06b9c-151">-WriteAccelerator</span></span>
<span data-ttu-id="06b9c-152">Określa, czy WriteAccelerator powinien być włączony, czy wyłączony na zarządzanym dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="06b9c-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="06b9c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b9c-153">CommonParameters</span></span>
<span data-ttu-id="06b9c-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06b9c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b9c-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06b9c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b9c-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06b9c-156">INPUTS</span></span>

### <span data-ttu-id="06b9c-157">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="06b9c-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="06b9c-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="06b9c-158">System.Int32</span></span>

### <span data-ttu-id="06b9c-159">System. String</span><span class="sxs-lookup"><span data-stu-id="06b9c-159">System.String</span></span>

### <span data-ttu-id="06b9c-160">Microsoft. Azure. Management. COMPUTE. MODELES. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="06b9c-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="06b9c-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06b9c-161">OUTPUTS</span></span>

### <span data-ttu-id="06b9c-162">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="06b9c-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="06b9c-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06b9c-163">NOTES</span></span>

## <span data-ttu-id="06b9c-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06b9c-164">RELATED LINKS</span></span>
