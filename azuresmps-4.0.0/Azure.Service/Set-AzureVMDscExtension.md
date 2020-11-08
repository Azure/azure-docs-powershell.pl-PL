---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061821"
---
# Set-AzureVMDscExtension

## STRESZCZENIe
Konfiguruje rozszerzenie DSC na maszynie wirtualnej.

## POLECENIA

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureVMDscExtension** Konfigurowanie żądanego rozszerzenia konfiguracji stanu (DSC) na maszynie wirtualnej.

## Przykłady

### Przykład 1: Konfigurowanie rozszerzenia DSC na maszynie wirtualnej
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

To polecenie umożliwia skonfigurowanie rozszerzenia DSC na maszynie wirtualnej.

Pakiet MyConfiguration.ps1.zip musi być wcześniej przekazany do magazynu Azure Storage przy użyciu polecenia **Publikuj-AzureVMDscConfiguration** i zawiera MyConfiguration.ps1 skryptu i modułów, od których zależy.

Argument moja konfiguracja wskazuje określoną konfigurację DSC w skrypcie do wykonania.
Parametr- *ConfigurationArgument* określa tablicę skrótów z argumentami przekazanymi do funkcji konfiguracji.

### Przykład 2: Konfigurowanie rozszerzenia DSC na maszynie wirtualnej przy użyciu ścieżki do danych konfiguracji
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

To polecenie umożliwia skonfigurowanie rozszerzenia DSC na maszynie wirtualnej przy użyciu ścieżki do danych konfiguracyjnych.

## PARAMETRÓW

### -ConfigurationArchive
Określa nazwę pakietu konfiguracji (pliku zip), który został wcześniej przekazany za pomocą narzędzia publikowanie-AzureVMDscConfiguration.
Ten parametr musi określać tylko nazwę pliku bez ścieżki.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationArgument
Określa tablicę skrótów określającą argumenty funkcji konfiguracji.
Klucze odpowiadają nazwom parametrów i wartościom parametrów.

Dopuszczalne wartości tego parametru to:

- typy pierwotne
- ciąg
- macierzy
- PSCredential

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Określa ścieżkę pliku psd1, który określa dane funkcji konfiguracji.
Ten plik musi zawierać tablicę Hashtable, jak opisano w oddzieleniu danych dotyczących konfiguracji i środowiska https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .

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

### -ConfigurationName
Określa nazwę skryptu lub modułu konfiguracji wywoływanego przez rozszerzenie DSC.

Wartość tego parametru musi być nazwą jednej z funkcji konfiguracji zawartych w skryptach lub modułach spakowanych w *ConfigurationArchive*.

To polecenie cmdlet domyślnie określa nazwę pliku podaną przez parametr *ConfigurationArchive* , jeśli pominięto ten parametr, wyłączając wszystkie rozszerzenia.
Jeśli na przykład *ConfigurationArchive* jest "SalesWebSite.ps1.zip", wartością domyślną *konfiguracji ConfigurationName* jest "SalesWebSite".

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

### -ContainerName
Określa nazwę kontenera magazynu platformy Azure, w którym znajduje się *ConfigurationArchive* .

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

### -DataCollection
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

### -Force
Wskazuje, że to polecenie cmdlet zastępuje istniejące obiekty blob.

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

### -ReferenceName
Określa ciąg zdefiniowany przez użytkownika, za pomocą którego można odwołać się do rozszerzenia.
Ten parametr jest określany po pierwszym dodaniu rozszerzenia do maszyny wirtualnej.
W przypadku kolejnych aktualizacji przed aktualizacją rozszerzenia należy określić poprzednio wykorzystaną nazwę odwołania.
Element *ReferenceName* przypisany do rozszerzenia jest zwracany przy użyciu polecenia cmdlet **Get-AzureVM** .

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

### -StorageContext
Określa kontekst usługi Azure Storage, który zapewnia ustawienia zabezpieczeń używane do uzyskiwania dostępu do skryptu konfiguracji.
Ten kontekst zapewnia dostęp do odczytu kontenera określonego przez parametr *ContainerName* .

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Określa sufiks punktu końcowego DNS dla wszystkich usług magazynowania, na przykład "core.contoso.net".

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

### -Version
Określa określoną wersję rozszerzenia DSC, której należy użyć.
Wartość domyślna jest ustawiona na "1. *", jeśli ten parametr nie jest określony.

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

### -VM
Określa trwały obiekt maszyny wirtualnej.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WmfVersion
Określa wersję narzędzia Windows Management Framework (WMF) do zainstalowania na maszynie wirtualnej.
Rozszerzenie DSC zależy od funkcji DSC, które są dostępne tylko w przypadku aktualizacji WMF.
Ten parametr określa wersję aktualizacji do zainstalowania na maszynie wirtualnej.
Dopuszczalne wartości tego parametru to:

- 4,0.
Instaluje program WMF 4,0, chyba że jest już zainstalowana nowsza wersja.
- 5,0.
Instaluje najnowszą wersję plików WMF 5,0.
- późniejsza.
Instaluje najnowszą wersję plików WMF, obecnie 5,0.

Wartość domyślna to najnowsza.

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

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureVMDscExtension](./Get-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Get-AzureVM](./Get-AzureVM.md)

[Publikowanie — AzureVMDscConfiguration](./Publish-AzureVMDscConfiguration.md)


