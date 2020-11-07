---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 79d8852fb3827e7856610d79ea7fb5f0a17543c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706486"
---
# <span data-ttu-id="2447f-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2447f-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="2447f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2447f-102">SYNOPSIS</span></span>
<span data-ttu-id="2447f-103">Dodaje dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="2447f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2447f-104">SYNTAX</span></span>

### <span data-ttu-id="2447f-105">VmNormalDiskParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2447f-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2447f-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2447f-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2447f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2447f-107">DESCRIPTION</span></span>
<span data-ttu-id="2447f-108">Polecenie cmdlet **Add-AzVMDataDisk** dodaje dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="2447f-109">Dysk danych można dodać podczas tworzenia maszyny wirtualnej lub można dodać dysk z danymi do istniejącej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="2447f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2447f-110">EXAMPLES</span></span>

### <span data-ttu-id="2447f-111">Przykład 1: Dodawanie dysków z danymi do nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2447f-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="2447f-112">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2447f-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2447f-113">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2447f-114">Kolejne trzy polecenia przypisują ścieżki trzech dysków z danymi do $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="2447f-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="2447f-115">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="2447f-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="2447f-116">Trzy ostatnie polecenia każdy z nich dodaje dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2447f-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="2447f-117">Polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="2447f-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="2447f-118">Identyfikator URI każdego dysku jest przechowywany w $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="2447f-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="2447f-119">Przykład 2: Dodawanie dysku danych do istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2447f-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="2447f-120">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="2447f-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="2447f-121">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2447f-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2447f-122">Drugie polecenie dodaje dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2447f-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="2447f-123">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2447f-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="2447f-124">Przykład 3: Dodawanie dysku danych do nowej maszyny wirtualnej z ogólnego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="2447f-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="2447f-125">Pierwsze polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2447f-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2447f-126">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2447f-127">Następne dwa polecenia umożliwiają przypisanie ścieżek do obrazów danych i dysków z danymi odpowiednio do $DataImageUri i $DataDiskUri zmiennych.</span><span class="sxs-lookup"><span data-stu-id="2447f-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="2447f-128">Ta metoda jest używana w celu poprawienia czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="2447f-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="2447f-129">Ostatnie polecenia dodają dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2447f-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="2447f-130">Polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="2447f-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="2447f-131">Przykład 4: Dodawanie dysków z danymi do nowej maszyny wirtualnej z obrazu specjalistycznego użytkownika</span><span class="sxs-lookup"><span data-stu-id="2447f-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="2447f-132">Pierwsze polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2447f-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2447f-133">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2447f-134">Następne polecenia przypisują ścieżki do $DataDiskUri zmiennej.</span><span class="sxs-lookup"><span data-stu-id="2447f-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="2447f-135">Ta metoda jest używana w celu poprawienia czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="2447f-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="2447f-136">Polecenie ostatnie Dodaj dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2447f-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="2447f-137">Polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="2447f-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="2447f-138">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2447f-138">PARAMETERS</span></span>

### <span data-ttu-id="2447f-139">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="2447f-139">-Caching</span></span>
<span data-ttu-id="2447f-140">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="2447f-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="2447f-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2447f-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2447f-142">Odczytu</span><span class="sxs-lookup"><span data-stu-id="2447f-142">ReadOnly</span></span>
- <span data-ttu-id="2447f-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2447f-143">ReadWrite</span></span>
- <span data-ttu-id="2447f-144">Żadna wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2447f-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="2447f-145">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="2447f-146">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="2447f-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="2447f-147">-Opcja</span><span class="sxs-lookup"><span data-stu-id="2447f-147">-CreateOption</span></span>
<span data-ttu-id="2447f-148">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="2447f-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="2447f-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2447f-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2447f-150">Ponowne.</span><span class="sxs-lookup"><span data-stu-id="2447f-150">Attach.</span></span>
<span data-ttu-id="2447f-151">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie specjalistycznego dysku.</span><span class="sxs-lookup"><span data-stu-id="2447f-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="2447f-152">Po określeniu tej opcji nie określaj parametru *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="2447f-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="2447f-153">*VhdUri* to wszystko, co jest potrzebne, aby poinformować platformę Azure o lokalizacji wirtualnego dysku twardego (VHD), który ma zostać dołączony jako dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="2447f-154">Wolnego.</span><span class="sxs-lookup"><span data-stu-id="2447f-154">Empty.</span></span>
<span data-ttu-id="2447f-155">Określ, czy chcesz utworzyć pusty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="2447f-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="2447f-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="2447f-156">FromImage.</span></span>
<span data-ttu-id="2447f-157">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie uogólnionego obrazu lub dysku.</span><span class="sxs-lookup"><span data-stu-id="2447f-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="2447f-158">Po określeniu tej opcji należy określić również parametr *SourceImageUri* , aby wskazać platformę Azure lokalizację dysku VHD, który ma zostać dołączony jako dysk danych.</span><span class="sxs-lookup"><span data-stu-id="2447f-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="2447f-159">Parametr *VhdUri* jest wykorzystywany jako lokalizacja identyfikująca lokalizację, w której dysk VHD z danymi będzie przechowywany, gdy jest on wykorzystywany przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="2447f-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="2447f-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2447f-160">-DefaultProfile</span></span>
<span data-ttu-id="2447f-161">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2447f-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2447f-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="2447f-162">-DiskSizeInGB</span></span>
<span data-ttu-id="2447f-163">Określa rozmiar, w gigabajtach, pustego dysku, który ma zostać dołączony do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-163">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="2447f-164">-LUN</span><span class="sxs-lookup"><span data-stu-id="2447f-164">-Lun</span></span>
<span data-ttu-id="2447f-165">Określa logiczny numer jednostki (LUN) dla dysku danych.</span><span class="sxs-lookup"><span data-stu-id="2447f-165">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="2447f-166">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="2447f-166">-ManagedDiskId</span></span>
<span data-ttu-id="2447f-167">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="2447f-167">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="2447f-168">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2447f-168">-Name</span></span>
<span data-ttu-id="2447f-169">Określa nazwę dysku danych, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="2447f-169">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="2447f-170">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="2447f-170">-SourceImageUri</span></span>
<span data-ttu-id="2447f-171">Określa źródłowy identyfikator URI dysku, który jest dołączony do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2447f-171">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="2447f-172">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2447f-172">-StorageAccountType</span></span>
<span data-ttu-id="2447f-173">Określa typ konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="2447f-173">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="2447f-174">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="2447f-174">-VhdUri</span></span>
<span data-ttu-id="2447f-175">Określa identyfikator URI (Uniform Resource Identifier) pliku wirtualnego dysku twardego (VHD), który ma zostać utworzony po użyciu obrazu platformy lub obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2447f-175">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="2447f-176">To polecenie cmdlet umożliwia skopiowanie do tej lokalizacji dużego obiektu (BLOB) w formacie binarnym.</span><span class="sxs-lookup"><span data-stu-id="2447f-176">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="2447f-177">To jest lokalizacja, z której ma zostać uruchomiona maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="2447f-177">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="2447f-178">-VM</span><span class="sxs-lookup"><span data-stu-id="2447f-178">-VM</span></span>
<span data-ttu-id="2447f-179">Określa lokalny obiekt maszyny wirtualnej, do którego ma zostać dodany dysk danych.</span><span class="sxs-lookup"><span data-stu-id="2447f-179">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="2447f-180">Aby uzyskać obiekt maszyny wirtualnej, można użyć polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="2447f-180">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="2447f-181">Za pomocą polecenia cmdlet **New-AzVMConfig** można utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2447f-181">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="2447f-182">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="2447f-182">-WriteAccelerator</span></span>
<span data-ttu-id="2447f-183">Określa, czy WriteAccelerator powinien być włączony, czy wyłączony na zarządzanym dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="2447f-183">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="2447f-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2447f-184">CommonParameters</span></span>
<span data-ttu-id="2447f-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2447f-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2447f-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2447f-186">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2447f-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2447f-187">INPUTS</span></span>

### <span data-ttu-id="2447f-188">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2447f-188">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="2447f-189">System. String</span><span class="sxs-lookup"><span data-stu-id="2447f-189">System.String</span></span>

### <span data-ttu-id="2447f-190">Microsoft. Azure. Management. COMPUTE. MODELES. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="2447f-190">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="2447f-191">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2447f-191">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2447f-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2447f-192">OUTPUTS</span></span>

### <span data-ttu-id="2447f-193">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2447f-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="2447f-194">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2447f-194">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2447f-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2447f-195">NOTES</span></span>

## <span data-ttu-id="2447f-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2447f-196">RELATED LINKS</span></span>

[<span data-ttu-id="2447f-197">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2447f-197">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="2447f-198">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2447f-198">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2447f-199">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2447f-199">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
