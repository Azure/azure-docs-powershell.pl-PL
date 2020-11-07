---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: 5c53355daf364553accd4168f89d6bc1a3ccff03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705174"
---
# Backup-AzKeyVaultSecret

## STRESZCZENIe
Tworzy kopię zapasową klucza tajnego w magazynie kluczy.

## POLECENIA

### BySecretName (domyślny)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Backup-AzKeyVaultSecret** wykonuje kopię zapasową określonego klucza tajnego w magazynie kluczy, pobierając go i zapisując w pliku.
Jeśli istnieje wiele wersji klucza tajnego, wszystkie wersje są uwzględniane w kopii zapasowej.
Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza magazynem kluczy platformy Azure.
Kopię zapasową klucza tajnego można przywrócić w dowolnym magazynie kluczy subskrypcji, z której wykonano kopię zapasową.
Typowe przyczyny korzystania z tego polecenia cmdlet:
- Chcesz zalogować się do kopii klucza tajnego, aby mieć kopię w trybie offline na wypadek przypadkowego usunięcia klucza tajnego w magazynie kluczy.
- Dodałeś klucz tajny do magazynu kluczy i chcesz teraz sklonować ten klucz tajny do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej. Użyj polecenia cmdlet Backup-AzKeyVaultSecret, aby pobrać klucz tajny w szyfrowanym formacie, a następnie użyć polecenia cmdlet Restore-AzKeyVaultSecret i określić Magazyn kluczy w drugim regionie. (Należy pamiętać, że regiony muszą należeć do tej samej geograficznej lokalizacji).

## Przykłady

### Przykład 1: wykonywanie kopii zapasowej hasła za pomocą automatycznie generowanej nazwy pliku
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

To polecenie pobiera tajne imię o nazwie dbsecret z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego wpisu do pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.

### Przykład 2: wykonywanie kopii zapasowej hasła do określonej nazwy pliku, zastąpienie istniejącego pliku bez monitowania
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

To polecenie pobiera tajne hasło o nazwie vaultnamed MyKeyVault i zapisuje kopię zapasową tego klucza tajnego w pliku o nazwie Backup. blob.

### Przykład 3: wykonywanie kopii zapasowej uprzednio pobranej do określonej nazwy pliku
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

W tym poleceniu jest używana nazwa i nazwa magazynu obiektu $secret w celu pobrania klucza tajnego i zapisu jego kopii zapasowej w pliku o nazwie Backup. blob.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Monituje o potwierdzenie przed zastąpieniem pliku wyjściowego, jeśli ten plik istnieje.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Nie można utworzyć kopii zapasowej, która została przetworzona na podstawie danych wyjściowych rozmowy.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę klucza tajnego do wykonania kopii zapasowej.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plik_wyjściowy
Określa plik wyjściowy, w którym jest przechowywany obiekt BLOB kopii zapasowej.
Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje nazwę pliku.
Jeśli określisz nazwę istniejącego pliku wyjściowego, operacja nie zostanie ukończona i zwróci komunikat o błędzie informujący o tym, że plik kopii zapasowej już istnieje.

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
Określa nazwę magazynu kluczy zawierającego klucz tajny do wykonania kopii zapasowej.

```yaml
Type: System.String
Parameter Sets: BySecretName
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. platforming. models. PSKeyVaultSecretIdentityItem

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

