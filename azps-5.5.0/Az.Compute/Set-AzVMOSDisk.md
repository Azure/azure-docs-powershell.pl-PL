---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238649"
---
# <span data-ttu-id="e690d-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="e690d-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="e690d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e690d-102">SYNOPSIS</span></span>
<span data-ttu-id="e690d-103">Ustawia właściwości dysku systemu operacyjnego na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="e690d-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="e690d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e690d-104">SYNTAX</span></span>

### <span data-ttu-id="e690d-105">DefaultParamSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e690d-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e690d-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="e690d-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e690d-107">WindowsMeterEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e690d-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e690d-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="e690d-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e690d-109">LinuxMeterEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e690d-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e690d-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="e690d-110">DESCRIPTION</span></span>
<span data-ttu-id="e690d-111">Polecenie **cmdlet Set-AzVMOSCmdlet** ustawia właściwości dysku systemu operacyjnego na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="e690d-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="e690d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e690d-112">EXAMPLES</span></span>

### <span data-ttu-id="e690d-113">Przykład 1. Ustawianie właściwości na maszyny wirtualnej z obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="e690d-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="e690d-114">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet13 w grupie zasobów o nazwie Grupa Zasobów11, a następnie przechowuje ten obiekt w zmiennej $AvailabilitySet zasobów.</span><span class="sxs-lookup"><span data-stu-id="e690d-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e690d-115">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="e690d-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e690d-116">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e690d-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e690d-117">Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e690d-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e690d-118">Ostatnie polecenie ustawia właściwości na komputerze wirtualnym w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e690d-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="e690d-119">Przykład 2. Ustawianie właściwości na komputerze wirtualnym na podstawie ogólnego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="e690d-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="e690d-120">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet13 w grupie zasobów o nazwie Grupa Zasobów11 i przechowuje ten obiekt w zmiennej $AvailabilitySet zasobów.</span><span class="sxs-lookup"><span data-stu-id="e690d-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e690d-121">Drugie polecenie tworzy obiekt maszyny wirtualnej i przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="e690d-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e690d-122">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e690d-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e690d-123">Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e690d-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e690d-124">Ostatnie polecenie ustawia właściwości na komputerze wirtualnym w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e690d-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="e690d-125">Przykład 3. Ustawianie właściwości na maszyny wirtualnej z specjalistycznego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="e690d-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="e690d-126">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet13 w grupie zasobów o nazwie ResourceGroup11 i przechowuje ten obiekt w zmiennej $AvailabilitySet zasobów.</span><span class="sxs-lookup"><span data-stu-id="e690d-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e690d-127">Drugie polecenie tworzy obiekt maszyny wirtualnej i przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="e690d-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e690d-128">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e690d-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e690d-129">Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e690d-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e690d-130">Ostatnie polecenie ustawia właściwości na komputerze wirtualnym w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e690d-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="e690d-131">Przykład 4. Ustawianie ustawień szyfrowania dysku na dysku systemu operacyjnego maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e690d-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="e690d-132">W tym przykładzie są ustawiane ustawienia szyfrowania dysku na dysku systemu operacyjnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e690d-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="e690d-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e690d-133">PARAMETERS</span></span>

### <span data-ttu-id="e690d-134">— buforowanie</span><span class="sxs-lookup"><span data-stu-id="e690d-134">-Caching</span></span>
<span data-ttu-id="e690d-135">Określa tryb buforowania dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e690d-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="e690d-136">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="e690d-136">Valid values are:</span></span> 
- <span data-ttu-id="e690d-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e690d-137">ReadOnly</span></span>
- <span data-ttu-id="e690d-138">ReadWrite Wartość domyślna to ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="e690d-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="e690d-139">Zmiana wartości pamięci buforowania powoduje ponowne uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e690d-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="e690d-140">To ustawienie ma wpływ na wydajność dysku.</span><span class="sxs-lookup"><span data-stu-id="e690d-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="e690d-141">— CreateOption</span><span class="sxs-lookup"><span data-stu-id="e690d-141">-CreateOption</span></span>
<span data-ttu-id="e690d-142">Określa, czy to polecenie cmdlet tworzy dysk na komputerze wirtualnym z platformy lub obrazu użytkownika, czy dołącza istniejący dysk.</span><span class="sxs-lookup"><span data-stu-id="e690d-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="e690d-143">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="e690d-143">Valid values are:</span></span> 
- <span data-ttu-id="e690d-144">Dołącz.</span><span class="sxs-lookup"><span data-stu-id="e690d-144">Attach.</span></span>
<span data-ttu-id="e690d-145">Określ tę opcję, aby utworzyć maszynę wirtualną na dysku specjalistycznym.</span><span class="sxs-lookup"><span data-stu-id="e690d-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="e690d-146">Po określeniu tej opcji nie należy określać *parametru SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="e690d-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="e690d-147">Zamiast tego użyj Set-AzVMSourceImage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e690d-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="e690d-148">Musisz także użyć parametrów systemu *Windows* lub *Linux,* aby określić platformie azure typ systemu operacyjnego na vhd.</span><span class="sxs-lookup"><span data-stu-id="e690d-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="e690d-149">Parametr *VhdUri* wystarczy, aby poinformować platformę azure o lokalizacji dysku do dołączenia.</span><span class="sxs-lookup"><span data-stu-id="e690d-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="e690d-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="e690d-150">FromImage.</span></span>
<span data-ttu-id="e690d-151">Określ tę opcję, aby utworzyć maszynę wirtualną na obrazie platformy lub na ogólnym obrazie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e690d-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="e690d-152">W przypadku ogólnego obrazu użytkownika musisz także określić parametr *SourceImageUri* oraz parametry systemu *Windows* lub *Linux,* aby wskazać platformie Azure lokalizację i typ dysku systemu operacyjnego VHD zamiast polecenia cmdlet **Set-AzVMSourceImage.**</span><span class="sxs-lookup"><span data-stu-id="e690d-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="e690d-153">W przypadku obrazu platformy parametr *VhdUri* jest wystarczający.</span><span class="sxs-lookup"><span data-stu-id="e690d-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="e690d-154">Puste.</span><span class="sxs-lookup"><span data-stu-id="e690d-154">Empty.</span></span>

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

### <span data-ttu-id="e690d-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e690d-155">-DefaultProfile</span></span>
<span data-ttu-id="e690d-156">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e690d-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e690d-157">-Diff Diff DiffSetting</span><span class="sxs-lookup"><span data-stu-id="e690d-157">-DiffDiskSetting</span></span>
<span data-ttu-id="e690d-158">Określa różne ustawienia dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e690d-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="e690d-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e690d-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="e690d-160">Określa lokalizację klucza szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e690d-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="e690d-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e690d-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="e690d-162">Określa identyfikator zasobu magazynu kluczy zawierającego klucz szyfrowania dysku.</span><span class="sxs-lookup"><span data-stu-id="e690d-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="e690d-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e690d-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e690d-164">Określa identyfikator zasobu zestawu szyfrowania dysków zarządzanych przez klienta.</span><span class="sxs-lookup"><span data-stu-id="e690d-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="e690d-165">Tę wartość można określić tylko dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e690d-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="e690d-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e690d-166">-DiskSizeInGB</span></span>
<span data-ttu-id="e690d-167">Określa rozmiar (w GB) dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e690d-167">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="e690d-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e690d-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e690d-169">Określa lokalizację klucza szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="e690d-169">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="e690d-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e690d-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="e690d-171">Określa identyfikator zasobu magazynu kluczy zawierającego klucz szyfrowania klucza.</span><span class="sxs-lookup"><span data-stu-id="e690d-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="e690d-172">— Linux</span><span class="sxs-lookup"><span data-stu-id="e690d-172">-Linux</span></span>
<span data-ttu-id="e690d-173">Oznacza, że system operacyjny na obrazie użytkownika to Linux.</span><span class="sxs-lookup"><span data-stu-id="e690d-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="e690d-174">Określ ten parametr dla wdrożenia maszyn wirtualnych opartych na obrazach użytkowników.</span><span class="sxs-lookup"><span data-stu-id="e690d-174">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="e690d-175">-Managed Jednakid</span><span class="sxs-lookup"><span data-stu-id="e690d-175">-ManagedDiskId</span></span>
<span data-ttu-id="e690d-176">Określa identyfikator dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="e690d-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="e690d-177">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e690d-177">-Name</span></span>
<span data-ttu-id="e690d-178">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e690d-178">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="e690d-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="e690d-179">-SourceImageUri</span></span>
<span data-ttu-id="e690d-180">Określa identyfikator URI VHD dla scenariuszy obrazów użytkowników.</span><span class="sxs-lookup"><span data-stu-id="e690d-180">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="e690d-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e690d-181">-StorageAccountType</span></span>
<span data-ttu-id="e690d-182">Określa typ konta magazynu zarządzanego dysku.</span><span class="sxs-lookup"><span data-stu-id="e690d-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="e690d-183">- VhdUri</span><span class="sxs-lookup"><span data-stu-id="e690d-183">-VhdUri</span></span>
<span data-ttu-id="e690d-184">Określa identyfikator URI wirtualnego dysku twardego (VHD).</span><span class="sxs-lookup"><span data-stu-id="e690d-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="e690d-185">W przypadku maszyny wirtualnej opartej na obrazie ten parametr określa plik VHD do utworzenia, gdy określono obraz platformy lub obraz użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e690d-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="e690d-186">Jest to lokalizacja, z której jest kopiowany duży obiekt binarny (BLOB) w celu uruchomienia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e690d-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="e690d-187">W przypadku scenariusza rozruchu maszyn wirtualnych opartych na dysku ten parametr określa plik VHD, który jest używany przez maszynę wirtualną bezpośrednio do uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="e690d-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="e690d-188">- MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="e690d-188">-VM</span></span>
<span data-ttu-id="e690d-189">Określa obiekt lokalnej maszyny wirtualnej, na którym mają być ustawiane właściwości dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e690d-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="e690d-190">Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e690d-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="e690d-191">— Windows</span><span class="sxs-lookup"><span data-stu-id="e690d-191">-Windows</span></span>
<span data-ttu-id="e690d-192">Oznacza, że system operacyjny na obrazie użytkownika to Windows.</span><span class="sxs-lookup"><span data-stu-id="e690d-192">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="e690d-193">- WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e690d-193">-WriteAccelerator</span></span>
<span data-ttu-id="e690d-194">Określa, czy funkcja WriteAccelerator ma być włączona, czy wyłączona na dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e690d-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="e690d-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e690d-195">CommonParameters</span></span>
<span data-ttu-id="e690d-196">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e690d-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e690d-197">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e690d-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e690d-198">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e690d-198">INPUTS</span></span>

### <span data-ttu-id="e690d-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e690d-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e690d-200">System.String</span><span class="sxs-lookup"><span data-stu-id="e690d-200">System.String</span></span>

## <span data-ttu-id="e690d-201">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e690d-201">OUTPUTS</span></span>

### <span data-ttu-id="e690d-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e690d-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e690d-203">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e690d-203">NOTES</span></span>

## <span data-ttu-id="e690d-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e690d-204">RELATED LINKS</span></span>

[<span data-ttu-id="e690d-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e690d-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e690d-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e690d-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="e690d-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e690d-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


