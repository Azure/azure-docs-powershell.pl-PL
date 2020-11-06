---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: 2eecb6d4bb069b1578b3080c04de4c9df1e42f09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542576"
---
# Backup-AzureKeyVaultKey

## STRESZCZENIe
Wykonywanie kopii zapasowej klucza w magazynie kluczy.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByKeyName (domyślny)
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Backup-AzureKeyVaultKey** wykonuje kopię zapasową określonego klucza w magazynie kluczy przez pobranie go i zapisanie go w pliku.
Jeśli istnieje wiele wersji klucza, wszystkie wersje są uwzględniane w kopii zapasowej.
Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza magazynem kluczy platformy Azure.
Klucz kopii zapasowej można przywrócić w dowolnym magazynie kluczy subskrypcji, z której wykonano kopię zapasową.

Typowe przyczyny korzystania z tego polecenia cmdlet: 

- Chcesz zalogować się do kopii klucza, aby uzyskać kopię w trybie offline, na wypadek przypadkowego usunięcia klucza w magazynie kluczy.
 
- Utworzono klucz za pomocą magazynu kluczy, a teraz chcę sklonować klucz do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.
Użyj polecenia cmdlet **Backup-AzureKeyVaultKey** , aby pobrać klucz w zaszyfrowanej formie, a następnie użyj polecenia cmdlet Restore-AzureKeyVaultKey i określ Magazyn kluczy w drugim regionie.

## Przykłady

### Przykład 1. Tworzenie kopii zapasowej klucza z automatycznie wygenerowaną nazwą pliku
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

To polecenie pobiera klucz o nazwie MyKey z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza w pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.

### Przykład 2: wykonywanie kopii zapasowej klucza na określonej nazwie pliku
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

To polecenie pobiera klucz o nazwie MyKey z klucza vaultnamed MyKeyVault i zapisuje kopię zapasową tego klucza do pliku o nazwie Backup. blob.

### Przykład 3: wykonywanie kopii zapasowej uprzednio pobranego klucza do określonej nazwy pliku, zastępując plik docelowy bez monitowania.
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

To polecenie tworzy kopię zapasową klucza o nazwie $key. Nazwa w magazynie o nazwie $key. Element magazynname do pliku o nazwie Backup. blob, w cichym zastępowaniu pliku, jeśli już istnieje.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Force
Zastąpienie danego pliku, jeśli istnieje

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Inputobject
Kluczowy pakiet do utworzenia kopii zapasowej, który połączył się z wyników rozmowy o pobraniu.

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę klucza, którego kopię zapasową należy wykonać.

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plik_wyjściowy
Określa plik wyjściowy, w którym jest przechowywany obiekt BLOB kopii zapasowej.
Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje nazwę pliku.
Jeśli określisz nazwę istniejącego pliku wyjściowego, operacja nie zostanie ukończona i zwróci komunikat o błędzie informujący o tym, że plik kopii zapasowej już istnieje.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Magazynname
Określa nazwę magazynu kluczy zawierającego klucz do utworzenia kopii zapasowej.

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Ciąg
Polecenie cmdlet zwraca ścieżkę pliku wyjściowego zawierającego kopię zapasową klucza.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Restore-AzureKeyVaultKey](./Restore-AzureKeyVaultKey.md)

