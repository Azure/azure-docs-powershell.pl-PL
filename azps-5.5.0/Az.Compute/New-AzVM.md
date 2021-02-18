---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 21c15b0395479a1a22e6b8420a97a3a7c0b75bce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181618"
---
# <span data-ttu-id="b6953-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6953-101">New-AzVM</span></span>

## <span data-ttu-id="b6953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6953-102">SYNOPSIS</span></span>
<span data-ttu-id="b6953-103">Tworzy maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="b6953-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="b6953-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6953-104">SYNTAX</span></span>

### <span data-ttu-id="b6953-105">SimpleParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b6953-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>]
 [-HostId <String>] [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6953-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6953-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6953-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6953-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6953-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6953-108">DESCRIPTION</span></span>
<span data-ttu-id="b6953-109">Polecenie **cmdlet New-AzVM** tworzy maszynę wirtualną na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b6953-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="b6953-110">To polecenie cmdlet pobiera obiekt maszyny wirtualnej jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="b6953-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="b6953-111">Użyj New-AzVMConfig cmdlet, aby utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="b6953-112">Inne polecenia cmdlet mogą być używane do konfigurowania maszyny wirtualnej, takie jak Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface i Set-AzVMOSSystem.</span><span class="sxs-lookup"><span data-stu-id="b6953-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="b6953-113">Zapewnia `SimpleParameterSet` ona wygodną metodę tworzenia maszyny wirtualnej przez opcjonalne utworzenie typowych argumentów utworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="b6953-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6953-114">EXAMPLES</span></span>

### <span data-ttu-id="b6953-115">Przykład 1. Tworzenie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b6953-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="b6953-116">W tym przykładzie pokazano, jak utworzyć maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="b6953-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="b6953-117">Skrypt poprosi o nazwę użytkownika i hasło maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="b6953-118">W tym skrypcie jest używane kilka innych cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6953-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="b6953-119">Przykład 2. Tworzenie maszyny wirtualnej z niestandardowego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="b6953-119">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account.
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance.
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3"
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="b6953-120">W tym przykładzie jest przechwytywany istniejący wstępnie wstępnie zlokalizowany, uogólniony obraz niestandardowego systemu operacyjnego i dołącza do niego dysk danych, inicjuje nową sieć, wdraża aplikację VHD i uruchamia ją.</span><span class="sxs-lookup"><span data-stu-id="b6953-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="b6953-121">Ten skrypt może być używany do automatycznego inicjowania obsługi administracyjnej, ponieważ używa on lokalnych poświadczeń administratora maszyn wirtualnych w tekście zamiast wywoływania funkcji **Get-Credential,** która wymaga interakcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6953-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="b6953-122">Ten skrypt zakłada, że zalogowano się już do konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b6953-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="b6953-123">Stan logowania możesz potwierdzić za pomocą polecenia cmdlet **Get-AzSubscription.**</span><span class="sxs-lookup"><span data-stu-id="b6953-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="b6953-124">Przykład 3. Tworzenie maszyny wirtualnej z obrazu rynku bez publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="b6953-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="b6953-125">W tym przykładzie wdrożono nową sieć i wdrożono maszynę wirtualnej systemu Windows z witryny Marketplace bez tworzenia publicznego adresu IP ani grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b6953-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="b6953-126">Ten skrypt może być używany do automatycznego inicjowania obsługi administracyjnej, ponieważ używa on lokalnych poświadczeń administratora maszyn wirtualnych w tekście zamiast wywoływania funkcji **Get-Credential,** która wymaga interakcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6953-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="b6953-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6953-127">PARAMETERS</span></span>

### <span data-ttu-id="b6953-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b6953-128">-AddressPrefix</span></span>
<span data-ttu-id="b6953-129">Prefiks adresu sieci wirtualnej, który zostanie utworzony dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="b6953-130">-AllocationMethod</span></span>
<span data-ttu-id="b6953-131">Metoda alokacji adresów IP dla publicznego adresu IP, który zostanie utworzony dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-132">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b6953-132">-AsJob</span></span>
<span data-ttu-id="b6953-133">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="b6953-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b6953-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="b6953-134">-AvailabilitySetName</span></span>
<span data-ttu-id="b6953-135">Określa nazwę zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="b6953-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-136">- Credential</span><span class="sxs-lookup"><span data-stu-id="b6953-136">-Credential</span></span>
<span data-ttu-id="b6953-137">Poświadczenia administratora maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-137">The administrator credentials for the VM.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-138">-DataSizeSizeInGb</span><span class="sxs-lookup"><span data-stu-id="b6953-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="b6953-139">Określa rozmiary dysków danych w GB.</span><span class="sxs-lookup"><span data-stu-id="b6953-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6953-140">-DefaultProfile</span></span>
<span data-ttu-id="b6953-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6953-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6953-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="b6953-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="b6953-143">Wskazuje, że to polecenie cmdlet nie instaluje rozszerzenia **BG Info** na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="b6953-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-144">- DiskFile</span><span class="sxs-lookup"><span data-stu-id="b6953-144">-DiskFile</span></span>
<span data-ttu-id="b6953-145">Ścieżka lokalna do wirtualnego pliku dysku twardego do przesłania do chmury i utworzenia maszyny wirtualnej, która musi mieć sufiks ".vhd".</span><span class="sxs-lookup"><span data-stu-id="b6953-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b6953-146">-DomainNameLabel</span></span>
<span data-ttu-id="b6953-147">Etykieta poddomeny dla w pełni kwalifikowanej nazwy domeny (FQDN) maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="b6953-148">Spowoduje to zajmę się `{domainNameLabel}.{location}.cloudapp.azure.com` formularzem.</span><span class="sxs-lookup"><span data-stu-id="b6953-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-149">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="b6953-149">-EnableUltraSSD</span></span>
<span data-ttu-id="b6953-150">Użyj dysków UltraSSD do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-150">Use UltraSSD disks for the vm.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6953-151">-EvictionPolicy</span></span>
<span data-ttu-id="b6953-152">Zasady wywłasowania dla maszyny wirtualnej Usługi Azure Spot.</span><span class="sxs-lookup"><span data-stu-id="b6953-152">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="b6953-153">Obsługiwane wartości to "Deallocate" i "Delete".</span><span class="sxs-lookup"><span data-stu-id="b6953-153">Supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-154">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="b6953-154">-HostGroupId</span></span>
<span data-ttu-id="b6953-155">Określa dedykowaną grupę hosta, w którym będzie znajdowała się maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="b6953-155">Specifies the dedicated host group the virtual machine will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-156">- HostId</span><span class="sxs-lookup"><span data-stu-id="b6953-156">-HostId</span></span>
<span data-ttu-id="b6953-157">Identyfikator hosta</span><span class="sxs-lookup"><span data-stu-id="b6953-157">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-158">— Obraz</span><span class="sxs-lookup"><span data-stu-id="b6953-158">-Image</span></span>
<span data-ttu-id="b6953-159">Przyjazna nazwa obrazu, na podstawie której zostanie zbudowana maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-159">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="b6953-160">Należą do nich: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, R UBUNTU, SLES.</span><span class="sxs-lookup"><span data-stu-id="b6953-160">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-161">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b6953-161">-LicenseType</span></span>
<span data-ttu-id="b6953-162">Określa typ licencji, który wskazuje, że obraz lub dysk maszyny wirtualnej został licencjonowany lokalnie.</span><span class="sxs-lookup"><span data-stu-id="b6953-162">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="b6953-163">Możliwe wartości dla systemu Windows Server to:</span><span class="sxs-lookup"><span data-stu-id="b6953-163">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="b6953-164">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="b6953-164">Windows_Client</span></span>
- <span data-ttu-id="b6953-165">Windows_Server możliwe wartości dla systemu operacyjnego Linux Server to:</span><span class="sxs-lookup"><span data-stu-id="b6953-165">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="b6953-166">RHEL_BYOS (dla RBLOCK)</span><span class="sxs-lookup"><span data-stu-id="b6953-166">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="b6953-167">SLES_BYOS (dla SUSE)</span><span class="sxs-lookup"><span data-stu-id="b6953-167">SLES_BYOS (for SUSE)</span></span> 

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-168">— Linux</span><span class="sxs-lookup"><span data-stu-id="b6953-168">-Linux</span></span>
<span data-ttu-id="b6953-169">Wskazuje, czy plik dysku jest dla maszyny wirtualnej systemu Linux, jeśli został określony; lub Windows, jeśli nie jest to domyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="b6953-169">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-170">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b6953-170">-Location</span></span>
<span data-ttu-id="b6953-171">Określa lokalizację dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-171">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-172">- MaxCena</span><span class="sxs-lookup"><span data-stu-id="b6953-172">-MaxPrice</span></span>
<span data-ttu-id="b6953-173">Maksymalna cena rozliczenia maszyny wirtualnej o niskim priorytecie.</span><span class="sxs-lookup"><span data-stu-id="b6953-173">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-174">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="b6953-174">-EncryptionAtHost</span></span>
<span data-ttu-id="b6953-175">Właściwość EncryptionAtHost może być używana przez użytkownika w żądaniu włączenia lub wyłączenia szyfrowania hosta dla zestawu skali maszyny wirtualnej lub maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-175">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="b6953-176">Spowoduje to włączenie szyfrowania dla wszystkich dysków, w tym dysku zasobu/tempa na samym hoście.</span><span class="sxs-lookup"><span data-stu-id="b6953-176">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="b6953-177">Domyślne: Szyfrowanie na hoście zostanie wyłączone, chyba że dla zasobu ta właściwość jest ustawiona na prawda.</span><span class="sxs-lookup"><span data-stu-id="b6953-177">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskParameterSet
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="b6953-178">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b6953-178">-Name</span></span>
<span data-ttu-id="b6953-179">Nazwa zasobu MASZYNY WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="b6953-179">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-180">- OpenPorts</span><span class="sxs-lookup"><span data-stu-id="b6953-180">-OpenPorts</span></span>
<span data-ttu-id="b6953-181">Lista portów do otwarcia w sieciowej grupie zabezpieczeń (NSG) utworzonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-181">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="b6953-182">Wartość domyślna zależy od typu wybranego obrazu (np. systemu Windows: 3389, 5985 i Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="b6953-182">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-183">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="b6953-183">-Priority</span></span>
<span data-ttu-id="b6953-184">Priorytet maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-184">The priority for the virtual machine.</span></span>  <span data-ttu-id="b6953-185">Obsługiwane są tylko wartości "Zwykła", "Spot" i "Niska".</span><span class="sxs-lookup"><span data-stu-id="b6953-185">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="b6953-186">"Zwykła" jest dla zwykłej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-186">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="b6953-187">"Spot" jest dla maszyny wirtualnej spot.</span><span class="sxs-lookup"><span data-stu-id="b6953-187">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="b6953-188">"Low" jest również dla maszyny wirtualnej spot, ale jest zastępowany przez "Spot".</span><span class="sxs-lookup"><span data-stu-id="b6953-188">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="b6953-189">Użyj pozycji "Spot" zamiast "Low".</span><span class="sxs-lookup"><span data-stu-id="b6953-189">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-190">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="b6953-190">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="b6953-191">Identyfikator zasobu grupy Położenie odległości do użycia z tą maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="b6953-191">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="b6953-192">-PublicIpAddressName</span></span>
<span data-ttu-id="b6953-193">Nazwa nowego (lub istniejącego) publicznego adresu IP utworzonej maszyny wirtualnej do użycia.</span><span class="sxs-lookup"><span data-stu-id="b6953-193">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="b6953-194">Jeśli nie zostanie określona, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="b6953-194">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6953-195">-ResourceGroupName</span></span>
<span data-ttu-id="b6953-196">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6953-196">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-197">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="b6953-197">-SecurityGroupName</span></span>
<span data-ttu-id="b6953-198">Nazwa nowej (lub istniejącej) grupy zabezpieczeń sieciowych (NSG) dla utworzonej maszyny wirtualnej do użycia.</span><span class="sxs-lookup"><span data-stu-id="b6953-198">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="b6953-199">Jeśli nie zostanie określona, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="b6953-199">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-200">— Rozmiar</span><span class="sxs-lookup"><span data-stu-id="b6953-200">-Size</span></span>
<span data-ttu-id="b6953-201">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-201">The Virtual Machine Size.</span></span>  <span data-ttu-id="b6953-202">Wartość domyślna to: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="b6953-202">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b6953-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="b6953-204">Prefiks adresu podsieci, która zostanie utworzona dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-204">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-205">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b6953-205">-SubnetName</span></span>
<span data-ttu-id="b6953-206">Nazwa nowej (lub istniejącej) podsieci dla utworzonej maszyny wirtualnej do użycia.</span><span class="sxs-lookup"><span data-stu-id="b6953-206">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="b6953-207">Jeśli nie zostanie określona, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="b6953-207">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-208">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b6953-208">-SystemAssignedIdentity</span></span>
<span data-ttu-id="b6953-209">Jeśli parametr jest obecny, oznacza to, że do maszyny wirtualnej jest przypisywana automatycznie generowana tożsamość systemu zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="b6953-209">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-210">— Tag</span><span class="sxs-lookup"><span data-stu-id="b6953-210">-Tag</span></span>
<span data-ttu-id="b6953-211">Określa, że zasoby i grupy zasobów mogą być otagowane za pomocą zestawu par wartości nazw.</span><span class="sxs-lookup"><span data-stu-id="b6953-211">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="b6953-212">Dodawanie tagów do zasobów umożliwia grupowanie zasobów w różnych grupach zasobów i tworzenie własnych widoków.</span><span class="sxs-lookup"><span data-stu-id="b6953-212">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="b6953-213">Każda grupa zasobów lub zasobu może mieć maksymalnie 15 tagów.</span><span class="sxs-lookup"><span data-stu-id="b6953-213">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b6953-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="b6953-215">Nazwa tożsamości usługi zarządzanej, która powinna zostać przypisana do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-215">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-216">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b6953-216">-VirtualNetworkName</span></span>
<span data-ttu-id="b6953-217">Nazwa nowej (lub istniejącej) sieci wirtualnej dla utworzonej maszyny wirtualnej do użycia.</span><span class="sxs-lookup"><span data-stu-id="b6953-217">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="b6953-218">Jeśli nie zostanie określona, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="b6953-218">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-219">- MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="b6953-219">-VM</span></span>
<span data-ttu-id="b6953-220">Określa lokalną maszynę wirtualną do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="b6953-220">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="b6953-221">Aby uzyskać obiekt maszyny wirtualnej, użyj New-AzVMConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6953-221">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="b6953-222">Inne polecenia cmdlet mogą być używane do konfigurowania maszyny wirtualnej, takie jak Set-AzVMOperatingSystem, Set-AzVMSourceImage i Add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="b6953-222">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-223">- Maszyny wirtualne</span><span class="sxs-lookup"><span data-stu-id="b6953-223">-VmssId</span></span>
<span data-ttu-id="b6953-224">Identyfikator zestawu skali maszyny wirtualnej, z który będzie skojarzona ta maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b6953-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-225">— Strefa</span><span class="sxs-lookup"><span data-stu-id="b6953-225">-Zone</span></span>
<span data-ttu-id="b6953-226">Określa listę stref maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b6953-226">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-227">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6953-227">-Confirm</span></span>
<span data-ttu-id="b6953-228">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b6953-228">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-229">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6953-229">-WhatIf</span></span>
<span data-ttu-id="b6953-230">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6953-230">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6953-231">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b6953-231">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6953-232">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6953-232">CommonParameters</span></span>
<span data-ttu-id="b6953-233">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6953-233">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6953-234">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6953-234">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6953-235">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6953-235">INPUTS</span></span>

### <span data-ttu-id="b6953-236">System.String</span><span class="sxs-lookup"><span data-stu-id="b6953-236">System.String</span></span>

### <span data-ttu-id="b6953-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b6953-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b6953-238">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b6953-238">System.String[]</span></span>

### <span data-ttu-id="b6953-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b6953-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b6953-240">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6953-240">OUTPUTS</span></span>

### <span data-ttu-id="b6953-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b6953-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="b6953-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b6953-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b6953-243">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6953-243">NOTES</span></span>

## <span data-ttu-id="b6953-244">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6953-244">RELATED LINKS</span></span>

[<span data-ttu-id="b6953-245">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6953-245">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b6953-246">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6953-246">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b6953-247">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6953-247">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b6953-248">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6953-248">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="b6953-249">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6953-249">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="b6953-250">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b6953-250">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="b6953-251">Add-AzVMDataData</span><span class="sxs-lookup"><span data-stu-id="b6953-251">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="b6953-252">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b6953-252">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="b6953-253">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b6953-253">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="b6953-254">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b6953-254">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="b6953-255">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="b6953-255">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="b6953-256">Set-AzVMOS Dolby</span><span class="sxs-lookup"><span data-stu-id="b6953-256">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


