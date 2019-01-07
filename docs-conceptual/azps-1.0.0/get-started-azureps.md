---
title: Rozpoczynanie pracy z programem Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 10/30/2018
ms.openlocfilehash: 7367648a0a84cd5be5c7501ef4bf743a4290ce0f
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982913"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="6f0b3-102">Rozpoczynanie pracy z programem Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f0b3-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="6f0b3-103">Program Azure PowerShell jest przeznaczony do zarządzania i administrowania zasobami platformy Azure przy użyciu wiersza polecenia oraz do tworzenia skryptów automatyzacji, które pozwalają obsługiwać usługę Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="6f0b3-104">Można go używać w przeglądarce dzięki usłudze [Azure Cloud Shell](/azure/cloud-shell/overview) albo można go zainstalować na maszynie lokalnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="6f0b3-105">W tym artykule przedstawiono podstawowe pojęcia związane z programem Azure PowerShell, które ułatwiają rozpoczęcie korzystania z niego.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="6f0b3-106">Instalowanie programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f0b3-106">Install Azure PowerShell</span></span>

<span data-ttu-id="6f0b3-107">Pierwszym krokiem jest upewnienie się, że jest zainstalowana najnowsza wersja programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="6f0b3-108">Aby uzyskać informacje o najnowszej wersji, zobacz [informacje o wersji](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6f0b3-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="6f0b3-109">[Zainstalowanie programu Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="6f0b3-109">[Install Azure PowerShell](install-az-ps.md).</span></span>

2. <span data-ttu-id="6f0b3-110">Aby sprawdzić, czy instalacja się powiodła, uruchom polecenie `Get-InstalledModule Az -AllVersions` w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-110">To verify the installation was successful, run `Get-InstalledModule Az -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="6f0b3-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="6f0b3-111">Azure Cloud Shell</span></span>

<span data-ttu-id="6f0b3-112">Najprostszym sposobem na rozpoczęcie pracy jest [uruchomienie usługi Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="6f0b3-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="6f0b3-113">Uruchom usługę Cloud Shell z górnego obszaru nawigacyjnego witryny Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Ikona powłoki](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="6f0b3-115">Wybierz subskrypcję, której chcesz użyć, a następnie utwórz konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Tworzenie konta magazynu](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="6f0b3-117">Po utworzeniu magazynu usługa Cloud Shell otworzy sesję programu PowerShell w przeglądarce.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Usługa Cloud Shell dla programu PowerShell](~/media/get-started-azureps/cloud-powershell.png)

## <a name="sign-in-to-azure"></a><span data-ttu-id="6f0b3-119">Logowanie do platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6f0b3-119">Sign in to Azure</span></span>

<span data-ttu-id="6f0b3-120">Logowanie interaktywne:</span><span class="sxs-lookup"><span data-stu-id="6f0b3-120">Sign on interactively:</span></span>

1. <span data-ttu-id="6f0b3-121">Wpisz polecenie `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-121">Type `Connect-AzAccount`.</span></span> <span data-ttu-id="6f0b3-122">Argument `-Environment` umożliwia uwierzytelnienie w innym regionie lub chmurze.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-122">The `-Environment` argument lets you authenticate for a different region or cloud.</span></span> <span data-ttu-id="6f0b3-123">Aby na przykład nawiązać połączenie z platformą Azure (Chiny):</span><span class="sxs-lookup"><span data-stu-id="6f0b3-123">For example, to connect to Azure China:</span></span>

    ```powershell-interactive
    Connect-AzAccount -Environment AzureChinaCloud
    ```

2. <span data-ttu-id="6f0b3-124">Uzyskasz token do użycia w witrynie https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-124">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="6f0b3-125">Otwórz tę stronę w przeglądarce i wprowadź token, aby zalogować się przy użyciu swoich poświadczeń platformy Azure i autoryzować program Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-125">Open this page in your browser and enter the token to sign in with your Azure credentials, and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="6f0b3-126">Po zalogowaniu się do konta platformy Azure można korzystać z poleceń cmdlet programu Azure PowerShell w celu uzyskania dostępu do zasobów subskrypcji i zarządzania nimi.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-126">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span> <span data-ttu-id="6f0b3-127">Aby dowiedzieć się więcej na temat procesu logowania i dostępnych metod uwierzytelniania, zobacz [Logowanie się w programie Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6f0b3-127">To learn more about the sign in process and available authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="6f0b3-128">Tworzenie maszyny wirtualnej z systemem Windows przy użyciu prostych wartości domyślnych</span><span class="sxs-lookup"><span data-stu-id="6f0b3-128">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="6f0b3-129">Polecenie cmdlet `New-AzVM` udostępnia uproszczoną składnię, co ułatwia utworzenie nowej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-129">The `New-AzVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="6f0b3-130">Trzeba podać jedynie dwie wartości parametrów: nazwę maszyny wirtualnej i zestaw poświadczeń dla lokalnego konta administratora na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-130">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="6f0b3-131">Najpierw utwórz obiekt poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-131">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="6f0b3-132">Następnie utwórz maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-132">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="6f0b3-133">Możesz się zastanawiać, co jeszcze jest tworzone i w jaki sposób maszyna wirtualna jest konfigurowana.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-133">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="6f0b3-134">Najpierw przyjrzyjmy się grupom zasobów.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-134">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="6f0b3-135">Grupa zasobów **cloud-shell-storage-westus** jest tworzona przy pierwszym użyciu usługi Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-135">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="6f0b3-136">Grupa zasobów **SampleVM** została utworzona przez polecenie cmdlet `New-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-136">The **SampleVM** resource group was created by the `New-AzVM` cmdlet.</span></span>

<span data-ttu-id="6f0b3-137">Jakie inne zasoby zostały utworzone w tej nowej grupie zasobów?</span><span class="sxs-lookup"><span data-stu-id="6f0b3-137">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="6f0b3-138">Uzyskajmy trochę więcej szczegółowych informacji o maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-138">Let's get some more details about the VM.</span></span> <span data-ttu-id="6f0b3-139">Poniższy przykład pokazuje, jak pobrać informacje o obrazie systemu operacyjnego użytym do utworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-139">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="6f0b3-140">Tworzenie w pełni skonfigurowanej maszyny wirtualnej z systemem Linux</span><span class="sxs-lookup"><span data-stu-id="6f0b3-140">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="6f0b3-141">W powyższym przykładzie użyto uproszczonej składni i domyślnych wartości parametrów do utworzenia maszyny wirtualnej z systemem Windows.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-141">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="6f0b3-142">W tym przykładzie podajemy wartości dla wszystkich opcji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-142">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="6f0b3-143">Tworzenie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6f0b3-143">Create a resource group</span></span>

<span data-ttu-id="6f0b3-144">W tym przykładzie chcemy utworzyć grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-144">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="6f0b3-145">Grupy zasobów na platformie Azure umożliwiają zarządzanie wieloma zasobami, które chcesz logicznie pogrupować razem.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-145">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="6f0b3-146">Możesz na przykład utworzyć grupę zasobów dla aplikacji lub projektu i dodać do niej maszynę wirtualną, bazę danych i usługę CDN.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-146">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="6f0b3-147">Utwórzmy grupę zasobów o nazwie „MyResourceGroup” w regionie świadczenia usługi Azure uswest2.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-147">Let's create a resource group named "MyResourceGroup" in the uswest2 region of Azure.</span></span> <span data-ttu-id="6f0b3-148">W tym celu wpisz następujące polecenie:</span><span class="sxs-lookup"><span data-stu-id="6f0b3-148">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name 'myResourceGroup' -Location 'westus2'
```

```output
ResourceGroupName : myResourceGroup
Location          : westus2
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="6f0b3-149">W tej nowej grupie zasobów zostaną umieszczone wszystkie zasoby niezbędne dla nowej maszyny wirtualnej, którą utworzymy.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-149">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="6f0b3-150">Aby utworzyć nową maszynę wirtualną z systemem Linux, musimy najpierw utworzyć inne wymagane zasoby i przypisać je do konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-150">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="6f0b3-151">Następnie możemy użyć tej konfiguracji do utworzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-151">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="6f0b3-152">Ponadto w katalogu `.ssh` profilu użytkownika musi znajdować się klucz publiczny SSH o nazwie `id_rsa.pub`.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-152">Also, you will need to have an SSH public key named `id_rsa.pub` in the `.ssh` directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="6f0b3-153">Tworzenie wymaganych zasobów sieciowych</span><span class="sxs-lookup"><span data-stu-id="6f0b3-153">Create the required network resources</span></span>

<span data-ttu-id="6f0b3-154">Najpierw musimy utworzyć konfigurację podsieci, która będzie używana w procesie tworzenia sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-154">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="6f0b3-155">Musimy również utworzyć publiczny adres IP umożliwiający nawiązywanie połączeń z tą maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-155">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="6f0b3-156">Dostęp do publicznego adresu zostanie zabezpieczony przy użyciu sieciowej grupy zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-156">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="6f0b3-157">Na koniec za pomocą wszystkich wymienionych zasobów utworzymy wirtualną kartę sieciową.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-157">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westus2"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="6f0b3-158">Tworzenie konfiguracji maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6f0b3-158">Create the VM configuration</span></span>

<span data-ttu-id="6f0b3-159">Teraz, gdy mamy potrzebne zasoby, możemy utworzyć obiekt konfiguracji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-159">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzVMConfig -VMName $vmName -VMSize Standard_B1s |
  Set-AzVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="6f0b3-160">Tworzenie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="6f0b3-160">Create the virtual machine</span></span>

<span data-ttu-id="6f0b3-161">Teraz możemy utworzyć maszynę wirtualną za pomocą obiektu konfiguracji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-161">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="6f0b3-162">Teraz, gdy maszyna wirtualna została już utworzona, możesz zalogować się do swojej nowej maszyny wirtualnej z systemem Linux przy użyciu protokołu SSH i publicznego adresu IP utworzonej maszyny wirtualnej:</span><span class="sxs-lookup"><span data-stu-id="6f0b3-162">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```powershell-interactive
ssh azureuser@$($publicIp.IpAddress)
```

```output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="6f0b3-163">Tworzenie innych zasobów na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="6f0b3-163">Creating other resources in Azure</span></span>

<span data-ttu-id="6f0b3-164">Omówiliśmy sposób tworzenia grupy zasobów, maszyny wirtualnej z systemem Linux i maszyny wirtualnej z systemem Windows Server.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-164">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="6f0b3-165">Możesz również utworzyć wiele innych typów zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-165">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="6f0b3-166">Aby na przykład utworzyć moduł równoważenia obciążenia sieci platformy Azure, który można będzie potem skojarzyć z nowo utworzonymi maszynami wirtualnymi, możemy użyć następującego polecenia create:</span><span class="sxs-lookup"><span data-stu-id="6f0b3-166">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westus2
```

<span data-ttu-id="6f0b3-167">Możemy także utworzyć nową prywatną sieć wirtualną (nazywaną „VNet” na platformie Azure) dla naszej infrastruktury, korzystając z następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="6f0b3-167">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzVirtualNetwork -ResourceGroupName myResourceGroup -Location westus2 `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="6f0b3-168">Tym, co sprawia, że platforma Azure i program Azure PowerShell są tak przydatne, jest to, że możemy ich używać nie tylko do uzyskiwania infrastruktury opartej na chmurze, ale również do tworzenia zarządzanych usług platformy.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-168">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="6f0b3-169">Zarządzane usługi platformy można również łączyć z infrastrukturą w celu tworzenia jeszcze bardziej zaawansowanych rozwiązań.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-169">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="6f0b3-170">Możesz na przykład użyć programu Azure PowerShell do utworzenia usługi Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-170">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="6f0b3-171">Usługa Azure App Service to zarządzana usługa platformy, która zapewnia doskonały sposób hostowania aplikacji internetowych bez konieczności troszczenia się o infrastrukturę.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-171">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="6f0b3-172">Po utworzeniu usługi Azure App Service możesz utworzyć dwie nowe aplikacje Azure Web Apps w ramach usługi App Service, korzystając z następujących poleceń:</span><span class="sxs-lookup"><span data-stu-id="6f0b3-172">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Get a UUID for creating the apps to avoid name conflicts
$guid = [System.Guid]::NewGuid().ToString()

# Create an Azure AppService that we can host any number of web apps within
New-AzAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westus2

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzWebApp -Name MyWebApp-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
New-AzWebApp -Name MyWebApp2-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="6f0b3-173">Wyświetlanie listy wdrożonych zasobów</span><span class="sxs-lookup"><span data-stu-id="6f0b3-173">Listing deployed resources</span></span>

<span data-ttu-id="6f0b3-174">Listę zasobów uruchomionych na platformie Azure można wyświetlić za pomocą polecenia cmdlet `Get-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-174">You can use the `Get-AzResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="6f0b3-175">W poniższym przykładzie zostaną wyświetlone zasoby utworzone w nowej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-175">The following example shows the resources we created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westus2 Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westus2 Microsoft.Compute/disks
myLinuxVM                                             westus2 Microsoft.Compute/virtualMachines
myWindowsVM                                           westus2 Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westus2 Microsoft.Compute/virtualMachines/extensions
myNic1                                                westus2 Microsoft.Network/networkInterfaces
myNic2                                                westus2 Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westus2 Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westus2 Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westus2 Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westus2 Microsoft.Network/publicIPAddresses
MYvNET1                                               westus2 Microsoft.Network/virtualNetworks
MYvNET2                                               westus2 Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westus2 Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="6f0b3-176">Usuwanie zasobów</span><span class="sxs-lookup"><span data-stu-id="6f0b3-176">Deleting resources</span></span>

<span data-ttu-id="6f0b3-177">Wyczyszczenie konta platformy Azure polega na usunięciu zasobów utworzonych w tym przykładzie.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-177">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="6f0b3-178">Aby usunąć zasoby, które nie są już potrzebne, możesz użyć poleceń cmdlet `Remove-Az*`.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-178">You can use the `Remove-Az*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="6f0b3-179">Aby usunąć utworzoną maszynę wirtualną z systemem Windows, użyj następującego polecenia:</span><span class="sxs-lookup"><span data-stu-id="6f0b3-179">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="6f0b3-180">Pojawi się monit o potwierdzenie usunięcia zasobu.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-180">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6f0b3-181">Można także usuwać wiele zasobów jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-181">You can also delete many resources at once.</span></span> <span data-ttu-id="6f0b3-182">Na przykład następujące polecenie pozwala usunąć grupę zasobów „MyResourceGroup”, która była używana we wszystkich dotychczasowych przykładach.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-182">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="6f0b3-183">Zostaną również usunięte wszystkie zasoby w grupie.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-183">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6f0b3-184">W zależności od liczby i typu zasobów wykonanie tego zadania może potrwać kilka minut.</span><span class="sxs-lookup"><span data-stu-id="6f0b3-184">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="6f0b3-185">Pobieranie przykładów</span><span class="sxs-lookup"><span data-stu-id="6f0b3-185">Get samples</span></span>

<span data-ttu-id="6f0b3-186">Aby dowiedzieć się więcej o sposobach używania programu Azure PowerShell, zapoznaj się z naszymi najbardziej typowymi skryptami dla [maszyn wirtualnych z systemem Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [maszyn wirtualnych z systemem Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [aplikacji internetowych](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) i [baz danych SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="6f0b3-186">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="6f0b3-187">Następne kroki</span><span class="sxs-lookup"><span data-stu-id="6f0b3-187">Next steps</span></span>

* [<span data-ttu-id="6f0b3-188">Logowanie się w programie Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f0b3-188">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="6f0b3-189">Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f0b3-189">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="6f0b3-190">Tworzenie jednostek usługi na platformie Azure przy użyciu programu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f0b3-190">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="6f0b3-191">Uzyskiwanie pomocy od społeczności:</span><span class="sxs-lookup"><span data-stu-id="6f0b3-191">Get help from the community:</span></span>
  * [<span data-ttu-id="6f0b3-192">Forum platformy Azure w witrynie MSDN</span><span class="sxs-lookup"><span data-stu-id="6f0b3-192">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="6f0b3-193">Witryna Stackoverflow</span><span class="sxs-lookup"><span data-stu-id="6f0b3-193">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
