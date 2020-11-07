---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 107441c07e958099d330859a5003a2dafcd64bf9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893626"
---
# <span data-ttu-id="3b580-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b580-101">New-AzVM</span></span>

## <span data-ttu-id="3b580-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b580-102">SYNOPSIS</span></span>
<span data-ttu-id="3b580-103">Umożliwia utworzenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="3b580-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b580-104">SYNTAX</span></span>

### <span data-ttu-id="3b580-105">SimpleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3b580-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b580-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b580-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b580-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b580-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b580-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3b580-108">DESCRIPTION</span></span>
<span data-ttu-id="3b580-109">Polecenie cmdlet **New-AzVM** umożliwia utworzenie maszyny wirtualnej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="3b580-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="3b580-110">To polecenie cmdlet pobiera obiekt maszyny wirtualnej jako wejście.</span><span class="sxs-lookup"><span data-stu-id="3b580-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="3b580-111">Użyj polecenia cmdlet New-AzVMConfig, aby utworzyć obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="3b580-112">Do konfigurowania maszyny wirtualnej można użyć innych poleceń cmdlet, takich jak Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface i Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="3b580-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

<span data-ttu-id="3b580-113">`SimpleParameterSet`Zapewnia wygodną metodę tworzenia maszyny wirtualnej, wprowadzając opcjonalnie typowe argumenty tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="3b580-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b580-114">EXAMPLES</span></span>

### <span data-ttu-id="3b580-115">Przykład 1: Tworzenie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3b580-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm
```

<span data-ttu-id="3b580-116">Ten przykładowy skrypt przedstawia sposób tworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="3b580-117">Ten skrypt używa kilku innych poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b580-117">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="3b580-118">Przykład 2: Tworzenie maszyny wirtualnej na podstawie niestandardowego obrazu użytkownika</span><span class="sxs-lookup"><span data-stu-id="3b580-118">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="3b580-119">W tym przykładzie zostanie podjęta lista sys-prepped, uogólniony niestandardowy obraz systemu operacyjnego i dołączanie do niego dysku danych, zastosowanie nowej sieci, wdrożenie dysku VHD i uruchomienie go.</span><span class="sxs-lookup"><span data-stu-id="3b580-119">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="3b580-120">Tego skryptu można użyć do automatycznego inicjowania obsługi administracyjnej, ponieważ używa on lokalnych poświadczeń administratora maszyny wirtualnej w tekście zamiast nawiązywania połączeń z **poświadczeniami** , które wymagają interakcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3b580-120">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="3b580-121">Ten skrypt zakłada, że użytkownik jest już zalogowany na koncie platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3b580-121">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="3b580-122">Aby potwierdzić stan logowania, użyj polecenia cmdlet **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="3b580-122">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="3b580-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b580-123">PARAMETERS</span></span>

### <span data-ttu-id="3b580-124">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3b580-124">-AddressPrefix</span></span>
<span data-ttu-id="3b580-125">Prefiks adresu sieci wirtualnej, który zostanie utworzony dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-125">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-126">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="3b580-126">-AllocationMethod</span></span>
<span data-ttu-id="3b580-127">Metoda przydzielania adresów IP dla publicznego adresu IP, które zostaną utworzone dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-127">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b580-128">-AsJob</span></span>
<span data-ttu-id="3b580-129">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="3b580-129">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3b580-130">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="3b580-130">-AvailabilitySetName</span></span>
<span data-ttu-id="3b580-131">Określa nazwę zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="3b580-131">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-132">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="3b580-132">-Credential</span></span>
<span data-ttu-id="3b580-133">Poświadczenia administratora maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-133">The administrator credentials for the VM.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b580-134">-DefaultProfile</span></span>
<span data-ttu-id="3b580-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b580-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b580-136">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="3b580-136">-DisableBginfoExtension</span></span>
<span data-ttu-id="3b580-137">Wskazuje, że to polecenie cmdlet nie instaluje rozszerzenia **informacji o BG** na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-137">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-138">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="3b580-138">-DiskFile</span></span>
<span data-ttu-id="3b580-139">Lokalna ścieżka do pliku wirtualnego dysku twardego, która ma zostać przekazana do chmury i do utworzenia maszyny wirtualnej, i musi zawierać jako sufiks "VHD".</span><span class="sxs-lookup"><span data-stu-id="3b580-139">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-140">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="3b580-140">-DomainNameLabel</span></span>
<span data-ttu-id="3b580-141">Etykieta poddomeny dla w pełni kwalifikowanej nazwy domeny (FQDN) maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-141">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="3b580-142">Spowoduje to wykonanie formularza `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="3b580-142">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-143">-ImageName</span><span class="sxs-lookup"><span data-stu-id="3b580-143">-ImageName</span></span>
<span data-ttu-id="3b580-144">Przyjazna nazwa obrazu, na podstawie której będzie budowana maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="3b580-144">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="3b580-145">Dotyczy to: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-przestępna, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="3b580-145">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-146">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3b580-146">-LicenseType</span></span>
<span data-ttu-id="3b580-147">Określa typ licencji wskazujący, że obraz lub dysk maszyny wirtualnej jest licencjonowany lokalnie.</span><span class="sxs-lookup"><span data-stu-id="3b580-147">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="3b580-148">Ta wartość jest używana tylko w przypadku obrazów zawierających system operacyjny Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3b580-148">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="3b580-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3b580-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b580-150">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="3b580-150">Windows_Client</span></span> 
- <span data-ttu-id="3b580-151">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="3b580-151">Windows_Server</span></span>

<span data-ttu-id="3b580-152">Tej wartości nie można zaktualizować.</span><span class="sxs-lookup"><span data-stu-id="3b580-152">This value cannot be updated.</span></span>
<span data-ttu-id="3b580-153">Jeśli określisz ten parametr dla aktualizacji, wartość musi być zgodna z wartością początkową maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-153">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-154">-Linux</span><span class="sxs-lookup"><span data-stu-id="3b580-154">-Linux</span></span>
<span data-ttu-id="3b580-155">Wskazuje, czy plik dysku dotyczy maszyny wirtualnej Linux, jeśli jest określony; lub Windows, jeśli domyślnie nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="3b580-155">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-156">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3b580-156">-Location</span></span>
<span data-ttu-id="3b580-157">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-157">Specifies a location for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-158">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b580-158">-Name</span></span>
<span data-ttu-id="3b580-159">Nazwa zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-159">The name of the VM resource.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-160">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="3b580-160">-OpenPorts</span></span>
<span data-ttu-id="3b580-161">Lista portów do otwarcia w grupie zabezpieczeń sieci (NSG) dla utworzonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-161">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="3b580-162">Wartość domyślna zależy od typu wybranego obrazu (tzn. Windows: 3389, 5985 i Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="3b580-162">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-163">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="3b580-163">-PublicIpAddressName</span></span>
<span data-ttu-id="3b580-164">Nazwa nowego (lub istniejącego) publicznego adresu IP do użycia dla utworzonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-164">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="3b580-165">Jeśli nie określono, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="3b580-165">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b580-166">-ResourceGroupName</span></span>
<span data-ttu-id="3b580-167">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b580-167">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-168">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="3b580-168">-SecurityGroupName</span></span>
<span data-ttu-id="3b580-169">Nazwa nowej (lub istniejącej) grupy zabezpieczeń sieci (NSG) dla utworzonej maszyny wirtualnej do użycia.</span><span class="sxs-lookup"><span data-stu-id="3b580-169">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="3b580-170">Jeśli nie określono, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="3b580-170">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-171">-Size</span><span class="sxs-lookup"><span data-stu-id="3b580-171">-Size</span></span>
<span data-ttu-id="3b580-172">Rozmiar maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-172">The Virtual Machine Size.</span></span>  <span data-ttu-id="3b580-173">Wartość domyślna to: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="3b580-173">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-174">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3b580-174">-SubnetAddressPrefix</span></span>
<span data-ttu-id="3b580-175">Prefiks adresu podsieci, który zostanie utworzony dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-175">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-176">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="3b580-176">-SubnetName</span></span>
<span data-ttu-id="3b580-177">Nazwa nowej (lub istniejącej) podsieci do użycia dla utworzonej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-177">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="3b580-178">Jeśli nie określono, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="3b580-178">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b580-179">-Tag</span></span>
<span data-ttu-id="3b580-180">Określa, że zasoby i grupy zasobów mogą być znakowane za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="3b580-180">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="3b580-181">Dodawanie znaczników do zasobów umożliwia grupowanie zasobów między grupami zasobów i tworzenie własnych widoków.</span><span class="sxs-lookup"><span data-stu-id="3b580-181">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="3b580-182">Każdy zasób lub Grupa zasobów może zawierać maksymalnie 15 tagów.</span><span class="sxs-lookup"><span data-stu-id="3b580-182">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-183">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3b580-183">-VirtualNetworkName</span></span>
<span data-ttu-id="3b580-184">Nazwa nowej (lub istniejącej) sieci wirtualnej dla utworzonej maszyny wirtualnej do użycia.</span><span class="sxs-lookup"><span data-stu-id="3b580-184">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="3b580-185">Jeśli nie określono, zostanie wygenerowana nazwa.</span><span class="sxs-lookup"><span data-stu-id="3b580-185">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-186">-VM</span><span class="sxs-lookup"><span data-stu-id="3b580-186">-VM</span></span>
<span data-ttu-id="3b580-187">Umożliwia określenie lokalnej maszyny wirtualnej do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="3b580-187">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="3b580-188">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="3b580-188">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="3b580-189">Do konfigurowania maszyny wirtualnej można użyć innych poleceń cmdlet, takich jak Set-AzVMOperatingSystem, Set-AzVMSourceImage i Add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="3b580-189">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="3b580-190">-Zone</span></span>
<span data-ttu-id="3b580-191">Określa listę stref maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3b580-191">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-192">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b580-192">-Confirm</span></span>
<span data-ttu-id="3b580-193">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b580-193">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b580-194">-WhatIf</span></span>
<span data-ttu-id="3b580-195">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b580-195">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3b580-196">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b580-196">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b580-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b580-197">CommonParameters</span></span>
<span data-ttu-id="3b580-198">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b580-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b580-199">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b580-199">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b580-200">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b580-200">INPUTS</span></span>

### <span data-ttu-id="3b580-201">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3b580-201">PSVirtualMachine</span></span>
<span data-ttu-id="3b580-202">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="3b580-202">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="3b580-203">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b580-203">OUTPUTS</span></span>

### <span data-ttu-id="3b580-204">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3b580-204">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3b580-205">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b580-205">NOTES</span></span>

## <span data-ttu-id="3b580-206">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b580-206">RELATED LINKS</span></span>

[<span data-ttu-id="3b580-207">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b580-207">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3b580-208">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b580-208">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="3b580-209">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b580-209">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="3b580-210">Start — AzVM</span><span class="sxs-lookup"><span data-stu-id="3b580-210">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="3b580-211">Zatrzymaj — AzVM</span><span class="sxs-lookup"><span data-stu-id="3b580-211">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="3b580-212">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3b580-212">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="3b580-213">Dodaj-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3b580-213">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="3b580-214">Dodaj-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3b580-214">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="3b580-215">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="3b580-215">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="3b580-216">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3b580-216">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="3b580-217">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="3b580-217">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="3b580-218">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="3b580-218">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


