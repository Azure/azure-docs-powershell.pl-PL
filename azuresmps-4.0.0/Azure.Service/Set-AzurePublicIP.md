---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054921"
---
# Set-AzurePublicIP

## STRESZCZENIe
Dodaje publiczny adres IP do maszyny wirtualnej platformy Azure.

## POLECENIA

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzurePublicIP** dodaje publiczny adres IP do maszyny wirtualnej platformy Azure.
Jeśli uruchamiasz to polecenie cmdlet dla istniejącej maszyny wirtualnej, zaktualizuj maszynę wirtualną, aby zaimplementować zmiany.
Możesz określić etykietę nazwy domeny, aby utworzyć odpowiedni wpis DNS dla publicznego adresu IP.

## Przykłady

### Przykład 1: Dodawanie publicznego adresu IP do istniejącej maszyny wirtualnej
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

To polecenie pobiera maszynę wirtualną o nazwie FTPInstance w usłudze o nazwie FTPInAzure przy użyciu polecenia cmdlet **Get-AzureVM** .
Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet umożliwia dodanie publicznej nazwy ftpip.
Polecenie przekazanie maszyny wirtualnej do polecenia cmdlet **Update-AzureVM** , które implementuje wprowadzone zmiany.

### Przykład 2: Dodawanie publicznego adresu IP do nowej maszyny wirtualnej
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

To polecenie tworzy obiekt konfiguracji maszyny wirtualnej przy użyciu polecenia cmdlet **New-AzureVMConfig** .
Polecenie przekazuje ten obiekt do polecenia cmdlet **Add-AzureProvisioningConfig** , które zapewnia dodatkową konfigurację.
Bieżące polecenie cmdlet umożliwia dodanie publicznej nazwy ftpip.
Polecenie przekazanie konfiguracji do polecenia cmdlet **New-AzureVM** , które powoduje utworzenie maszyny wirtualnej.

### Przykład 3: Dodawanie publicznego adresu IP i etykiety do istniejącej maszyny wirtualnej
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

To polecenie pobiera maszynę wirtualną o nazwie FTPInstance w usłudze o nazwie FTPInAzure przy użyciu polecenia cmdlet **Get-AzureVM** .
Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet dodaje publiczną nazwę IP ftpip i etykietę ipname.
Polecenie aktualizuje maszynę wirtualną, która implementuje wprowadzone zmiany.

### Przykład 4: Dodawanie publicznego adresu IP i etykiety do nowej maszyny wirtualnej
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje ten obiekt do **dodatku Add-AzureProvisioningConfig** , który zapewnia dodatkową konfigurację.
Bieżące polecenie cmdlet dodaje publiczną nazwę IP ftpip i etykietę ipname.
Polecenie tworzy maszynę wirtualną.

## PARAMETRÓW

### -DomainNameLabel
Określa nazwę, która ma być używana dla odpowiedniego wpisu DNS dla publicznego adresu IP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
Określa okres czasu bezczynności protokołu TCP w minutach.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

### -PublicIPName
Określa publiczną nazwę IP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Określa maszynę wirtualną, do której to polecenie cmdlet dodaje publiczny adres IP.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. servicemanagement. model. IPersistentVM

## INFORMACYJN

## LINKI POKREWNE

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[Get-AzureVM](./Get-AzureVM.md)

[Nowe — AzureVM](./New-AzureVM.md)

[Nowe — AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzurePublicIP](./Remove-AzurePublicIP.md)

[Update-AzureVM](./Update-AzureVM.md)


