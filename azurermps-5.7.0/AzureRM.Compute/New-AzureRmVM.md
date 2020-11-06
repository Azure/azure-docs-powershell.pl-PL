---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526950"
---
# New-AzureRmVM

## STRESZCZENIe
Umożliwia utworzenie maszyny wirtualnej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### SimpleParameterSet (domyślny)
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DefaultParameterSet
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DiskFileParameterSet
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmVM** umożliwia utworzenie maszyny wirtualnej na platformie Azure.
To polecenie cmdlet pobiera obiekt maszyny wirtualnej jako wejście.
Użyj polecenia cmdlet New-AzureRmVMConfig, aby utworzyć obiekt maszyny wirtualnej.
Do konfigurowania maszyny wirtualnej można użyć innych poleceń cmdlet, takich jak Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface i Set-AzureRmVMOSDisk.

`SimpleParameterSet`Zapewnia wygodną metodę tworzenia maszyny wirtualnej, wprowadzając opcjonalnie typowe argumenty tworzenia maszyny wirtualnej.

## Przykłady

### Przykład 1: Tworzenie maszyny wirtualnej
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

Ten przykładowy skrypt przedstawia sposób tworzenia maszyny wirtualnej.
Skrypt poprosi o podanie nazwy użytkownika i hasła do maszyny wirtualnej.
Ten skrypt używa kilku innych poleceń cmdlet.

### Przykład 2: Tworzenie maszyny wirtualnej na podstawie niestandardowego obrazu użytkownika
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

W tym przykładzie zostanie podjęta lista sys-prepped, uogólniony niestandardowy obraz systemu operacyjnego i dołączanie do niego dysku danych, zastosowanie nowej sieci, wdrożenie dysku VHD i uruchomienie go.

Tego skryptu można użyć do automatycznego inicjowania obsługi administracyjnej, ponieważ używa on lokalnych poświadczeń administratora maszyny wirtualnej w tekście zamiast nawiązywania połączeń z **poświadczeniami** , które wymagają interakcji użytkownika.

Ten skrypt zakłada, że użytkownik jest już zalogowany na koncie platformy Azure.
Aby potwierdzić stan logowania, użyj polecenia cmdlet **Get-AzureSubscription** .

## PARAMETRÓW

### -AddressPrefix
Prefiks adresu sieci wirtualnej, który zostanie utworzony dla maszyny wirtualnej.

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

### -AllocationMethod
Metoda przydzielania adresów IP dla publicznego adresu IP, które zostaną utworzone dla maszyny wirtualnej.

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

### -AsJob
Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.

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

### -AvailabilitySetName
Określa nazwę zestawu dostępności.

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

### — Poświadczenie
Poświadczenia administratora maszyny wirtualnej.

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

### -DataDiskSizeInGb
Określa rozmiary dysków z danymi w GB.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -DisableBginfoExtension
Wskazuje, że to polecenie cmdlet nie instaluje rozszerzenia **informacji o BG** na maszynie wirtualnej.

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

### -DiskFile
Lokalna ścieżka do pliku wirtualnego dysku twardego, która ma zostać przekazana do chmury i do utworzenia maszyny wirtualnej, i musi zawierać jako sufiks "VHD".

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

### -DomainNameLabel
Etykieta poddomeny dla w pełni kwalifikowanej nazwy domeny (FQDN) maszyny wirtualnej.  Spowoduje to wykonanie formularza `{domainNameLabel}.{location}.cloudapp.azure.com` .

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

### -ImageName
Przyjazna nazwa obrazu, na podstawie której będzie budowana maszyna wirtualna.  Dotyczy to: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-przestępna, RHEL, SLES.

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

### -LicenseType
Określa typ licencji wskazujący, że obraz lub dysk maszyny wirtualnej jest licencjonowany lokalnie.
Ta wartość jest używana tylko w przypadku obrazów zawierających system operacyjny Windows Server.
Dopuszczalne wartości tego parametru to:

- Windows_Client
- Windows_Server

Tej wartości nie można zaktualizować.
Jeśli określisz ten parametr dla aktualizacji, wartość musi być zgodna z wartością początkową maszyny wirtualnej.

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

### -Linux
Wskazuje, czy plik dysku dotyczy maszyny wirtualnej Linux, jeśli jest określony; lub Windows, jeśli domyślnie nie jest określony.

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

### — Lokalizacja
Określa lokalizację maszyny wirtualnej.

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

### -Name (nazwa)
Nazwa zasobu maszyny wirtualnej.

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

### -OpenPorts
Lista portów do otwarcia w grupie zabezpieczeń sieci (NSG) dla utworzonej maszyny wirtualnej.  Wartość domyślna zależy od typu wybranego obrazu (tzn. Windows: 3389, 5985 i Linux: 22).

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

### -PublicIpAddressName
Nazwa nowego (lub istniejącego) publicznego adresu IP do użycia dla utworzonej maszyny wirtualnej.  Jeśli nie określono, zostanie wygenerowana nazwa.

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

### -ResourceGroupName
Określa nazwę grupy zasobów.

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

### -SecurityGroupName
Nazwa nowej (lub istniejącej) grupy zabezpieczeń sieci (NSG) dla utworzonej maszyny wirtualnej do użycia.  Jeśli nie określono, zostanie wygenerowana nazwa.

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

### -Size
Rozmiar maszyny wirtualnej.  Wartość domyślna to: Standard_DS1_v2.

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

### -SubnetAddressPrefix
Prefiks adresu podsieci, który zostanie utworzony dla maszyny wirtualnej.

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

### -Subnetname
Nazwa nowej (lub istniejącej) podsieci do użycia dla utworzonej maszyny wirtualnej.  Jeśli nie określono, zostanie wygenerowana nazwa.

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

### -Tag
Określa, że zasoby i grupy zasobów mogą być znakowane za pomocą zestawu par nazwa-wartość.
Dodawanie znaczników do zasobów umożliwia grupowanie zasobów między grupami zasobów i tworzenie własnych widoków.
Każdy zasób lub Grupa zasobów może zawierać maksymalnie 15 tagów.

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

### -VirtualNetworkName
Nazwa nowej (lub istniejącej) sieci wirtualnej dla utworzonej maszyny wirtualnej do użycia.  Jeśli nie określono, zostanie wygenerowana nazwa.

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

### -VM
Umożliwia określenie lokalnej maszyny wirtualnej do utworzenia.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet New-AzureRmVMConfig.
Do konfigurowania maszyny wirtualnej można użyć innych poleceń cmdlet, takich jak Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage i Add-AzureRmVMNetworkInterface.

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

### -Zone
Określa listę stref maszyny wirtualnej.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.

Polecenie cmdlet nie jest uruchamiane.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSVirtualMachine
Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Remove-AzureRmVM](./Remove-AzureRmVM.md)

[Restart-AzureRmVM](./Restart-AzureRmVM.md)

[Start — AzureRmVM](./Start-AzureRmVM.md)

[Zatrzymaj — AzureRmVM](./Stop-AzureRmVM.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)

[Dodaj-AzureRmVMDataDisk](./Add-AzureRmVMDataDisk.md)

[Dodaj-AzureRmVMNetworkInterface](./Add-AzureRmVMNetworkInterface.md)

[Nowe — AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)

[Set-AzureRmVMSourceImage](./Set-AzureRmVMSourceImage.md)

[Set-AzureRmVMOSDisk](./Set-AzureRmVMOSDisk.md)


