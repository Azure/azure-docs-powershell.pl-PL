---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 4eefa5a0a22b3db0e7ab10085729e1040dbd4e71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504069"
---
# <span data-ttu-id="6e629-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6e629-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="6e629-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e629-102">SYNOPSIS</span></span>
<span data-ttu-id="6e629-103">Tworzy obiekt lokalnego dysku danych dla maszyny wirtualnej lub maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="6e629-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="6e629-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e629-104">SYNTAX</span></span>

### <span data-ttu-id="6e629-105">NormalDiskParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6e629-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e629-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6e629-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e629-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6e629-107">DESCRIPTION</span></span>
<span data-ttu-id="6e629-108">Polecenie cmdlet **New-AzVMDataDisk** tworzy obiekt lokalnego dysku danych dla maszyny wirtualnej lub VMSS maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e629-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="6e629-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e629-109">EXAMPLES</span></span>

### <span data-ttu-id="6e629-110">Przykład 1: dodanie zarządzanego dysku danych do maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="6e629-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="6e629-111">Pierwsze polecenie uzyskuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="6e629-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="6e629-112">Polecenie następne powoduje utworzenie obiektu dysk danych z zarządzanym dyskiem.</span><span class="sxs-lookup"><span data-stu-id="6e629-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="6e629-113">Następne polecenie pobiera istniejącą maszynę wirtualną VMSS określoną przez nazwę grupy zasobów, nazwę VMSS i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="6e629-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="6e629-114">Ostatnie polecenie aktualizuje VMSS VM, dodając nowy dysk danych.</span><span class="sxs-lookup"><span data-stu-id="6e629-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="6e629-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6e629-115">Example 2</span></span>

<span data-ttu-id="6e629-116">Tworzy obiekt lokalnego dysku danych dla maszyny wirtualnej lub maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="6e629-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="6e629-117">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="6e629-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="6e629-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e629-118">PARAMETERS</span></span>

### <span data-ttu-id="6e629-119">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="6e629-119">-Caching</span></span>
<span data-ttu-id="6e629-120">Buforowanie dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e629-120">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="6e629-121">-Opcja</span><span class="sxs-lookup"><span data-stu-id="6e629-121">-CreateOption</span></span>
<span data-ttu-id="6e629-122">Opcja tworzenia dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e629-122">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="6e629-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e629-123">-DefaultProfile</span></span>
<span data-ttu-id="6e629-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e629-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e629-125">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="6e629-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="6e629-126">Identyfikator zestawu szyfrowania dysków zarządzanego przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="6e629-126">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="6e629-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="6e629-127">-DiskSizeInGB</span></span>
<span data-ttu-id="6e629-128">Rozmiar dysku danych maszyny wirtualnej w GB.</span><span class="sxs-lookup"><span data-stu-id="6e629-128">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="6e629-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="6e629-129">-Lun</span></span>
<span data-ttu-id="6e629-130">Jednostka LUN dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e629-130">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="6e629-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="6e629-131">-ManagedDiskId</span></span>
<span data-ttu-id="6e629-132">Identyfikator dysku zarządzanego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e629-132">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="6e629-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e629-133">-Name</span></span>
<span data-ttu-id="6e629-134">Nazwa dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e629-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="6e629-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="6e629-135">-SourceImageUri</span></span>
<span data-ttu-id="6e629-136">Identyfikator URI obrazu źródłowego dysku systemu operacyjnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e629-136">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="6e629-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6e629-137">-StorageAccountType</span></span>
<span data-ttu-id="6e629-138">Typ konta dysk zarządzany maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e629-138">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="6e629-139">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="6e629-139">-VhdUri</span></span>
<span data-ttu-id="6e629-140">Identyfikator URI wirtualnego dysku twardego z danymi maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6e629-140">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="6e629-141">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="6e629-141">-WriteAccelerator</span></span>
<span data-ttu-id="6e629-142">Określa, czy WriteAccelerator powinien być włączony, czy wyłączony na zarządzanym dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="6e629-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="6e629-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e629-143">CommonParameters</span></span>
<span data-ttu-id="6e629-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e629-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e629-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e629-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e629-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e629-146">INPUTS</span></span>

### <span data-ttu-id="6e629-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6e629-147">System.Int32</span></span>

### <span data-ttu-id="6e629-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6e629-148">System.String</span></span>

### <span data-ttu-id="6e629-149">Microsoft. Azure. Management. COMPUTE. MODELES. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="6e629-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="6e629-150">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6e629-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6e629-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e629-151">OUTPUTS</span></span>

### <span data-ttu-id="6e629-152">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="6e629-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="6e629-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e629-153">NOTES</span></span>

## <span data-ttu-id="6e629-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e629-154">RELATED LINKS</span></span>
