---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: d5dc3afe69495e5fef8c0a1ad5a9d155fd15d295
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710161"
---
# <span data-ttu-id="38b5e-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="38b5e-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="38b5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="38b5e-103">Umożliwia zaktualizowanie stanu maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="38b5e-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="38b5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38b5e-104">SYNTAX</span></span>

### <span data-ttu-id="38b5e-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="38b5e-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b5e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="38b5e-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b5e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="38b5e-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38b5e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="38b5e-108">DESCRIPTION</span></span>
<span data-ttu-id="38b5e-109">Umożliwia zaktualizowanie stanu maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="38b5e-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="38b5e-110">Na razie jedyną dozwoloną aktualizacją jest dodawanie dysku z danymi zarządzanymi.</span><span class="sxs-lookup"><span data-stu-id="38b5e-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="38b5e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38b5e-111">EXAMPLES</span></span>

### <span data-ttu-id="38b5e-112">Przykład 1: Dodawanie zarządzanego dysku danych do maszyny wirtualnej VMSS przy użyciu New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="38b5e-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="38b5e-113">Pierwsze polecenie uzyskuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="38b5e-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="38b5e-114">Polecenie następne powoduje utworzenie obiektu dysk danych z zarządzanym dyskiem.</span><span class="sxs-lookup"><span data-stu-id="38b5e-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="38b5e-115">Następne polecenie pobiera istniejącą maszynę wirtualną VMSS określoną przez nazwę grupy zasobów, nazwę VMSS i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="38b5e-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="38b5e-116">Ostatnie polecenie aktualizuje VMSS VM, dodając nowy dysk danych.</span><span class="sxs-lookup"><span data-stu-id="38b5e-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="38b5e-117">Przykład 2: Dodawanie zarządzanego dysku danych do maszyny wirtualnej VMSS przy użyciu Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="38b5e-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="38b5e-118">Pierwsze polecenie uzyskuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="38b5e-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="38b5e-119">Następne polecenie pobiera istniejącą maszynę wirtualną VMSS określoną przez nazwę grupy zasobów, nazwę VMSS i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="38b5e-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="38b5e-120">Polecenie Next (następne) dodaje dysk zarządzany do maszyny wirtualnej VMSS zapisanej lokalnie w $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="38b5e-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="38b5e-121">W ostatnim poleceniu zostanie zaktualizowana maszyna wirtualna VMSS z dodanym dyskiem danych.</span><span class="sxs-lookup"><span data-stu-id="38b5e-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="38b5e-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38b5e-122">PARAMETERS</span></span>

### <span data-ttu-id="38b5e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38b5e-123">-AsJob</span></span>
<span data-ttu-id="38b5e-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="38b5e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38b5e-125">-Datadysk</span><span class="sxs-lookup"><span data-stu-id="38b5e-125">-DataDisk</span></span>

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

### <span data-ttu-id="38b5e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b5e-126">-DefaultProfile</span></span>
<span data-ttu-id="38b5e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38b5e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b5e-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="38b5e-128">-InstanceId</span></span>
<span data-ttu-id="38b5e-129">Określa identyfikator wystąpienia maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="38b5e-129">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="38b5e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b5e-130">-ResourceGroupName</span></span>
<span data-ttu-id="38b5e-131">Określa nazwę grupy zasobów VMSS.</span><span class="sxs-lookup"><span data-stu-id="38b5e-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="38b5e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38b5e-132">-ResourceId</span></span>
<span data-ttu-id="38b5e-133">Identyfikator zasobu zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="38b5e-133">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="38b5e-134">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="38b5e-134">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="38b5e-135">Obiekt maszyny wirtualnej ustawienia lokalnej skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="38b5e-135">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="38b5e-136">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="38b5e-136">-VMScaleSetName</span></span>
<span data-ttu-id="38b5e-137">Nazwa zestawu skali maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="38b5e-137">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="38b5e-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38b5e-138">-Confirm</span></span>
<span data-ttu-id="38b5e-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b5e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b5e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b5e-140">-WhatIf</span></span>
<span data-ttu-id="38b5e-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b5e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38b5e-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="38b5e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b5e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b5e-143">CommonParameters</span></span>
<span data-ttu-id="38b5e-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b5e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b5e-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b5e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b5e-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38b5e-146">INPUTS</span></span>

### <span data-ttu-id="38b5e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="38b5e-147">System.String</span></span>

### <span data-ttu-id="38b5e-148">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="38b5e-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="38b5e-149">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="38b5e-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="38b5e-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38b5e-150">OUTPUTS</span></span>

### <span data-ttu-id="38b5e-151">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="38b5e-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="38b5e-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38b5e-152">NOTES</span></span>

## <span data-ttu-id="38b5e-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38b5e-153">RELATED LINKS</span></span>
