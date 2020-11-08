---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054898"
---
# New-AzureCertificateSetting

## STRESZCZENIe
Tworzy obiekt ustawienia certyfikatu dla certyfikatu w usłudze.

## POLECENIA

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureCertificateSetting** tworzy obiekt ustawienia certyfikatu dla certyfikatu, który znajduje się w usłudze Azure.

Za pomocą obiektu Ustawienia certyfikatu można utworzyć obiekt konfiguracji przy użyciu polecenia cmdlet **Add-AzureProvisioningConfig** .
Użyj obiektu konfiguracji do utworzenia maszyny wirtualnej za pomocą polecenia cmdlet **New-AzureVM** .
Za pomocą obiektu Ustawienia certyfikatu można utworzyć maszynę wirtualną przy użyciu polecenia cmdlet **New-AzureQuickVM** .

## Przykłady

### Przykład 1: Tworzenie obiektu Ustawienia certyfikatu
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

To polecenie tworzy obiekt ustawienia certyfikatu dla istniejącego certyfikatu.

### Przykład 2: Tworzenie maszyny wirtualnej używającej obiektu ustawień konfiguracji
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

Pierwsze polecenie dodaje certyfikat ContosoCert. cer do usługi o nazwie ContosoService przy użyciu polecenia cmdlet **Add-AzureCertificate** .

Drugie polecenie tworzy obiekt ustawienia certyfikatu, a następnie zapisuje go w zmiennej $CertificateSetting.

Trzecie polecenie pobiera obraz z repozytorium obrazów przy użyciu polecenia cmdlet **Get-AzureVMImage** .
To polecenie zapisuje obraz w zmiennej $Image.

Ostatnie polecenie tworzy obiekt konfiguracji maszyny wirtualnej na podstawie obrazu w $Image przy użyciu polecenia cmdlet **New-AzureVMConfig** .
Polecenie przekazuje ten obiekt do polecenia cmdlet **Add-AzureProvisioningConfig** przy użyciu operatora potoku.
Polecenie cmdlet umożliwia dodanie informacji o aprowizacji do konfiguracji.
Polecenie przekazuje obiekt do polecenia cmdlet **New-AzureVM** , które powoduje utworzenie maszyny wirtualnej.

## PARAMETRÓW

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

### -Pole NazwaSklepu
Określa magazyn certyfikatów, w którym ma zostać umieszczony certyfikat.
Prawidłowe wartości: 

- Adresowej
- AuthRoot
- CertificateAuthority
- — Zabronione
- MOJE
- Poziomie głównym
- TrustedPeople
- TrustedPublisher

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Odcisk palca
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureCertificate](./Add-AzureCertificate.md)

[Dodaj-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Nowe — AzureQuickVM](./New-AzureQuickVM.md)

[Nowe — AzureVM](./New-AzureVM.md)

[Remove-AzureCertificate](./Remove-AzureCertificate.md)


