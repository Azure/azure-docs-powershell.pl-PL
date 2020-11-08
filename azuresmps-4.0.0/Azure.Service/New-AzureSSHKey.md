---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054948"
---
# New-AzureSSHKey

## STRESZCZENIe
Tworzy obiekt klucza SSH, aby wstawić istniejący certyfikat do nowej maszyny wirtualnej opartej na platformie Linux.

## POLECENIA

### para
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### publickey
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureSSHKey** tworzy obiekt klucza SSH dla certyfikatu, który został już dodany do platformy Azure.
Ten obiekt klucza SSH może być następnie używany przez **nowe-AzureProvisioningConfig** podczas tworzenia obiektu konfiguracji dla nowej maszyny wirtualnej przy użyciu **nowych funkcji-AzureVM** lub podczas tworzenia nowej maszyny wirtualnej z opcją **New-AzureQuickVM**.
Po dołączeniu w ramach skryptu tworzenia maszyny wirtualnej do nowej maszyny wirtualnej zostanie dodany określony klucz publiczny SSH lub para kluczy.

## Przykłady

### Przykład 1: Tworzenie obiektu Ustawienia certyfikatu
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

To polecenie tworzy obiekt ustawienia certyfikatu dla istniejącego certyfikatu, a następnie zapisuje obiekt w zmiennej do późniejszego użycia.

### Przykład 2: Dodawanie certyfikatu do usługi
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

To polecenie umożliwia dodanie certyfikatu do usługi Azure, a następnie utworzenie nowej maszyny wirtualnej Linux używającej tego certyfikatu.

## PARAMETRÓW

### -Odcisk cyfrowy
Określa odcisk palca certyfikatu.

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

### -Para
Określa, że to polecenie cmdlet tworzy obiekt służący do wstawiania pary kluczy SSH do nowej konfiguracji maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Określa ścieżkę do przechowywania klucza publicznego SSH lub pary kluczy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicKey
Określa, że to polecenie cmdlet tworzy obiekt służący do wstawiania klucza publicznego SSH do nowej konfiguracji maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
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

[Dodaj-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Nowe — AzureVMConfig](./New-AzureVMConfig.md)

[Nowe — AzureVM](./New-AzureVM.md)

[Nowe — AzureQuickVM](./New-AzureQuickVM.md)


