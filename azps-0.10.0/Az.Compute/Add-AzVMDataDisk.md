---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 4c7e59b847ec1ae1d95c5a884c8979d12d193084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891638"
---
# <span data-ttu-id="7999d-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7999d-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="7999d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7999d-102">SYNOPSIS</span></span>
<span data-ttu-id="7999d-103">Dodaje dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="7999d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7999d-104">SYNTAX</span></span>

```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7999d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7999d-105">DESCRIPTION</span></span>
<span data-ttu-id="7999d-106">Polecenie cmdlet **Add-AzVMDataDisk** dodaje dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-106">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="7999d-107">Dysk danych można dodać podczas tworzenia maszyny wirtualnej lub można dodać dysk z danymi do istniejącej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="7999d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7999d-108">EXAMPLES</span></span>

### <span data-ttu-id="7999d-109">Przykład 1: Dodawanie dysków z danymi do nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7999d-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="7999d-110">Pierwsze polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7999d-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7999d-111">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="7999d-112">Kolejne trzy polecenia przypisują ścieżki trzech dysków z danymi do $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03 zmiennych.</span><span class="sxs-lookup"><span data-stu-id="7999d-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="7999d-113">Taka metoda dotyczy tylko czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="7999d-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="7999d-114">Trzy ostatnie polecenia każdy z nich dodaje dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7999d-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7999d-115">Polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="7999d-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="7999d-116">Identyfikator URI każdego dysku jest przechowywany w $DataDiskVhdUri 01, $DataDiskVhdUri 02 i $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="7999d-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="7999d-117">Przykład 2: Dodawanie dysku danych do istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="7999d-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="7999d-118">Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie VirtualMachine07 przy użyciu polecenia cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="7999d-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="7999d-119">Polecenie zapisuje maszynę wirtualną w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7999d-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7999d-120">Drugie polecenie dodaje dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7999d-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="7999d-121">Polecenie ostatnie umożliwia zaktualizowanie stanu maszyny wirtualnej przechowywanej w $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7999d-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="7999d-122">Przykład 3: Dodawanie dysku danych do nowej maszyny wirtualnej z ogólnego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="7999d-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="7999d-123">Pierwsze polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7999d-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7999d-124">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="7999d-125">Następne dwa polecenia umożliwiają przypisanie ścieżek do obrazów danych i dysków z danymi odpowiednio do $DataImageUri i $DataDiskUri zmiennych.</span><span class="sxs-lookup"><span data-stu-id="7999d-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="7999d-126">Ta metoda jest używana w celu poprawienia czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="7999d-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="7999d-127">Ostatnie polecenia dodają dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7999d-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7999d-128">Polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="7999d-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="7999d-129">Przykład 4: Dodawanie dysków z danymi do nowej maszyny wirtualnej z obrazu specjalistycznego użytkownika</span><span class="sxs-lookup"><span data-stu-id="7999d-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="7999d-130">Pierwsze polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7999d-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7999d-131">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="7999d-132">Następne polecenia przypisują ścieżki do $DataDiskUri zmiennej.</span><span class="sxs-lookup"><span data-stu-id="7999d-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="7999d-133">Ta metoda jest używana w celu poprawienia czytelności następujących poleceń.</span><span class="sxs-lookup"><span data-stu-id="7999d-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="7999d-134">Polecenie ostatnie Dodaj dysk danych do maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7999d-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7999d-135">Polecenie określa nazwę i lokalizację dysku oraz inne właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="7999d-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="7999d-136">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7999d-136">PARAMETERS</span></span>

### <span data-ttu-id="7999d-137">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="7999d-137">-Caching</span></span>
<span data-ttu-id="7999d-138">Określa tryb buforowania dysku.</span><span class="sxs-lookup"><span data-stu-id="7999d-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="7999d-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7999d-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7999d-140">Odczytu</span><span class="sxs-lookup"><span data-stu-id="7999d-140">ReadOnly</span></span>
- <span data-ttu-id="7999d-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7999d-141">ReadWrite</span></span>
- <span data-ttu-id="7999d-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7999d-142">None</span></span>

<span data-ttu-id="7999d-143">Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="7999d-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="7999d-144">Zmiana tej wartości powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="7999d-145">To ustawienie wpływa na spójność i wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="7999d-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-146">-Opcja</span><span class="sxs-lookup"><span data-stu-id="7999d-146">-CreateOption</span></span>
<span data-ttu-id="7999d-147">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika, tworzy pusty dysk lub dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="7999d-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="7999d-148">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7999d-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7999d-149">Ponowne.</span><span class="sxs-lookup"><span data-stu-id="7999d-149">Attach.</span></span>
<span data-ttu-id="7999d-150">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie specjalistycznego dysku.</span><span class="sxs-lookup"><span data-stu-id="7999d-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="7999d-151">Po określeniu tej opcji nie określaj parametru *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="7999d-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="7999d-152">*VhdUri* to wszystko, co jest potrzebne, aby poinformować platformę Azure o lokalizacji wirtualnego dysku twardego (VHD), który ma zostać dołączony jako dysk danych do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="7999d-153">Wolnego.</span><span class="sxs-lookup"><span data-stu-id="7999d-153">Empty.</span></span>
<span data-ttu-id="7999d-154">Określ, czy chcesz utworzyć pusty dysk danych.</span><span class="sxs-lookup"><span data-stu-id="7999d-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="7999d-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="7999d-155">FromImage.</span></span>
<span data-ttu-id="7999d-156">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie uogólnionego obrazu lub dysku.</span><span class="sxs-lookup"><span data-stu-id="7999d-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="7999d-157">Po określeniu tej opcji należy określić również parametr *SourceImageUri* , aby wskazać platformę Azure lokalizację dysku VHD, który ma zostać dołączony jako dysk danych.</span><span class="sxs-lookup"><span data-stu-id="7999d-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="7999d-158">Parametr *VhdUri* jest wykorzystywany jako lokalizacja identyfikująca lokalizację, w której dysk VHD z danymi będzie przechowywany, gdy jest on wykorzystywany przez maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="7999d-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7999d-159">-DefaultProfile</span></span>
<span data-ttu-id="7999d-160">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7999d-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-161">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7999d-161">-DiskSizeInGB</span></span>
<span data-ttu-id="7999d-162">Określa rozmiar, w gigabajtach, pustego dysku, który ma zostać dołączony do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-162">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-163">-LUN</span><span class="sxs-lookup"><span data-stu-id="7999d-163">-Lun</span></span>
<span data-ttu-id="7999d-164">Określa logiczny numer jednostki (LUN) dla dysku danych.</span><span class="sxs-lookup"><span data-stu-id="7999d-164">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-165">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="7999d-165">-ManagedDiskId</span></span>
<span data-ttu-id="7999d-166">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="7999d-166">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-167">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7999d-167">-Name</span></span>
<span data-ttu-id="7999d-168">Określa nazwę dysku danych, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="7999d-168">Specifies the name of the data disk to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-169">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="7999d-169">-SourceImageUri</span></span>
<span data-ttu-id="7999d-170">Określa źródłowy identyfikator URI dysku, który jest dołączony do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7999d-170">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-171">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7999d-171">-StorageAccountType</span></span>
<span data-ttu-id="7999d-172">Określa typ konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="7999d-172">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-173">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="7999d-173">-VhdUri</span></span>
<span data-ttu-id="7999d-174">Określa identyfikator URI (Uniform Resource Identifier) pliku wirtualnego dysku twardego (VHD), który ma zostać utworzony po użyciu obrazu platformy lub obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7999d-174">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="7999d-175">To polecenie cmdlet umożliwia skopiowanie do tej lokalizacji dużego obiektu (BLOB) w formacie binarnym.</span><span class="sxs-lookup"><span data-stu-id="7999d-175">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="7999d-176">To jest lokalizacja, z której ma zostać uruchomiona maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="7999d-176">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-177">-VM</span><span class="sxs-lookup"><span data-stu-id="7999d-177">-VM</span></span>
<span data-ttu-id="7999d-178">Określa lokalny obiekt maszyny wirtualnej, do którego ma zostać dodany dysk danych.</span><span class="sxs-lookup"><span data-stu-id="7999d-178">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="7999d-179">Aby uzyskać obiekt maszyny wirtualnej, można użyć polecenia cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="7999d-179">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="7999d-180">Za pomocą polecenia cmdlet **New-AzVMConfig** można utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7999d-180">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-181">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7999d-181">-WriteAccelerator</span></span>
<span data-ttu-id="7999d-182">Określa, czy WriteAccelerator ma być włączony, czy wyłączony na dysku z danymi.</span><span class="sxs-lookup"><span data-stu-id="7999d-182">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7999d-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7999d-183">CommonParameters</span></span>
<span data-ttu-id="7999d-184">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7999d-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7999d-185">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7999d-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7999d-186">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7999d-186">INPUTS</span></span>

### <span data-ttu-id="7999d-187">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7999d-187">PSVirtualMachine</span></span>
<span data-ttu-id="7999d-188">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="7999d-188">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="7999d-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7999d-189">OUTPUTS</span></span>

### <span data-ttu-id="7999d-190">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7999d-190">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7999d-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7999d-191">NOTES</span></span>

## <span data-ttu-id="7999d-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7999d-192">RELATED LINKS</span></span>

[<span data-ttu-id="7999d-193">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7999d-193">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="7999d-194">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7999d-194">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7999d-195">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7999d-195">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
