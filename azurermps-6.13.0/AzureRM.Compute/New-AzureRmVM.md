---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: da307e1bc5bca5c3127e33a32bb4480148fe14a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717470"
---
# <span data-ttu-id="18ea7-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="18ea7-101">New-AzureRmVM</span></span>

## <span data-ttu-id="18ea7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="18ea7-103">Umożliwia utworzenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18ea7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18ea7-104">SYNTAX</span></span>

### <span data-ttu-id="18ea7-105">SimpleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="18ea7-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18ea7-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="18ea7-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18ea7-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="18ea7-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18ea7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="18ea7-108">DESCRIPTION</span></span>
<span data-ttu-id="18ea7-109">Polecenie cmdlet **New-AzureRmVM** umożliwia utworzenie maszyny wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="18ea7-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="18ea7-110">To polecenie cmdlet pobiera obiekt maszyny wirtualnej jako wejście.</span><span class="sxs-lookup"><span data-stu-id="18ea7-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="18ea7-111">Użyj polecenia cmdlet New-AzureRmVMConfig, aby utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="18ea7-112">Do konfigurowania maszyny wirtualnej można użyć innych poleceń cmdlet, takich jak Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface i Set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="18ea7-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>
<span data-ttu-id="18ea7-113">`SimpleParameterSet`Zapewnia wygodną metodę tworzenia maszyny wirtualnej, wprowadzając opcjonalnie typowe argumenty tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="18ea7-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18ea7-114">EXAMPLES</span></span>

### <span data-ttu-id="18ea7-115">Przykład 1: Tworzenie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="18ea7-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="18ea7-116">Ten przykładowy skrypt przedstawia sposób tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="18ea7-117">Skrypt poprosi o podanie nazwy użytkownika i hasła do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="18ea7-118">Ten skrypt używa kilku innych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ea7-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="18ea7-119">Przykład 2: Tworzenie maszyny wirtualnej na podstawie niestandardowego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="18ea7-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="18ea7-120">W tym przykładzie zostanie podjęta lista sys-prepped, uogólniony niestandardowy obraz systemu operacyjnego i dołączanie do niego dysku danych, zastosowanie nowej sieci, wdrożenie dysku VHD i uruchomienie go.</span><span class="sxs-lookup"><span data-stu-id="18ea7-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="18ea7-121">Tego skryptu można użyć do automatycznego inicjowania obsługi administracyjnej, ponieważ używa on lokalnych poświadczeń administratora maszyny wirtualnej w tekście zamiast nawiązywania połączeń z **poświadczeniami** , które wymagają interakcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="18ea7-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="18ea7-122">Ten skrypt zakłada, że użytkownik jest już zalogowany na koncie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="18ea7-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="18ea7-123">Aby potwierdzić stan logowania, użyj polecenia cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="18ea7-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

### <span data-ttu-id="18ea7-124">Przykład 3: Tworzenie maszyny wirtualnej na podstawie obrazu witryny Marketplace bez publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="18ea7-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="18ea7-125">W tym przykładzie przedstawiono sposób tworzenia nowej sieci i wdrożenia maszyny wirtualnej z systemem Windows z poziomu witryny Marketplace bez tworzenia publicznego adresu IP lub grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="18ea7-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="18ea7-126">Tego skryptu można użyć do automatycznego inicjowania obsługi administracyjnej, ponieważ używa on lokalnych poświadczeń administratora maszyny wirtualnej w tekście zamiast nawiązywania połączeń z **poświadczeniami** , które wymagają interakcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="18ea7-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="18ea7-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18ea7-127">PARAMETERS</span></span>

### <span data-ttu-id="18ea7-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="18ea7-128">-AddressPrefix</span></span>
<span data-ttu-id="18ea7-129">Prefiks adresu sieci wirtualnej, który zostanie utworzony dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="18ea7-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="18ea7-130">-AllocationMethod</span></span>
<span data-ttu-id="18ea7-131">Metoda przydzielania adresów IP dla publicznego adresu IP, które zostaną utworzone dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="18ea7-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18ea7-132">-AsJob</span></span>
<span data-ttu-id="18ea7-133">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="18ea7-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="18ea7-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="18ea7-134">-AvailabilitySetName</span></span>
<span data-ttu-id="18ea7-135">Określa nazwę zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="18ea7-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="18ea7-136">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="18ea7-136">-Credential</span></span>
<span data-ttu-id="18ea7-137">Poświadczenia administratora maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="18ea7-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="18ea7-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="18ea7-139">Określa rozmiary dysków z danymi w GB.</span><span class="sxs-lookup"><span data-stu-id="18ea7-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="18ea7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ea7-140">-DefaultProfile</span></span>
<span data-ttu-id="18ea7-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="18ea7-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18ea7-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="18ea7-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="18ea7-143">Wskazuje, że to polecenie cmdlet nie instaluje rozszerzenia **informacji o BG** na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="18ea7-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="18ea7-144">-DiskFile</span></span>
<span data-ttu-id="18ea7-145">Lokalna ścieżka do pliku wirtualnego dysku twardego, która ma zostać przekazana do chmury i do utworzenia maszyny wirtualnej, i musi zawierać jako sufiks "VHD".</span><span class="sxs-lookup"><span data-stu-id="18ea7-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="18ea7-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="18ea7-146">-DomainNameLabel</span></span>
<span data-ttu-id="18ea7-147">Etykieta poddomeny dla w pełni kwalifikowanej nazwy domeny (FQDN) maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="18ea7-148">Spowoduje to wykonanie formularza `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="18ea7-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="18ea7-149">-Image</span><span class="sxs-lookup"><span data-stu-id="18ea7-149">-Image</span></span>
<span data-ttu-id="18ea7-150">Przyjazna nazwa obrazu, na podstawie której będzie budowana maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="18ea7-150">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="18ea7-151">Dotyczy to: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-przestępna, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="18ea7-151">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="18ea7-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="18ea7-152">-LicenseType</span></span>
<span data-ttu-id="18ea7-153">Określa typ licencji wskazujący, że obraz lub dysk maszyny wirtualnej jest licencjonowany lokalnie.</span><span class="sxs-lookup"><span data-stu-id="18ea7-153">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="18ea7-154">Ta wartość jest używana tylko w przypadku obrazów zawierających system operacyjny Windows Server.</span><span class="sxs-lookup"><span data-stu-id="18ea7-154">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="18ea7-155">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="18ea7-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18ea7-156">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="18ea7-156">Windows_Client</span></span>
- <span data-ttu-id="18ea7-157">Windows_Server tej wartości nie można zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="18ea7-157">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="18ea7-158">Jeśli określisz ten parametr dla aktualizacji, wartość musi być zgodna z wartością początkową maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-158">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="18ea7-159">-Linux</span><span class="sxs-lookup"><span data-stu-id="18ea7-159">-Linux</span></span>
<span data-ttu-id="18ea7-160">Wskazuje, czy plik dysku dotyczy maszyny wirtualnej Linux, jeśli jest określony; lub Windows, jeśli domyślnie nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="18ea7-160">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="18ea7-161">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="18ea7-161">-Location</span></span>
<span data-ttu-id="18ea7-162">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-162">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="18ea7-163">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="18ea7-163">-Name</span></span>
<span data-ttu-id="18ea7-164">Nazwa zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-164">The name of the VM resource.</span></span>

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

### <span data-ttu-id="18ea7-165">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="18ea7-165">-OpenPorts</span></span>
<span data-ttu-id="18ea7-166">Lista portów do otwarcia w grupie zabezpieczeń sieci (NSG) dla utworzonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-166">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="18ea7-167">Wartość domyślna zależy od typu wybranego obrazu (tzn. Windows: 3389, 5985 i Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="18ea7-167">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="18ea7-168">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="18ea7-168">-PublicIpAddressName</span></span>
<span data-ttu-id="18ea7-169">Nazwa nowego (lub istniejącego) publicznego adresu IP do użycia dla utworzonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-169">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="18ea7-170">Jeśli nie określono, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="18ea7-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="18ea7-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18ea7-171">-ResourceGroupName</span></span>
<span data-ttu-id="18ea7-172">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="18ea7-172">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="18ea7-173">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="18ea7-173">-SecurityGroupName</span></span>
<span data-ttu-id="18ea7-174">Nazwa nowej (lub istniejącej) grupy zabezpieczeń sieci (NSG) dla utworzonej maszyny wirtualnej do użycia.</span><span class="sxs-lookup"><span data-stu-id="18ea7-174">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="18ea7-175">Jeśli nie określono, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="18ea7-175">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="18ea7-176">-Size</span><span class="sxs-lookup"><span data-stu-id="18ea7-176">-Size</span></span>
<span data-ttu-id="18ea7-177">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-177">The Virtual Machine Size.</span></span>  <span data-ttu-id="18ea7-178">Wartość domyślna to: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="18ea7-178">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="18ea7-179">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="18ea7-179">-SubnetAddressPrefix</span></span>
<span data-ttu-id="18ea7-180">Prefiks adresu podsieci, który zostanie utworzony dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-180">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="18ea7-181">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="18ea7-181">-SubnetName</span></span>
<span data-ttu-id="18ea7-182">Nazwa nowej (lub istniejącej) podsieci do użycia dla utworzonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-182">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="18ea7-183">Jeśli nie określono, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="18ea7-183">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="18ea7-184">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="18ea7-184">-SystemAssignedIdentity</span></span>
<span data-ttu-id="18ea7-185">Jeśli parametr jest obecny, maszyna wirtualna ma przypisaną tożsamość systemową, która jest generowana automatycznie.</span><span class="sxs-lookup"><span data-stu-id="18ea7-185">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="18ea7-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="18ea7-186">-Tag</span></span>
<span data-ttu-id="18ea7-187">Określa, że zasoby i grupy zasobów mogą być znakowane za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="18ea7-187">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="18ea7-188">Dodawanie znaczników do zasobów umożliwia grupowanie zasobów między grupami zasobów i tworzenie własnych widoków.</span><span class="sxs-lookup"><span data-stu-id="18ea7-188">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="18ea7-189">Każdy zasób lub Grupa zasobów może zawierać maksymalnie 15 tagów.</span><span class="sxs-lookup"><span data-stu-id="18ea7-189">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="18ea7-190">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="18ea7-190">-UserAssignedIdentity</span></span>
<span data-ttu-id="18ea7-191">Nazwa tożsamości zarządzanej usługi, która powinna być przypisana do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-191">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="18ea7-192">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="18ea7-192">-VirtualNetworkName</span></span>
<span data-ttu-id="18ea7-193">Nazwa nowej (lub istniejącej) sieci wirtualnej dla utworzonej maszyny wirtualnej do użycia.</span><span class="sxs-lookup"><span data-stu-id="18ea7-193">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="18ea7-194">Jeśli nie określono, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="18ea7-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="18ea7-195">-VM</span><span class="sxs-lookup"><span data-stu-id="18ea7-195">-VM</span></span>
<span data-ttu-id="18ea7-196">Umożliwia określenie lokalnej maszyny wirtualnej do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="18ea7-196">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="18ea7-197">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="18ea7-197">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="18ea7-198">Do konfigurowania maszyny wirtualnej można użyć innych poleceń cmdlet, takich jak Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage i Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="18ea7-198">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="18ea7-199">-Zone</span><span class="sxs-lookup"><span data-stu-id="18ea7-199">-Zone</span></span>
<span data-ttu-id="18ea7-200">Określa listę stref maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="18ea7-200">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="18ea7-201">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="18ea7-201">-Confirm</span></span>
<span data-ttu-id="18ea7-202">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ea7-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18ea7-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18ea7-203">-WhatIf</span></span>
<span data-ttu-id="18ea7-204">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18ea7-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18ea7-205">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="18ea7-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18ea7-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ea7-206">CommonParameters</span></span>
<span data-ttu-id="18ea7-207">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ea7-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ea7-208">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ea7-208">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ea7-209">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18ea7-209">INPUTS</span></span>

### <span data-ttu-id="18ea7-210">System. String</span><span class="sxs-lookup"><span data-stu-id="18ea7-210">System.String</span></span>

### <span data-ttu-id="18ea7-211">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="18ea7-211">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="18ea7-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="18ea7-212">System.String[]</span></span>

### <span data-ttu-id="18ea7-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18ea7-213">System.Collections.Hashtable</span></span>

## <span data-ttu-id="18ea7-214">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18ea7-214">OUTPUTS</span></span>

### <span data-ttu-id="18ea7-215">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="18ea7-215">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="18ea7-216">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="18ea7-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="18ea7-217">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18ea7-217">NOTES</span></span>

## <span data-ttu-id="18ea7-218">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18ea7-218">RELATED LINKS</span></span>

[<span data-ttu-id="18ea7-219">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="18ea7-219">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="18ea7-220">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="18ea7-220">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="18ea7-221">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="18ea7-221">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="18ea7-222">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="18ea7-222">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="18ea7-223">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="18ea7-223">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="18ea7-224">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="18ea7-224">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="18ea7-225">Dodaj-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="18ea7-225">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="18ea7-226">Dodaj-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="18ea7-226">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="18ea7-227">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="18ea7-227">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="18ea7-228">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="18ea7-228">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="18ea7-229">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="18ea7-229">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="18ea7-230">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="18ea7-230">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


