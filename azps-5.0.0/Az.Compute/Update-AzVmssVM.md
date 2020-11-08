---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225722"
---
# <span data-ttu-id="1e0e0-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="1e0e0-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="1e0e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0e0-103">Umożliwia zaktualizowanie stanu maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="1e0e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e0e0-104">SYNTAX</span></span>

### <span data-ttu-id="1e0e0-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1e0e0-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e0e0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1e0e0-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e0e0-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1e0e0-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e0e0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1e0e0-108">DESCRIPTION</span></span>
<span data-ttu-id="1e0e0-109">Umożliwia zaktualizowanie stanu maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="1e0e0-110">Na razie jedyną dozwoloną aktualizacją jest dodawanie dysku z danymi zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="1e0e0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e0e0-111">EXAMPLES</span></span>

### <span data-ttu-id="1e0e0-112">Przykład 1: Dodawanie zarządzanego dysku danych do maszyny wirtualnej VMSS przy użyciu New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1e0e0-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="1e0e0-113">Pierwsze polecenie uzyskuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="1e0e0-114">Polecenie następne powoduje utworzenie obiektu dysk danych z zarządzanym dyskiem.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="1e0e0-115">Następne polecenie pobiera istniejącą maszynę wirtualną VMSS określoną przez nazwę grupy zasobów, nazwę VMSS i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="1e0e0-116">Ostatnie polecenie aktualizuje VMSS VM, dodając nowy dysk danych.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="1e0e0-117">Przykład 2: Dodawanie zarządzanego dysku danych do maszyny wirtualnej VMSS przy użyciu Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1e0e0-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="1e0e0-118">Pierwsze polecenie uzyskuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="1e0e0-119">Następne polecenie pobiera istniejącą maszynę wirtualną VMSS określoną przez nazwę grupy zasobów, nazwę VMSS i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="1e0e0-120">Polecenie Next (następne) dodaje dysk zarządzany do maszyny wirtualnej VMSS zapisanej lokalnie w $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="1e0e0-121">W ostatnim poleceniu zostanie zaktualizowana maszyna wirtualna VMSS z dodanym dyskiem danych.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="1e0e0-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1e0e0-122">Example 3</span></span>

<span data-ttu-id="1e0e0-123">Umożliwia zaktualizowanie stanu maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="1e0e0-124">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="1e0e0-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="1e0e0-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e0e0-125">PARAMETERS</span></span>

### <span data-ttu-id="1e0e0-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e0e0-126">-AsJob</span></span>
<span data-ttu-id="1e0e0-127">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1e0e0-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e0e0-128">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="1e0e0-128">-DataDisk</span></span>

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

### <span data-ttu-id="1e0e0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0e0-129">-DefaultProfile</span></span>
<span data-ttu-id="1e0e0-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e0e0-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1e0e0-131">-InstanceId</span></span>
<span data-ttu-id="1e0e0-132">Określa identyfikator wystąpienia maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="1e0e0-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="1e0e0-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="1e0e0-134">Wskazuje, że nie należy brać pod uwagę zestawu skali maszyny wirtualnej w celu usunięcia podczas operacji skalowania.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="1e0e0-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="1e0e0-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="1e0e0-136">Wskazuje, że aktualizacje lub akcje modelu (w tym skalowanie) zainicjowane na VMSS nie powinny być stosowane do maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="1e0e0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e0e0-137">-ResourceGroupName</span></span>
<span data-ttu-id="1e0e0-138">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="1e0e0-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e0e0-139">-ResourceId</span></span>
<span data-ttu-id="1e0e0-140">Identyfikator zasobu zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1e0e0-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="1e0e0-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1e0e0-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="1e0e0-142">Obiekt maszyny wirtualnej ustawienia lokalnej skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1e0e0-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="1e0e0-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1e0e0-143">-VMScaleSetName</span></span>
<span data-ttu-id="1e0e0-144">Nazwa zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1e0e0-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="1e0e0-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e0e0-145">-Confirm</span></span>
<span data-ttu-id="1e0e0-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e0e0-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e0e0-147">-WhatIf</span></span>
<span data-ttu-id="1e0e0-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e0e0-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e0e0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0e0-150">CommonParameters</span></span>
<span data-ttu-id="1e0e0-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e0e0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0e0-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e0e0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0e0-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e0e0-153">INPUTS</span></span>

### <span data-ttu-id="1e0e0-154">System. String</span><span class="sxs-lookup"><span data-stu-id="1e0e0-154">System.String</span></span>

### <span data-ttu-id="1e0e0-155">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="1e0e0-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="1e0e0-156">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1e0e0-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="1e0e0-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e0e0-157">OUTPUTS</span></span>

### <span data-ttu-id="1e0e0-158">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1e0e0-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="1e0e0-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e0e0-159">NOTES</span></span>

## <span data-ttu-id="1e0e0-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e0e0-160">RELATED LINKS</span></span>
