---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 4eefa5a0a22b3db0e7ab10085729e1040dbd4e71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181586"
---
# <span data-ttu-id="33a1f-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="33a1f-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="33a1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="33a1f-103">Tworzy lokalny obiekt dysku danych dla maszyny wirtualnej lub maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="33a1f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33a1f-104">SYNTAX</span></span>

### <span data-ttu-id="33a1f-105">NormalMeterParameterSetName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="33a1f-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33a1f-106">ManagedMeterParameterSetName</span><span class="sxs-lookup"><span data-stu-id="33a1f-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33a1f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="33a1f-107">DESCRIPTION</span></span>
<span data-ttu-id="33a1f-108">Polecenie **cmdlet New-AzVMDataData Umożliwia** utworzenie lokalnego obiektu dysku danych dla maszyny wirtualnej lub maszyny wirtualnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="33a1f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33a1f-109">EXAMPLES</span></span>

### <span data-ttu-id="33a1f-110">Przykład 1. Dodawanie zarządzanego dysku danych do maszyny wirtualnej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="33a1f-111">Pierwsze polecenie otrzymuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="33a1f-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="33a1f-112">Następne polecenie tworzy obiekt dysku danych z dyskiem zarządzanym.</span><span class="sxs-lookup"><span data-stu-id="33a1f-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="33a1f-113">Następne polecenie pobiera istniejącą maszynę wirtualnej maszyny wirtualnej, która jest podana przez nazwę grupy zasobów, nazwę maszyny wirtualnej i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="33a1f-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="33a1f-114">Końcowe polecenie aktualizuje maszynę wirtualnej maszyny wirtualnej przez dodanie nowego dysku danych.</span><span class="sxs-lookup"><span data-stu-id="33a1f-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="33a1f-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="33a1f-115">Example 2</span></span>

<span data-ttu-id="33a1f-116">Tworzy lokalny obiekt dysku danych dla maszyny wirtualnej lub maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="33a1f-117">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="33a1f-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="33a1f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33a1f-118">PARAMETERS</span></span>

### <span data-ttu-id="33a1f-119">— buforowanie</span><span class="sxs-lookup"><span data-stu-id="33a1f-119">-Caching</span></span>
<span data-ttu-id="33a1f-120">Buforowanie dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-120">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="33a1f-121">— CreateOption</span><span class="sxs-lookup"><span data-stu-id="33a1f-121">-CreateOption</span></span>
<span data-ttu-id="33a1f-122">Opcja tworzenia dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-122">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33a1f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a1f-123">-DefaultProfile</span></span>
<span data-ttu-id="33a1f-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="33a1f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33a1f-125">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="33a1f-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="33a1f-126">Identyfikator zestawu szyfrowania dysku zarządzanego przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="33a1f-126">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="33a1f-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="33a1f-127">-DiskSizeInGB</span></span>
<span data-ttu-id="33a1f-128">Rozmiar dysku danych maszyny wirtualnej w GB.</span><span class="sxs-lookup"><span data-stu-id="33a1f-128">The virtual machine data disk's size in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33a1f-129">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="33a1f-129">-Lun</span></span>
<span data-ttu-id="33a1f-130">Serwer danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-130">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33a1f-131">-Managed Jednakid</span><span class="sxs-lookup"><span data-stu-id="33a1f-131">-ManagedDiskId</span></span>
<span data-ttu-id="33a1f-132">Identyfikator dysku zarządzanego przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="33a1f-132">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33a1f-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="33a1f-133">-Name</span></span>
<span data-ttu-id="33a1f-134">Nazwa dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="33a1f-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="33a1f-135">-SourceImageUri</span></span>
<span data-ttu-id="33a1f-136">Uri źródła dysku systemu operacyjnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-136">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33a1f-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="33a1f-137">-StorageAccountType</span></span>
<span data-ttu-id="33a1f-138">Typ konta zarządzanego przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="33a1f-138">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33a1f-139">- VhdUri</span><span class="sxs-lookup"><span data-stu-id="33a1f-139">-VhdUri</span></span>
<span data-ttu-id="33a1f-140">Wirtualny Uri na dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="33a1f-140">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33a1f-141">- WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="33a1f-141">-WriteAccelerator</span></span>
<span data-ttu-id="33a1f-142">Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na zarządzanym dysku danych.</span><span class="sxs-lookup"><span data-stu-id="33a1f-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a1f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a1f-143">CommonParameters</span></span>
<span data-ttu-id="33a1f-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a1f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a1f-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33a1f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a1f-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33a1f-146">INPUTS</span></span>

### <span data-ttu-id="33a1f-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="33a1f-147">System.Int32</span></span>

### <span data-ttu-id="33a1f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="33a1f-148">System.String</span></span>

### <span data-ttu-id="33a1f-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="33a1f-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="33a1f-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="33a1f-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="33a1f-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33a1f-151">OUTPUTS</span></span>

### <span data-ttu-id="33a1f-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataData1</span><span class="sxs-lookup"><span data-stu-id="33a1f-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="33a1f-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33a1f-153">NOTES</span></span>

## <span data-ttu-id="33a1f-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33a1f-154">RELATED LINKS</span></span>
