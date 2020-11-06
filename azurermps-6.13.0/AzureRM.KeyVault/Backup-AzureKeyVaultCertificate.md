---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527937"
---
# Backup-AzureKeyVaultCertificate

## STRESZCZENIe
Wykonywanie kopii zapasowej certyfikatu w magazynie kluczy.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByCertificateName (domyślny)
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Backup-AzureKeyVaultCertificate** wykonuje kopię zapasową określonego certyfikatu w magazynie kluczy przez pobranie go i zapisanie go w pliku.
Jeśli certyfikat zawiera wiele wersji, wszystkie jego wersje zostaną uwzględnione w kopii zapasowej.
Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza magazynem kluczy platformy Azure.
Możesz przywrócić kopię zapasową certyfikatu do dowolnego magazynu kluczy w subskrypcji, z której wykonano kopię zapasową, o ile magazyn znajduje się w tej samej geograficznej platformie Azure.
Typowe przyczyny korzystania z tego polecenia cmdlet: 
- Chcesz zachować kopię certyfikatu w trybie offline na wypadek przypadkowego usunięcia oryginału z magazynu.
 
- Utworzono certyfikat przy użyciu magazynu kluczy, a teraz chcę sklonować obiekt do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.
Użyj polecenia cmdlet **Backup-AzureKeyVaultCertificate** , aby pobrać certyfikat w formacie zaszyfrowanym, a następnie użyj polecenia cmdlet **Restore-AzureKeyVaultCertificate** i określ Magazyn kluczy w drugim regionie.

## Przykłady

### Przykład 1. wykonywanie kopii zapasowej certyfikatu z automatycznie wygenerowaną nazwą pliku
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

To polecenie pobiera certyfikat o nazwie CERT z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego certyfikatu do pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.

### Przykład 2: wykonywanie kopii zapasowej certyfikatu pod określoną nazwą pliku
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

To polecenie pobiera certyfikat o nazwie CERT z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego certyfikatu do pliku o nazwie Backup. blob.

### Przykład 3: wykonywanie kopii zapasowej uprzednio pobranego certyfikatu do określonej nazwy pliku, zastępując plik docelowy bez monitowania.
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

To polecenie tworzy kopię zapasową certyfikatu o nazwie $cert. Nazwa w magazynie o nazwie $cert. Element magazynname do pliku o nazwie Backup. blob, w cichym zastępowaniu pliku, jeśli już istnieje.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Force
Zastąpienie danego pliku, jeśli istnieje

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

### -Inputobject
Nie można utworzyć kopii zapasowej, która została przetworzona na podstawie danych wyjściowych rozmowy.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa tajna.
Polecenie cmdlet tworzy nazwę FQDN wpisu tajnego na podstawie nazwy magazynu, obecnie wybranej nazwy środowiska i sekretu.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plik_wyjściowy
Plik wyjściowy.
Plik wyjściowy, w którym ma być przechowywana kopia zapasowa certyfikatu.
Jeśli nie podano tego parametru, zostanie wygenerowana domyślna nazwa pliku.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Magazynname
Nazwa magazynu.
Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIdentityItem
Parametry: Inputobject (ByValue)

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE
