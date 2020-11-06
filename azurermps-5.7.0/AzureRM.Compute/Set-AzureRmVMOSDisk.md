---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: dfcd408e3afa7988b06a1e020d76844c48d990b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526917"
---
# <span data-ttu-id="e514b-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="e514b-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="e514b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e514b-102">SYNOPSIS</span></span>
<span data-ttu-id="e514b-103">Ustawia właściwości dysku systemu operacyjnego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e514b-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e514b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e514b-104">SYNTAX</span></span>

### <span data-ttu-id="e514b-105">DefaultParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e514b-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes>
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="e514b-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="e514b-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="e514b-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e514b-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

### <span data-ttu-id="e514b-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="e514b-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="e514b-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e514b-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

## <span data-ttu-id="e514b-110">Opis</span><span class="sxs-lookup"><span data-stu-id="e514b-110">DESCRIPTION</span></span>
<span data-ttu-id="e514b-111">Polecenie cmdlet **Set-AzureRmVMOSDisk** ustawia właściwości dysku systemu operacyjnego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e514b-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="e514b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e514b-112">EXAMPLES</span></span>

### <span data-ttu-id="e514b-113">Przykład 1: Ustawianie właściwości na maszynie wirtualnej na podstawie obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="e514b-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="e514b-114">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet13 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e514b-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e514b-115">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e514b-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e514b-116">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e514b-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e514b-117">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e514b-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e514b-118">Polecenie ostatnie ustawia właściwości na maszynie wirtualnej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e514b-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="e514b-119">Przykład 2: ustawia właściwości na maszynie wirtualnej z ogólnego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="e514b-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="e514b-120">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet13 w grupie zasobów o nazwie ResourceGroup11 i zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e514b-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e514b-121">Drugie polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e514b-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e514b-122">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e514b-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e514b-123">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e514b-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e514b-124">Polecenie ostatnie ustawia właściwości na maszynie wirtualnej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e514b-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="e514b-125">Przykład 3: Ustawianie właściwości na maszynie wirtualnej z obrazu specjalistycznego użytkownika</span><span class="sxs-lookup"><span data-stu-id="e514b-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="e514b-126">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet13 w grupie zasobów o nazwie ResourceGroup11 i zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e514b-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e514b-127">Drugie polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e514b-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e514b-128">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e514b-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e514b-129">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e514b-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e514b-130">Polecenie ostatnie ustawia właściwości na maszynie wirtualnej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e514b-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="e514b-131">Przykład 4: Ustawianie ustawień szyfrowania dysków na dysku z systemem operacyjnym maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e514b-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="e514b-132">W tym przykładzie są ustawiane ustawienia szyfrowania dysków na dysku z systemem operacyjnym maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e514b-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="e514b-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e514b-133">PARAMETERS</span></span>

### <span data-ttu-id="e514b-134">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="e514b-134">-Caching</span></span>
<span data-ttu-id="e514b-135">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e514b-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="e514b-136">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e514b-136">Valid values are:</span></span> 

- <span data-ttu-id="e514b-137">Odczytu</span><span class="sxs-lookup"><span data-stu-id="e514b-137">ReadOnly</span></span>
- <span data-ttu-id="e514b-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e514b-138">ReadWrite</span></span>

<span data-ttu-id="e514b-139">Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="e514b-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="e514b-140">Zmiana wartości w pamięci podręcznej powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e514b-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="e514b-141">To ustawienie wpływa na wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="e514b-141">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="e514b-142">-Opcja</span><span class="sxs-lookup"><span data-stu-id="e514b-142">-CreateOption</span></span>
<span data-ttu-id="e514b-143">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika albo dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="e514b-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="e514b-144">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e514b-144">Valid values are:</span></span> 

- <span data-ttu-id="e514b-145">Ponowne.</span><span class="sxs-lookup"><span data-stu-id="e514b-145">Attach.</span></span>
<span data-ttu-id="e514b-146">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie specjalistycznego dysku.</span><span class="sxs-lookup"><span data-stu-id="e514b-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="e514b-147">Po określeniu tej opcji nie określaj parametru *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="e514b-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="e514b-148">Zamiast tego użyj polecenia cmdlet Set-AzureRmVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="e514b-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="e514b-149">Należy również użyć parametrów *systemu Windows* lub *Linux* , aby poinformować platformę azure2 o typie systemu operacyjnego na dysku VHD.</span><span class="sxs-lookup"><span data-stu-id="e514b-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="e514b-150">Parametr *VhdUri* jest wystarczający, aby poinformować platformę azure2 o lokalizacji dysku do dołączenia.</span><span class="sxs-lookup"><span data-stu-id="e514b-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="e514b-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="e514b-151">FromImage.</span></span>
<span data-ttu-id="e514b-152">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie obrazu platformy lub uogólnionego obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e514b-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="e514b-153">W przypadku ogólnego obrazu użytkownika należy również określić parametr *SourceImageUri* , a także parametry *systemu Windows* lub *Linux* , aby poinformować platformę Azure o lokalizacji i typie wirtualnego dysku twardego systemu operacyjnego zamiast użyciu polecenia cmdlet **Set-AzureRmVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="e514b-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="e514b-154">W przypadku obrazu platformy parametr *VhdUri* jest wystarczający.</span><span class="sxs-lookup"><span data-stu-id="e514b-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="e514b-155">Wolnego.</span><span class="sxs-lookup"><span data-stu-id="e514b-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-156">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e514b-156">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="e514b-157">Określa lokalizację klucza szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e514b-157">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-158">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e514b-158">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="e514b-159">Określa identyfikator zasobu magazynu kluczy zawierającego klucz szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e514b-159">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-160">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e514b-160">-DiskSizeInGB</span></span>
<span data-ttu-id="e514b-161">Określa rozmiar dysku systemu operacyjnego (w GB).</span><span class="sxs-lookup"><span data-stu-id="e514b-161">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-162">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e514b-162">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e514b-163">Określa lokalizację klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="e514b-163">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-164">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e514b-164">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="e514b-165">Określa identyfikator zasobu magazynu kluczy zawierającego klucz szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="e514b-165">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="e514b-166">-Linux</span></span>
<span data-ttu-id="e514b-167">Wskazuje, że system operacyjny na obrazie użytkownika to Linux.</span><span class="sxs-lookup"><span data-stu-id="e514b-167">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="e514b-168">Określ ten parametr dla wdrożenia maszyny wirtualnej opartej na obrazie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e514b-168">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e514b-169">-ManagedDiskId</span></span>
<span data-ttu-id="e514b-170">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e514b-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-171">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e514b-171">-Name</span></span>
<span data-ttu-id="e514b-172">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e514b-172">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="e514b-173">-SourceImageUri</span></span>
<span data-ttu-id="e514b-174">Określa identyfikator URI wirtualnego dysku twardego dla scenariuszy obrazów użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e514b-174">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e514b-175">-StorageAccountType</span></span>
<span data-ttu-id="e514b-176">Określa typ konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e514b-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="e514b-177">-VhdUri</span></span>
<span data-ttu-id="e514b-178">Określa identyfikator URI (Uniform Resource Identifier) wirtualnego dysku twardego (VHD).</span><span class="sxs-lookup"><span data-stu-id="e514b-178">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="e514b-179">W przypadku maszyny wirtualnej opartej na obrazie ten parametr określa plik VHD, który ma zostać utworzony po określeniu obrazu platformy lub obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e514b-179">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="e514b-180">Jest to lokalizacja, z której jest kopiowany duży obiekt (obiekt BLOB) obrazu w celu uruchomienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e514b-180">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="e514b-181">W przypadku scenariusza rozruchu maszyny wirtualnej opartej na dysku ten parametr określa plik VHD, którego maszyna wirtualna używa bezpośrednio do uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="e514b-181">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-182">-VM</span><span class="sxs-lookup"><span data-stu-id="e514b-182">-VM</span></span>
<span data-ttu-id="e514b-183">Określa lokalny obiekt maszyny wirtualnej, na którym należy ustawić właściwości dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e514b-183">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="e514b-184">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="e514b-184">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="e514b-185">-Windows</span><span class="sxs-lookup"><span data-stu-id="e514b-185">-Windows</span></span>
<span data-ttu-id="e514b-186">Wskazuje, że system operacyjny obrazu użytkownika jest w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="e514b-186">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e514b-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e514b-187">CommonParameters</span></span>
<span data-ttu-id="e514b-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e514b-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e514b-189">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e514b-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e514b-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e514b-190">INPUTS</span></span>

### <span data-ttu-id="e514b-191">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e514b-191">None</span></span>
<span data-ttu-id="e514b-192">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e514b-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e514b-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e514b-193">OUTPUTS</span></span>

## <span data-ttu-id="e514b-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e514b-194">NOTES</span></span>

## <span data-ttu-id="e514b-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e514b-195">RELATED LINKS</span></span>

[<span data-ttu-id="e514b-196">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e514b-196">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e514b-197">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e514b-197">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="e514b-198">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="e514b-198">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


