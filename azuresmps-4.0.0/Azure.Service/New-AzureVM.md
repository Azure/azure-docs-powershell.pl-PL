---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055166"
---
# New-AzureVM

## STRESZCZENIe
Umożliwia utworzenie maszyny wirtualnej platformy Azure.

## POLECENIA

### ExistingService (domyślny)
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Usługa serviceservice
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureVM** umożliwia dodanie nowej maszyny wirtualnej do istniejącej usługi Azure lub utworzenie maszyny wirtualnej i usługi w bieżącej subskrypcji, jeśli została określona *Lokalizacja* lub *AffinityGroup* .

## Przykłady

### Przykład 1: Tworzenie maszyny wirtualnej dla konfiguracji systemu Windows
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

To polecenie tworzy konfigurację obsługi na podstawie konfiguracji maszyny wirtualnej dla systemu operacyjnego Windows i używa jej do tworzenia maszyny wirtualnej w określonej grupie koligacji.

### Przykład 2: Tworzenie maszyny wirtualnej dla konfiguracji systemu Linux
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

To polecenie tworzy konfigurację obsługi na podstawie konfiguracji maszyny wirtualnej dla systemu Linux i używa jej do tworzenia maszyny wirtualnej w określonej grupie koligacji.

### Przykład 3: Tworzenie maszyny wirtualnej i Dodawanie dysku z danymi
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

Dwa pierwsze polecenia uzyskują dostępne obrazy za pomocą polecenia cmdlet **Get-AzureVMImage** i zapisuje je w zmiennej $Image.

To polecenie tworzy konfigurację obsługi na podstawie konfiguracji maszyny wirtualnej dla systemu operacyjnego Windows i używa jej do tworzenia maszyny wirtualnej z dyskiem danych platformy Azure.

### Przykład 4: Tworzenie maszyny wirtualnej z zastrzeżonym adresem IP
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

To polecenie tworzy konfigurację obsługi na podstawie konfiguracji maszyny wirtualnej dla systemu operacyjnego Windows i używa jej do tworzenia maszyny wirtualnej z zastrzeżonym adresem IP.

## PARAMETRÓW

### -AffinityGroup
Określa grupę koligacji platformy Azure, w której znajduje się usługa chmury.
Ten parametr jest wymagany tylko wtedy, gdy to polecenie cmdlet tworzy usługę w chmurze.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentLabel
Określa etykietę wdrożenia.

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

### -Deploymentname
Określa nazwę wdrożenia.
Jeśli nie podano tego polecenia, to polecenie cmdlet użyje nazwy usługi jako nazwy wdrożenia.

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

### -DnsSettings
Określa obiekt serwera DNS definiujący ustawienia DNS nowego wdrożenia.

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InternalLoadBalancerConfig
Umożliwia określenie wewnętrznego modułu równoważenia obciążenia.
Ten parametr nie jest stosowany.

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację, w której znajduje się nowa usługa.
Jeśli usługa już istnieje, nie określaj tego parametru.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReservedIPName
Określa nazwę zastrzeżonego adresu IP.

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

### -ReverseDnsFqdn
Określa w pełni kwalifikowaną nazwę domeny dla zwrotnego DNS.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Opis
Określa opis nowej usługi.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servicelabel
Określa etykietę nowej usługi.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Określa nową lub istniejącą nazwę usługi.

Jeśli usługa nie istnieje, to polecenie cmdlet utworzy je za Ciebie.
Użyj parametru *Location* lub *AffinityGroup* , aby określić, gdzie utworzyć usługę.

Jeśli ta usługa istnieje, parametr *Lokalizacja* lub *AffinityGroup* nie jest potrzebny.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMs
Określa listę obiektów maszyny wirtualnej, które mają zostać utworzone.

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -VNetName
Określa nazwę sieci wirtualnej, w której to polecenie cmdlet wdraża maszynę wirtualną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForBoot
Określa, że to polecenie cmdlet oczekuje, że maszyna wirtualna będzie mieć dostęp do stanu **ReadyRole** .
To polecenie cmdlet kończy się niepowodzeniem, jeśli maszyna wirtualna jest w jednym z następujących stanów podczas oczekiwania: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureDataDisk](./Add-AzureDataDisk.md)

[Dodaj-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Nowe — AzureVMConfig](./New-AzureVMConfig.md)


