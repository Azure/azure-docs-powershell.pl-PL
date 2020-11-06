---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: c4a4aa530f29de93458f618dbf45f639fe873f1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547492"
---
# <span data-ttu-id="8d950-101">Add-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8d950-101">Add-AzureRmVmssVMDataDisk</span></span>

## <span data-ttu-id="8d950-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d950-102">SYNOPSIS</span></span>
<span data-ttu-id="8d950-103">Dodaje dysk danych do maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d950-103">Adds a data disk to a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d950-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d950-104">SYNTAX</span></span>

```
Add-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d950-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8d950-105">DESCRIPTION</span></span>
<span data-ttu-id="8d950-106">Polecenie cmdlet **Add-AzureRmVmssVMDataDisk** umożliwia dodanie dysku z danymi do VMSS maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d950-106">The **Add-AzureRmVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="8d950-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d950-107">EXAMPLES</span></span>

### <span data-ttu-id="8d950-108">Przykład 1: dodanie zarządzanego dysku danych do maszyny wirtualnej VMSS.</span><span class="sxs-lookup"><span data-stu-id="8d950-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="8d950-109">Pierwsze polecenie uzyskuje istniejący dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="8d950-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="8d950-110">Następne polecenie pobiera istniejącą maszynę wirtualną VMSS określoną przez nazwę grupy zasobów, nazwę VMSS i identyfikator wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="8d950-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="8d950-111">Polecenie Next (następne) dodaje dysk zarządzany do maszyny wirtualnej VMSS zapisanej lokalnie w $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="8d950-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="8d950-112">W ostatnim poleceniu zostanie zaktualizowana maszyna wirtualna VMSS z dodanym dyskiem danych.</span><span class="sxs-lookup"><span data-stu-id="8d950-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="8d950-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d950-113">PARAMETERS</span></span>

### <span data-ttu-id="8d950-114">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="8d950-114">-Caching</span></span>
<span data-ttu-id="8d950-115">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="8d950-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="8d950-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8d950-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d950-117">Odczytu</span><span class="sxs-lookup"><span data-stu-id="8d950-117">ReadOnly</span></span>
- <span data-ttu-id="8d950-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8d950-118">ReadWrite</span></span>
- <span data-ttu-id="8d950-119">Żadna wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="8d950-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="8d950-120">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d950-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="8d950-121">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="8d950-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="8d950-122">-Opcja</span><span class="sxs-lookup"><span data-stu-id="8d950-122">-CreateOption</span></span>
<span data-ttu-id="8d950-123">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="8d950-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="8d950-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8d950-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d950-125">Ponowne.</span><span class="sxs-lookup"><span data-stu-id="8d950-125">Attach.</span></span>
<span data-ttu-id="8d950-126">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie specjalistycznego dysku.</span><span class="sxs-lookup"><span data-stu-id="8d950-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="8d950-127">Po określeniu tej opcji nie określaj parametru *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="8d950-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="8d950-128">*VhdUri* to wszystko, co jest potrzebne, aby poinformować platformę Azure o lokalizacji wirtualnego dysku twardego (VHD), który ma zostać dołączony jako dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d950-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="8d950-129">Wolnego.</span><span class="sxs-lookup"><span data-stu-id="8d950-129">Empty.</span></span>
<span data-ttu-id="8d950-130">Określ, czy chcesz utworzyć pusty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="8d950-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="8d950-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="8d950-131">FromImage.</span></span>
<span data-ttu-id="8d950-132">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie uogólnionego obrazu lub dysku.</span><span class="sxs-lookup"><span data-stu-id="8d950-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="8d950-133">Po określeniu tej opcji należy określić również parametr *SourceImageUri* , aby wskazać platformę Azure lokalizację dysku VHD, który ma zostać dołączony jako dysk danych.</span><span class="sxs-lookup"><span data-stu-id="8d950-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="8d950-134">Parametr *VhdUri* jest wykorzystywany jako lokalizacja identyfikująca lokalizację, w której dysk VHD z danymi będzie przechowywany, gdy jest on wykorzystywany przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="8d950-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="8d950-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d950-135">-DefaultProfile</span></span>
<span data-ttu-id="8d950-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d950-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d950-137">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8d950-137">-DiskSizeInGB</span></span>
<span data-ttu-id="8d950-138">Określa rozmiar, w gigabajtach, pustego dysku, który ma zostać dołączony do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d950-138">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="8d950-139">-LUN</span><span class="sxs-lookup"><span data-stu-id="8d950-139">-Lun</span></span>
<span data-ttu-id="8d950-140">Określa logiczny numer jednostki (LUN) dla dysku danych.</span><span class="sxs-lookup"><span data-stu-id="8d950-140">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="8d950-141">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="8d950-141">-ManagedDiskId</span></span>
<span data-ttu-id="8d950-142">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="8d950-142">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="8d950-143">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8d950-143">-StorageAccountType</span></span>
<span data-ttu-id="8d950-144">Określa typ konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="8d950-144">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="8d950-145">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="8d950-145">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="8d950-146">Określa obiekt maszyny wirtualnej w lokalnej skali maszyny wirtualnej, do którego ma zostać dodany dysk danych.</span><span class="sxs-lookup"><span data-stu-id="8d950-146">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="8d950-147">Za pomocą polecenia cmdlet **Get-AzureRmVmssVM** można uzyskać obiekt maszyny wirtualnej w skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8d950-147">You can use the **Get-AzureRmVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d950-148">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="8d950-148">-WriteAccelerator</span></span>
<span data-ttu-id="8d950-149">Określa, czy WriteAccelerator powinien być włączony, czy wyłączony na zarządzanym dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="8d950-149">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="8d950-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d950-150">CommonParameters</span></span>
<span data-ttu-id="8d950-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d950-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d950-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d950-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d950-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d950-153">INPUTS</span></span>

### <span data-ttu-id="8d950-154">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="8d950-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="8d950-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8d950-155">System.Int32</span></span>

### <span data-ttu-id="8d950-156">System. String</span><span class="sxs-lookup"><span data-stu-id="8d950-156">System.String</span></span>

### <span data-ttu-id="8d950-157">Microsoft. Azure. Management. COMPUTE. MODELES. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="8d950-157">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="8d950-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d950-158">OUTPUTS</span></span>

### <span data-ttu-id="8d950-159">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="8d950-159">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="8d950-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d950-160">NOTES</span></span>

## <span data-ttu-id="8d950-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d950-161">RELATED LINKS</span></span>
