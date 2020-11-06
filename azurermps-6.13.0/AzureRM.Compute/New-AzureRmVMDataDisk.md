---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMDataDisk.md
ms.openlocfilehash: 6eb86e0c2ddb8c5e3a46cf10f98bcea52ba03dd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548835"
---
# <span data-ttu-id="97be4-101">New-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="97be4-101">New-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="97be4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97be4-102">SYNOPSIS</span></span>
<span data-ttu-id="97be4-103">Tworzy obiekt lokalnego dysku danych dla maszyny wirtualnej lub maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="97be4-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97be4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97be4-104">SYNTAX</span></span>

### <span data-ttu-id="97be4-105">NormalDiskParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="97be4-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzureRmVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97be4-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="97be4-106">ManagedDiskParameterSetName</span></span>
```
New-AzureRmVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97be4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="97be4-107">DESCRIPTION</span></span>
<span data-ttu-id="97be4-108">Polecenie cmdlet **New-AzureRmVMDataDisk** tworzy obiekt lokalnego dysku danych dla maszyny wirtualnej lub VMSS maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97be4-108">The **New-AzureRmVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="97be4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97be4-109">EXAMPLES</span></span>

### <span data-ttu-id="97be4-110">Przykład 1: dodanie zarządzanego dysku danych do maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="97be4-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzureRmVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="97be4-111">Pierwsze polecenie uzyskuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="97be4-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="97be4-112">Polecenie następne powoduje utworzenie obiektu dysk danych z zarządzanym dyskiem.</span><span class="sxs-lookup"><span data-stu-id="97be4-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="97be4-113">Następne polecenie pobiera istniejącą maszynę wirtualną VMSS określoną przez nazwę grupy zasobów, nazwę VMSS i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="97be4-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="97be4-114">Ostatnie polecenie aktualizuje VMSS VM, dodając nowy dysk danych.</span><span class="sxs-lookup"><span data-stu-id="97be4-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="97be4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97be4-115">PARAMETERS</span></span>

### <span data-ttu-id="97be4-116">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="97be4-116">-Caching</span></span>
<span data-ttu-id="97be4-117">Buforowanie dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97be4-117">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="97be4-118">-Opcja</span><span class="sxs-lookup"><span data-stu-id="97be4-118">-CreateOption</span></span>
<span data-ttu-id="97be4-119">Opcja tworzenia dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97be4-119">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="97be4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97be4-120">-DefaultProfile</span></span>
<span data-ttu-id="97be4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97be4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97be4-122">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="97be4-122">-DiskSizeInGB</span></span>
<span data-ttu-id="97be4-123">Rozmiar dysku danych maszyny wirtualnej w GB.</span><span class="sxs-lookup"><span data-stu-id="97be4-123">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="97be4-124">-LUN</span><span class="sxs-lookup"><span data-stu-id="97be4-124">-Lun</span></span>
<span data-ttu-id="97be4-125">Jednostka LUN dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97be4-125">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="97be4-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="97be4-126">-ManagedDiskId</span></span>
<span data-ttu-id="97be4-127">Identyfikator dysku zarządzanego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97be4-127">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="97be4-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97be4-128">-Name</span></span>
<span data-ttu-id="97be4-129">Nazwa dysku danych maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97be4-129">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="97be4-130">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="97be4-130">-SourceImageUri</span></span>
<span data-ttu-id="97be4-131">Identyfikator URI obrazu źródłowego dysku systemu operacyjnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97be4-131">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="97be4-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="97be4-132">-StorageAccountType</span></span>
<span data-ttu-id="97be4-133">Typ konta dysk zarządzany maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97be4-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="97be4-134">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="97be4-134">-VhdUri</span></span>
<span data-ttu-id="97be4-135">Identyfikator URI wirtualnego dysku twardego z danymi maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97be4-135">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="97be4-136">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="97be4-136">-WriteAccelerator</span></span>
<span data-ttu-id="97be4-137">Określa, czy WriteAccelerator powinien być włączony, czy wyłączony na zarządzanym dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="97be4-137">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="97be4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97be4-138">CommonParameters</span></span>
<span data-ttu-id="97be4-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97be4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97be4-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97be4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97be4-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97be4-141">INPUTS</span></span>

### <span data-ttu-id="97be4-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="97be4-142">System.Int32</span></span>

### <span data-ttu-id="97be4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="97be4-143">System.String</span></span>

### <span data-ttu-id="97be4-144">Microsoft. Azure. Management. COMPUTE. MODELES. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="97be4-144">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="97be4-145">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="97be4-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="97be4-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97be4-146">OUTPUTS</span></span>

### <span data-ttu-id="97be4-147">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="97be4-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="97be4-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97be4-148">NOTES</span></span>

## <span data-ttu-id="97be4-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97be4-149">RELATED LINKS</span></span>
