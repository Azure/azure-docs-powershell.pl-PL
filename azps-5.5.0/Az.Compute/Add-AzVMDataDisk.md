---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199370"
---
# <span data-ttu-id="276cd-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="276cd-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="276cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="276cd-102">SYNOPSIS</span></span>
<span data-ttu-id="276cd-103">Dodaje dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="276cd-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="276cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="276cd-104">SYNTAX</span></span>

### <span data-ttu-id="276cd-105">VmNormalMeterParameterSetName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="276cd-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="276cd-106">VmManagedMeterParameterSetName</span><span class="sxs-lookup"><span data-stu-id="276cd-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="276cd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="276cd-107">DESCRIPTION</span></span>
<span data-ttu-id="276cd-108">Polecenie **cmdlet Add-AzVMDataData Umożliwia** dodanie dysku danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="276cd-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="276cd-109">Możesz dodać dysk danych podczas tworzenia maszyny wirtualnej lub dodać dysk danych do istniejącej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="276cd-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="276cd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="276cd-110">EXAMPLES</span></span>

### <span data-ttu-id="276cd-111">Przykład 1. Dodawanie dysków danych do nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="276cd-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="276cd-112">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="276cd-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="276cd-113">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="276cd-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="276cd-114">Następne trzy polecenia przypiszą ścieżki trzech dysków danych do zmiennych $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="276cd-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="276cd-115">Ta metoda ma na celu tylko czytelność następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="276cd-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="276cd-116">Ostatnie trzy polecenia każdego z nich dodają dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="276cd-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="276cd-117">To polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="276cd-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="276cd-118">URI każdego dysku jest przechowywany w $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="276cd-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="276cd-119">Przykład 2. Dodawanie dysku danych do istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="276cd-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="276cd-120">Pierwsze polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet [Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="276cd-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="276cd-121">Polecenie przechowuje maszynę wirtualną w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="276cd-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="276cd-122">Drugie polecenie powoduje dodanie dysku danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="276cd-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="276cd-123">Ostatnie polecenie aktualizuje stan maszyny wirtualnej przechowywanej w u $VirtualMachine ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="276cd-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="276cd-124">Przykład 3. Dodawanie dysku danych do nowej maszyny wirtualnej z ogólnego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="276cd-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="276cd-125">Pierwsze polecenie tworzy obiekt maszyny wirtualnej i przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="276cd-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="276cd-126">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="276cd-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="276cd-127">Następne dwa polecenia przypiszą ścieżki obrazu danych i dyskryminowania danych do $DataImageUri i $DataDiskUri zmiennych.</span><span class="sxs-lookup"><span data-stu-id="276cd-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="276cd-128">Ta metoda ma na celu poprawę czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="276cd-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="276cd-129">Końcowe polecenia dodają dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="276cd-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="276cd-130">To polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="276cd-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="276cd-131">Przykład 4. Dodawanie dyskerów danych do nowej maszyny wirtualnej z specjalistycznego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="276cd-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="276cd-132">Pierwsze polecenie tworzy obiekt maszyny wirtualnej i przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="276cd-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="276cd-133">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="276cd-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="276cd-134">Następne polecenia przypisze ścieżki dysku danych do zmiennej $DataDiskUri danych.</span><span class="sxs-lookup"><span data-stu-id="276cd-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="276cd-135">Ta metoda ma na celu poprawę czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="276cd-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="276cd-136">Ostatnie polecenie dodaje dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="276cd-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="276cd-137">To polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="276cd-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="276cd-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="276cd-138">PARAMETERS</span></span>

### <span data-ttu-id="276cd-139">— buforowanie</span><span class="sxs-lookup"><span data-stu-id="276cd-139">-Caching</span></span>
<span data-ttu-id="276cd-140">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="276cd-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="276cd-141">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="276cd-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="276cd-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="276cd-142">ReadOnly</span></span>
- <span data-ttu-id="276cd-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="276cd-143">ReadWrite</span></span>
- <span data-ttu-id="276cd-144">Brak Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="276cd-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="276cd-145">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="276cd-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="276cd-146">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="276cd-146">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-147">— CreateOption</span><span class="sxs-lookup"><span data-stu-id="276cd-147">-CreateOption</span></span>
<span data-ttu-id="276cd-148">Określa, czy to polecenie cmdlet tworzy dysk na komputerze wirtualnym z platformy lub obrazu użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="276cd-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="276cd-149">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="276cd-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="276cd-150">Dołączanie.</span><span class="sxs-lookup"><span data-stu-id="276cd-150">Attach.</span></span>
<span data-ttu-id="276cd-151">Określ tę opcję, aby utworzyć maszynę wirtualną na dysku specjalistycznym.</span><span class="sxs-lookup"><span data-stu-id="276cd-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="276cd-152">Po określeniu tej opcji nie należy określać *parametru SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="276cd-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="276cd-153">*VhdUri* to wszystko, co jest potrzebne, aby poinformować platformę Azure o lokalizacji wirtualnego dysku twardego (VHD) w celu dołączenia go jako dysku danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="276cd-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="276cd-154">Puste.</span><span class="sxs-lookup"><span data-stu-id="276cd-154">Empty.</span></span>
<span data-ttu-id="276cd-155">Określ tę wartość, aby utworzyć pusty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="276cd-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="276cd-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="276cd-156">FromImage.</span></span>
<span data-ttu-id="276cd-157">Określ tę opcję, aby utworzyć maszynę wirtualną na dysku lub obrazie ogólnym.</span><span class="sxs-lookup"><span data-stu-id="276cd-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="276cd-158">Podczas określania tej opcji musisz określić parametr *SourceImageUri,* aby wskazać platformie Azure lokalizację pliku VHD do dołączenia jako dysku danych.</span><span class="sxs-lookup"><span data-stu-id="276cd-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="276cd-159">Parametr *VhdUri* jest używany jako lokalizacja identyfikująca miejsce przechowywania dysku danych VHD, gdy będzie używany przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="276cd-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276cd-160">-DefaultProfile</span></span>
<span data-ttu-id="276cd-161">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="276cd-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="276cd-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="276cd-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="276cd-163">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanych przez klienta.</span><span class="sxs-lookup"><span data-stu-id="276cd-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="276cd-164">Tę wartość można określić tylko dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="276cd-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="276cd-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="276cd-165">-DiskSizeInGB</span></span>
<span data-ttu-id="276cd-166">Określa w gigabajtach rozmiar pustego dysku do dołączenia do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="276cd-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-167">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="276cd-167">-Lun</span></span>
<span data-ttu-id="276cd-168">Określa numer jednostki logicznej (OWĄ) dla dysku danych.</span><span class="sxs-lookup"><span data-stu-id="276cd-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-169">-Managed Jednakid</span><span class="sxs-lookup"><span data-stu-id="276cd-169">-ManagedDiskId</span></span>
<span data-ttu-id="276cd-170">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="276cd-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-171">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="276cd-171">-Name</span></span>
<span data-ttu-id="276cd-172">Określa nazwę dysku danych do dodania.</span><span class="sxs-lookup"><span data-stu-id="276cd-172">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="276cd-173">-SourceImageUri</span></span>
<span data-ttu-id="276cd-174">Określa źródłowy URI dysku, który jest dołączany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="276cd-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="276cd-175">-StorageAccountType</span></span>
<span data-ttu-id="276cd-176">Określa typ konta magazynu zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="276cd-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-177">- VhdUri</span><span class="sxs-lookup"><span data-stu-id="276cd-177">-VhdUri</span></span>
<span data-ttu-id="276cd-178">Określa identyfikator URI dla pliku wirtualnego dysku twardego (VHD) do utworzenia w przypadku użycia obrazu platformy lub obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="276cd-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="276cd-179">To polecenie cmdlet kopiuje do tej lokalizacji duży obiekt (blob) obrazu.</span><span class="sxs-lookup"><span data-stu-id="276cd-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="276cd-180">Jest to lokalizacja, z której należy uruchomić maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="276cd-180">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-181">- MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="276cd-181">-VM</span></span>
<span data-ttu-id="276cd-182">Określa lokalny obiekt maszyny wirtualnej, do którego ma być dodać dysk danych.</span><span class="sxs-lookup"><span data-stu-id="276cd-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="276cd-183">Aby uzyskać obiekt maszyny wirtualnej, możesz użyć polecenia cmdlet **Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="276cd-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="276cd-184">Aby utworzyć obiekt maszyny wirtualnej, możesz użyć polecenia cmdlet **New-AzVMConfig.**</span><span class="sxs-lookup"><span data-stu-id="276cd-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-185">- WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="276cd-185">-WriteAccelerator</span></span>
<span data-ttu-id="276cd-186">Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na zarządzanym dysku danych.</span><span class="sxs-lookup"><span data-stu-id="276cd-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="276cd-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276cd-187">CommonParameters</span></span>
<span data-ttu-id="276cd-188">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="276cd-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276cd-189">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="276cd-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276cd-190">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="276cd-190">INPUTS</span></span>

### <span data-ttu-id="276cd-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="276cd-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="276cd-192">System.String</span><span class="sxs-lookup"><span data-stu-id="276cd-192">System.String</span></span>

### <span data-ttu-id="276cd-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="276cd-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="276cd-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="276cd-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="276cd-195">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="276cd-195">OUTPUTS</span></span>

### <span data-ttu-id="276cd-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="276cd-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="276cd-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="276cd-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="276cd-198">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="276cd-198">NOTES</span></span>

## <span data-ttu-id="276cd-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="276cd-199">RELATED LINKS</span></span>

[<span data-ttu-id="276cd-200">Remove-AzVMDataData</span><span class="sxs-lookup"><span data-stu-id="276cd-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="276cd-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="276cd-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="276cd-202">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="276cd-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
