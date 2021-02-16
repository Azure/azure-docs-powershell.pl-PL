---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194955"
---
# <span data-ttu-id="94332-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="94332-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="94332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94332-102">SYNOPSIS</span></span>
<span data-ttu-id="94332-103">Aktualizuje stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94332-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="94332-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94332-104">SYNTAX</span></span>

### <span data-ttu-id="94332-105">DefaultParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="94332-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94332-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="94332-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94332-107">ObjectParameters</span><span class="sxs-lookup"><span data-stu-id="94332-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94332-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="94332-108">DESCRIPTION</span></span>
<span data-ttu-id="94332-109">Aktualizuje stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94332-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="94332-110">Obecnie jedyną dozwoloną aktualizacją jest dodanie zarządzanego dysku danych.</span><span class="sxs-lookup"><span data-stu-id="94332-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="94332-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94332-111">EXAMPLES</span></span>

### <span data-ttu-id="94332-112">Przykład 1. Dodawanie zarządzanego dysku danych do maszyny wirtualnej maszyny wirtualnej przy użyciu New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="94332-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="94332-113">Pierwsze polecenie otrzymuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="94332-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="94332-114">Następne polecenie tworzy obiekt dysku danych z dyskiem zarządzanym.</span><span class="sxs-lookup"><span data-stu-id="94332-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="94332-115">Następne polecenie pobiera istniejącą maszynę wirtualnej maszyny wirtualnej maszyny wirtualnej, która jest podana przez nazwę grupy zasobów, nazwę maszyny wirtualnej i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="94332-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="94332-116">Końcowe polecenie aktualizuje maszynę wirtualnej maszyny wirtualnej przez dodanie nowego dysku danych.</span><span class="sxs-lookup"><span data-stu-id="94332-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="94332-117">Przykład 2. Dodawanie zarządzanego dysku danych do maszyny wirtualnej maszyny wirtualnej przy użyciu Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="94332-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="94332-118">Pierwsze polecenie otrzymuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="94332-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="94332-119">Następne polecenie pobiera istniejącą maszynę wirtualnej maszyny wirtualnej, która jest podana przez nazwę grupy zasobów, nazwę maszyny wirtualnej i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="94332-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="94332-120">Następne polecenie dodaje dysk zarządzany do maszyny wirtualnej maszyny wirtualnej przechowywanej lokalnie w $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="94332-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="94332-121">Końcowe polecenie aktualizuje maszynę wirtualnej maszyny wirtualnej z dodanym dyskiem danych.</span><span class="sxs-lookup"><span data-stu-id="94332-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="94332-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="94332-122">Example 3</span></span>

<span data-ttu-id="94332-123">Aktualizuje stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94332-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="94332-124">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="94332-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="94332-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94332-125">PARAMETERS</span></span>

### <span data-ttu-id="94332-126">— AsJob</span><span class="sxs-lookup"><span data-stu-id="94332-126">-AsJob</span></span>
<span data-ttu-id="94332-127">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="94332-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94332-128">-DataDrive</span><span class="sxs-lookup"><span data-stu-id="94332-128">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94332-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94332-129">-DefaultProfile</span></span>
<span data-ttu-id="94332-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94332-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94332-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="94332-131">-InstanceId</span></span>
<span data-ttu-id="94332-132">Określa identyfikator wystąpienia maszyny wirtualnej maszyny wirtualnej maszyny wirtualnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94332-132">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94332-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="94332-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="94332-134">Wskazuje, że podczas operacji skalowania nie należy traktować maszyny wirtualnej jako zestawu skalowania maszyny wirtualnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="94332-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94332-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="94332-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="94332-136">Wskazuje, że aktualizacje modelu lub akcje (w tym skalowanie) zainicjowane w usługach WIRTUALNYCHSS nie powinny być stosowane do maszyny wirtualnej MASZYNY WIRTUALNEJ.</span><span class="sxs-lookup"><span data-stu-id="94332-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94332-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94332-137">-ResourceGroupName</span></span>
<span data-ttu-id="94332-138">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="94332-138">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94332-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94332-139">-ResourceId</span></span>
<span data-ttu-id="94332-140">Identyfikator zasobu dla zestawu maszyn wirtualnych do skalowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="94332-140">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94332-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="94332-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="94332-142">Lokalny obiekt skalowania maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="94332-142">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94332-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="94332-143">-VMScaleSetName</span></span>
<span data-ttu-id="94332-144">Nazwa zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="94332-144">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94332-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94332-145">-Confirm</span></span>
<span data-ttu-id="94332-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94332-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94332-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94332-147">-WhatIf</span></span>
<span data-ttu-id="94332-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94332-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94332-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94332-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94332-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94332-150">CommonParameters</span></span>
<span data-ttu-id="94332-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94332-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94332-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94332-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94332-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94332-153">INPUTS</span></span>

### <span data-ttu-id="94332-154">System.String</span><span class="sxs-lookup"><span data-stu-id="94332-154">System.String</span></span>

### <span data-ttu-id="94332-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataData(]</span><span class="sxs-lookup"><span data-stu-id="94332-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="94332-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="94332-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="94332-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94332-157">OUTPUTS</span></span>

### <span data-ttu-id="94332-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="94332-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="94332-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94332-159">NOTES</span></span>

## <span data-ttu-id="94332-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94332-160">RELATED LINKS</span></span>
