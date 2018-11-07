---
title: Rozpoczynanie pracy z programem Azure PowerShell | Microsoft Docs
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 3114f9e9b36dc374f9fb2d402c448cff7fef0aa3
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211455"
---
# <a name="getting-started-with-azure-powershell"></a>Rozpoczynanie pracy z programem Azure PowerShell

Program Azure PowerShell jest przeznaczony do zarządzania i administrowania zasobami platformy Azure przy użyciu wiersza polecenia oraz do tworzenia skryptów automatyzacji, które pozwalają obsługiwać usługę Azure Resource Manager. Można go również używać w przeglądarce z usługą [Azure Cloud Shell](/azure/cloud-shell/overview) albo można go zainstalować na maszynie lokalnej i używać w dowolnej sesji programu PowerShell. W tym artykule przedstawiono podstawowe pojęcia związane z programem Azure PowerShell, które ułatwiają rozpoczęcie korzystania z niego.

## <a name="connect"></a>Połączenie

Najprostszym sposobem na rozpoczęcie pracy jest [uruchomienie usługi Cloud Shell](/azure/cloud-shell/quickstart).

1. Uruchom usługę Cloud Shell z górnego obszaru nawigacyjnego witryny Azure Portal.

   ![Ikona powłoki](~/media/get-started-azureps/shell-icon.png)

2. Wybierz subskrypcję, której chcesz użyć, a następnie utwórz konto magazynu.

   ![Tworzenie konta magazynu](~/media/get-started-azureps/storage-prompt.png)

Po utworzeniu magazynu usługa Cloud Shell otworzy sesję programu PowerShell w przeglądarce.

![Usługa Cloud Shell dla programu PowerShell](~/media/get-started-azureps/cloud-powershell.png)

Program Azure PowerShell można również zainstalować i używać lokalnie w sesji programu PowerShell.

## <a name="install-azure-powershell"></a>Instalowanie programu Azure PowerShell

Pierwszym krokiem jest upewnienie się, że jest zainstalowana najnowsza wersja programu Azure PowerShell. Aby uzyskać informacje o najnowszej wersji, zobacz [informacje o wersji](./release-notes-azureps.md).

1. [Zainstalowanie programu Azure PowerShell](install-azurerm-ps.md).

2. Aby sprawdzić, czy instalacja się powiodła, uruchom polecenie `Get-Module AzureRM -ListAvailable` w wierszu polecenia.

## <a name="log-in-to-azure"></a>Zaloguj się do platformy Azure.

Logowanie interaktywne:

1. Wpisz polecenie `Login-AzureRmAccount`. Zostanie wyświetlone okno dialogowe z monitem o podanie poświadczeń platformy Azure. Opcja „-EnvironmentName” pozwala zalogować się na platformie Azure (Chiny) lub Azure (Niemcy).

   np. Login-AzureRmAccount -EnvironmentName AzureChinaCloud

2. Wpisz adres e-mail i hasło skojarzone z kontem. Nastąpi uwierzytelnienie i zapisanie informacji o poświadczeniach na platformie Azure, a następnie zamknięcie okna.

Po zalogowaniu się do konta platformy Azure można korzystać z poleceń cmdlet programu Azure PowerShell w celu uzyskania dostępu do zasobów subskrypcji i zarządzania nimi.

## <a name="create-a-resource-group"></a>Tworzenie grupy zasobów

Teraz gdy wszystko jest już skonfigurowane, użyjemy programu Azure PowerShell do utworzenia zasobów na platformie Azure.

Najpierw utwórz grupę zasobów. Grupy zasobów na platformie Azure umożliwiają zarządzanie wieloma zasobami, które chcesz logicznie pogrupować razem. Możesz na przykład utworzyć grupę zasobów dla aplikacji lub projektu i dodać do niej maszynę wirtualną, bazę danych i usługę CDN.

Utworzymy grupę zasobów o nazwie „MyResourceGroup” w regionie westeurope świadczenia usługi Azure. W tym celu wpisz następujące polecenie:

```powershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a>Tworzenie maszyny wirtualnej z systemem Windows

Teraz gdy mamy grupę zasobów, utwórzmy w niej maszynę wirtualną z systemem Windows. Aby utworzyć nową maszynę wirtualną, musimy najpierw utworzyć inne wymagane zasoby i przypisać je do konfiguracji. Następnie możemy użyć tej konfiguracji do utworzenia maszyny wirtualnej.

### <a name="create-the-required-network-resources"></a>Tworzenie wymaganych zasobów sieciowych

Najpierw musimy utworzyć konfigurację podsieci, która będzie używana w procesie tworzenia sieci wirtualnej. Musimy również utworzyć publiczny adres IP umożliwiający nawiązywanie połączeń z tą maszyną wirtualną. Dostęp do publicznego adresu zostanie zabezpieczony przy użyciu sieciowej grupy zabezpieczeń. Na koniec za pomocą wszystkich wymienionych zasobów utworzymy wirtualną kartę sieciową.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>Tworzenie maszyny wirtualnej

Potrzebujemy zestawu poświadczeń dla systemu operacyjnego.

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

Teraz gdy mamy potrzebne zasoby, możemy utworzyć maszynę wirtualną. W tym kroku utworzymy obiekt konfiguracji maszyny wirtualnej, a następnie użyjemy tej konfiguracji do utworzenia maszyny wirtualnej.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Polecenie `New-AzureRmVM` zwraca dane wyjściowe, gdy maszyna wirtualna została w pełni utworzona i można jej używać.

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

Teraz zaloguj się do nowo utworzonej maszyny wirtualnej z systemem Windows Server za pomocą pulpitu zdalnego i publicznego adresu IP maszyny wirtualnej. Następujące polecenie umożliwia wyświetlenie publicznego adresu IP utworzonego w poprzednim skrypcie.

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

Jeśli korzystasz z komputera z systemem Windows, możesz to zrobić w wierszu polecenia przy użyciu polecenia mstsc:

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

Aby się zalogować, podaj tę samą kombinację nazwy użytkownika/hasła, którą podano podczas tworzenia maszyny wirtualnej.

## <a name="create-a-linux-virtual-machine"></a>Tworzenie maszyny wirtualnej z systemem Linux

Aby utworzyć nową maszynę wirtualną z systemem Linux, musimy najpierw utworzyć inne wymagane zasoby i przypisać je do konfiguracji. Następnie możemy użyć tej konfiguracji do utworzenia maszyny wirtualnej. Zakłada się, że została już utworzona grupa zasobów zgodnie z wcześniejszymi instrukcjami. Ponadto w katalogu ssh profilu użytkownika musi znajdować się klucz publiczny SSH o nazwie `id_rsa.pub`.

### <a name="create-the-required-network-resources"></a>Tworzenie wymaganych zasobów sieciowych

Najpierw musimy utworzyć konfigurację podsieci, która będzie używana w procesie tworzenia sieci wirtualnej. Musimy również utworzyć publiczny adres IP umożliwiający nawiązywanie połączeń z tą maszyną wirtualną. Dostęp do publicznego adresu zostanie zabezpieczony przy użyciu sieciowej grupy zabezpieczeń. Na koniec za pomocą wszystkich wymienionych zasobów utworzymy wirtualną kartę sieciową.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>Tworzenie maszyny wirtualnej

Teraz gdy mamy potrzebne zasoby, możemy utworzyć maszynę wirtualną. W tym kroku utworzymy obiekt konfiguracji maszyny wirtualnej, a następnie użyjemy tej konfiguracji do utworzenia maszyny wirtualnej.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Teraz gdy maszyna wirtualna została już utworzona, możesz zalogować się do swojej nowej maszyny wirtualnej z systemem Linux przy użyciu protokołu SSH i publicznego adresu IP utworzonej maszyny wirtualnej:

```bash
ssh xx.xxx.xxx.xxx
```

```Output
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

## <a name="creating-other-resources-in-azure"></a>Tworzenie innych zasobów na platformie Azure

Omówiliśmy sposób tworzenia grupy zasobów, maszyny wirtualnej z systemem Linux i maszyny wirtualnej z systemem Windows Server. Możesz również utworzyć wiele innych typów zasobów platformy Azure.

Aby na przykład utworzyć moduł równoważenia obciążenia sieci platformy Azure, który można będzie potem skojarzyć z nowo utworzonymi maszynami wirtualnymi, możemy użyć następującego polecenia create:

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Możemy także utworzyć nową prywatną sieć wirtualną (nazywaną „VNet” na platformie Azure) dla naszej infrastruktury, korzystając z następującego polecenia:

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Tym, co sprawia, że platforma Azure i program Azure PowerShell są tak przydatne, jest to, że możemy ich używać nie tylko do uzyskiwania infrastruktury opartej na chmurze, ale również do tworzenia zarządzanych usług platformy. Zarządzane usługi platformy można również łączyć z infrastrukturą w celu tworzenia jeszcze bardziej zaawansowanych rozwiązań.

Możesz na przykład użyć programu Azure PowerShell do utworzenia usługi Azure App Service. Usługa Azure App Service to zarządzana usługa platformy, która zapewnia doskonały sposób hostowania aplikacji internetowych bez konieczności troszczenia się o infrastrukturę. Po utworzeniu usługi Azure App Service możesz utworzyć dwie nowe aplikacje Azure Web Apps w ramach usługi App Service, korzystając z następujących poleceń:

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Wyświetlanie listy wdrożonych zasobów

Listę zasobów uruchomionych na platformie Azure można wyświetlić za pomocą polecenia cmdlet `Get-AzureRmResource`. W poniższym przykładzie zostaną wyświetlone zasoby utworzone w nowej grupie zasobów.

```powershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a>Usuwanie zasobów

Wyczyszczenie konta platformy Azure polega na usunięciu zasobów utworzonych w tym przykładzie. Aby usunąć zasoby, które nie są już potrzebne, możesz użyć poleceń cmdlet `Remove-AzureRm*`. Aby usunąć utworzoną maszynę wirtualną z systemem Windows, użyj następującego polecenia:

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Pojawi się monit o potwierdzenie usunięcia zasobu.

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Można także usuwać wiele zasobów jednocześnie. Na przykład następujące polecenie pozwala usunąć całą grupę zasobów „MyResourceGroup”, która była używana we wszystkich przykładach w tym samouczku wprowadzającym. Usunięta zostanie grupa zasobów i wszystkie zasoby w niej zawarte.

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Może to potrwać kilka minut.

## <a name="get-samples"></a>Pobieranie przykładów

Aby dowiedzieć się więcej o sposobach używania programu Azure PowerShell, zapoznaj się z naszymi najbardziej typowymi skryptami dla [maszyn wirtualnych z systemem Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [maszyn wirtualnych z systemem Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [aplikacji internetowych](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) i [baz danych SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Następne kroki

* [Logowanie za pomocą programu Azure PowerShell](authenticate-azureps.md)
* [Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell](manage-subscriptions-azureps.md)
* [Tworzenie jednostek usługi na platformie Azure przy użyciu programu Azure PowerShell](create-azure-service-principal-azureps.md)
* Przeczytaj informacje o wersji dotyczące migracji ze starszej wersji: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Uzyskiwanie pomocy od społeczności:
  * [Forum platformy Azure w witrynie MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Witryna Stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
