---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 6804f0e45746798a1ed890ad52b9b9e103d64533
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706172"
---
# <span data-ttu-id="028fc-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="028fc-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="028fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="028fc-102">SYNOPSIS</span></span>
<span data-ttu-id="028fc-103">Ustawia właściwości dysku systemu operacyjnego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="028fc-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="028fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="028fc-104">SYNTAX</span></span>

### <span data-ttu-id="028fc-105">DefaultParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="028fc-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="028fc-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="028fc-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="028fc-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="028fc-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="028fc-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="028fc-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="028fc-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="028fc-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="028fc-110">Opis</span><span class="sxs-lookup"><span data-stu-id="028fc-110">DESCRIPTION</span></span>
<span data-ttu-id="028fc-111">Polecenie cmdlet **Set-AzVMOSDisk** ustawia właściwości dysku systemu operacyjnego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="028fc-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="028fc-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="028fc-112">EXAMPLES</span></span>

### <span data-ttu-id="028fc-113">Przykład 1: Ustawianie właściwości na maszynie wirtualnej na podstawie obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="028fc-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="028fc-114">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet13 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="028fc-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="028fc-115">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="028fc-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="028fc-116">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="028fc-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="028fc-117">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="028fc-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="028fc-118">Polecenie ostatnie ustawia właściwości na maszynie wirtualnej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="028fc-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="028fc-119">Przykład 2: ustawia właściwości na maszynie wirtualnej z ogólnego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="028fc-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="028fc-120">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet13 w grupie zasobów o nazwie ResourceGroup11 i zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="028fc-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="028fc-121">Drugie polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="028fc-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="028fc-122">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="028fc-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="028fc-123">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="028fc-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="028fc-124">Polecenie ostatnie ustawia właściwości na maszynie wirtualnej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="028fc-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="028fc-125">Przykład 3: Ustawianie właściwości na maszynie wirtualnej z obrazu specjalistycznego użytkownika</span><span class="sxs-lookup"><span data-stu-id="028fc-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="028fc-126">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet13 w grupie zasobów o nazwie ResourceGroup11 i zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="028fc-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="028fc-127">Drugie polecenie tworzy obiekt maszyny wirtualnej i zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="028fc-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="028fc-128">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="028fc-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="028fc-129">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="028fc-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="028fc-130">Polecenie ostatnie ustawia właściwości na maszynie wirtualnej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="028fc-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="028fc-131">Przykład 4: Ustawianie ustawień szyfrowania dysków na dysku z systemem operacyjnym maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="028fc-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="028fc-132">W tym przykładzie są ustawiane ustawienia szyfrowania dysków na dysku z systemem operacyjnym maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="028fc-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="028fc-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="028fc-133">PARAMETERS</span></span>

### <span data-ttu-id="028fc-134">-Buforowanie</span><span class="sxs-lookup"><span data-stu-id="028fc-134">-Caching</span></span>
<span data-ttu-id="028fc-135">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="028fc-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="028fc-136">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="028fc-136">Valid values are:</span></span> 
- <span data-ttu-id="028fc-137">Odczytu</span><span class="sxs-lookup"><span data-stu-id="028fc-137">ReadOnly</span></span>
- <span data-ttu-id="028fc-138">ReadWrite wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="028fc-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="028fc-139">Zmiana wartości w pamięci podręcznej powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="028fc-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="028fc-140">To ustawienie wpływa na wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="028fc-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-141">-Opcja</span><span class="sxs-lookup"><span data-stu-id="028fc-141">-CreateOption</span></span>
<span data-ttu-id="028fc-142">Określa, czy to polecenie cmdlet tworzy dysk na maszynie wirtualnej na platformie lub obrazie użytkownika albo dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="028fc-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="028fc-143">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="028fc-143">Valid values are:</span></span> 
- <span data-ttu-id="028fc-144">Ponowne.</span><span class="sxs-lookup"><span data-stu-id="028fc-144">Attach.</span></span>
<span data-ttu-id="028fc-145">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie specjalistycznego dysku.</span><span class="sxs-lookup"><span data-stu-id="028fc-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="028fc-146">Po określeniu tej opcji nie określaj parametru *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="028fc-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="028fc-147">Zamiast tego użyj polecenia cmdlet Set-AzVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="028fc-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="028fc-148">Należy również użyć parametrów *systemu Windows* lub *Linux* , aby poinformować platformę Azure o typie systemu operacyjnego na dysku VHD.</span><span class="sxs-lookup"><span data-stu-id="028fc-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="028fc-149">Parametr *VhdUri* jest wystarczający, aby poinformować platformę Azure o lokalizacji dysku do dołączenia.</span><span class="sxs-lookup"><span data-stu-id="028fc-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="028fc-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="028fc-150">FromImage.</span></span>
<span data-ttu-id="028fc-151">Wybierz tę opcję, aby utworzyć maszynę wirtualną na podstawie obrazu platformy lub uogólnionego obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="028fc-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="028fc-152">W przypadku ogólnego obrazu użytkownika należy również określić parametr *SourceImageUri* , a także parametry *systemu Windows* lub *Linux* , aby poinformować platformę Azure o lokalizacji i typie wirtualnego dysku twardego systemu operacyjnego zamiast użyciu polecenia cmdlet **Set-AzVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="028fc-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="028fc-153">W przypadku obrazu platformy parametr *VhdUri* jest wystarczający.</span><span class="sxs-lookup"><span data-stu-id="028fc-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="028fc-154">Wolnego.</span><span class="sxs-lookup"><span data-stu-id="028fc-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028fc-155">-DefaultProfile</span></span>
<span data-ttu-id="028fc-156">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="028fc-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="028fc-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="028fc-157">-DiffDiskSetting</span></span>
<span data-ttu-id="028fc-158">Określa ustawienia dysku różnicowego dla dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="028fc-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="028fc-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="028fc-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="028fc-160">Określa lokalizację klucza szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="028fc-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="028fc-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="028fc-162">Określa identyfikator zasobu magazynu kluczy zawierającego klucz szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="028fc-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-163">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="028fc-163">-DiskSizeInGB</span></span>
<span data-ttu-id="028fc-164">Określa rozmiar dysku systemu operacyjnego (w GB).</span><span class="sxs-lookup"><span data-stu-id="028fc-164">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-165">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="028fc-165">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="028fc-166">Określa lokalizację klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="028fc-166">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-167">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="028fc-167">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="028fc-168">Określa identyfikator zasobu magazynu kluczy zawierającego klucz szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="028fc-168">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-169">-Linux</span><span class="sxs-lookup"><span data-stu-id="028fc-169">-Linux</span></span>
<span data-ttu-id="028fc-170">Wskazuje, że system operacyjny na obrazie użytkownika to Linux.</span><span class="sxs-lookup"><span data-stu-id="028fc-170">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="028fc-171">Określ ten parametr dla wdrożenia maszyny wirtualnej opartej na obrazie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="028fc-171">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="028fc-172">-ManagedDiskId</span></span>
<span data-ttu-id="028fc-173">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="028fc-173">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="028fc-174">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="028fc-174">-Name</span></span>
<span data-ttu-id="028fc-175">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="028fc-175">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="028fc-176">-SourceImageUri</span></span>
<span data-ttu-id="028fc-177">Określa identyfikator URI wirtualnego dysku twardego dla scenariuszy obrazów użytkownika.</span><span class="sxs-lookup"><span data-stu-id="028fc-177">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="028fc-178">-StorageAccountType</span></span>
<span data-ttu-id="028fc-179">Określa typ konta magazynu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="028fc-179">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="028fc-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="028fc-180">-VhdUri</span></span>
<span data-ttu-id="028fc-181">Określa identyfikator URI (Uniform Resource Identifier) wirtualnego dysku twardego (VHD).</span><span class="sxs-lookup"><span data-stu-id="028fc-181">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="028fc-182">W przypadku maszyny wirtualnej opartej na obrazie ten parametr określa plik VHD, który ma zostać utworzony po określeniu obrazu platformy lub obrazu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="028fc-182">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="028fc-183">Jest to lokalizacja, z której jest kopiowany duży obiekt (obiekt BLOB) obrazu w celu uruchomienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="028fc-183">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="028fc-184">W przypadku scenariusza rozruchu maszyny wirtualnej opartej na dysku ten parametr określa plik VHD, którego maszyna wirtualna używa bezpośrednio do uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="028fc-184">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-185">-VM</span><span class="sxs-lookup"><span data-stu-id="028fc-185">-VM</span></span>
<span data-ttu-id="028fc-186">Określa lokalny obiekt maszyny wirtualnej, na którym należy ustawić właściwości dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="028fc-186">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="028fc-187">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="028fc-187">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-188">-Windows</span><span class="sxs-lookup"><span data-stu-id="028fc-188">-Windows</span></span>
<span data-ttu-id="028fc-189">Wskazuje, że system operacyjny obrazu użytkownika jest w systemie Windows.</span><span class="sxs-lookup"><span data-stu-id="028fc-189">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028fc-190">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="028fc-190">-WriteAccelerator</span></span>
<span data-ttu-id="028fc-191">Określa, czy WriteAccelerator należy włączyć lub wyłączyć na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="028fc-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="028fc-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028fc-192">CommonParameters</span></span>
<span data-ttu-id="028fc-193">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="028fc-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028fc-194">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="028fc-194">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028fc-195">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="028fc-195">INPUTS</span></span>

### <span data-ttu-id="028fc-196">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="028fc-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="028fc-197">System. String</span><span class="sxs-lookup"><span data-stu-id="028fc-197">System.String</span></span>

## <span data-ttu-id="028fc-198">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="028fc-198">OUTPUTS</span></span>

### <span data-ttu-id="028fc-199">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="028fc-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="028fc-200">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="028fc-200">NOTES</span></span>

## <span data-ttu-id="028fc-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="028fc-201">RELATED LINKS</span></span>

[<span data-ttu-id="028fc-202">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="028fc-202">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="028fc-203">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="028fc-203">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="028fc-204">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="028fc-204">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


