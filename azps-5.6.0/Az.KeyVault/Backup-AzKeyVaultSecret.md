---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: ae60c2d10c8b186db22fb9fc9cd0a1e66aa1c07d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962010"
---
# Backup-AzKeyVaultSecret

## SYNOPSIS
Kopię zapasową klucza tajnego w magazynie kluczy.

## SKŁADNIA

### BySecretName (Default)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Backup-AzKeyVaultSecret** kopii zapasowej określonego klucza tajnego jest kopią zapasową w magazynie kluczy, pobierając ją i przechowując w pliku.
Jeśli istnieje wiele wersji tajnych, wszystkie wersje są uwzględniane w kopii zapasowej.
Pobrana zawartość jest zaszyfrowana, więc nie można jej używać poza magazynem kluczy platformy Azure.
Kopię zapasową klucza tajnego możesz przywrócić do dowolnego magazynu kluczy w subskrypcji, z których została wyzowana jego kopii zapasowej.
Typowe powody, dla których należy używać tego polecenia cmdlet, to:
- Chcesz usunąć kopię klucza tajnego, aby mieć kopię w trybie offline na wypadek przypadkowego usunięcia klucza tajnego w twoim magazynie kluczy.
- Dodano klucz tajny do magazynu kluczy i teraz chcesz sklonować klucz tajny w innym regionie platformy Azure, aby można było jej używać ze wszystkich wystąpień aplikacji rozproszonej. Użyj Backup-AzKeyVaultSecret cmdlet, aby pobrać klucz tajny w zaszyfrowanym formacie, a następnie użyj polecenia cmdlet Restore-AzKeyVaultSecret i określ magazyn kluczy w drugim regionie. (Regiony muszą należeć do tej samej lokalizacji geograficznej).

## PRZYKŁADY

### Przykład 1. Tworzy kopię zapasową sekretu przy użyciu automatycznie wygenerowanej nazwy pliku
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

To polecenie pobiera klucz tajny o nazwie MySecret z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza tajnego w automatycznie nazwanym pliku i wyświetla nazwę pliku.

### Przykład 2. Kopii zapasowej tajnej nazwy pliku z podaną nazwą pliku, która nie wyświetla monitu o nadpisanie istniejącego pliku
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

To polecenie pobiera klucz tajny o nazwie MySecret z magazynu klucza o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza tajnego w pliku o nazwie Backup.blob.

### Przykład 3. Kopii zapasowej poprzednio pobranej informacji tajnej do określonej nazwy pliku
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

To polecenie używa nazwy i $secret magazynu obiektu w celu pobrania informacji tajnych i zapisania jego kopii zapasowej w pliku o nazwie Backup.blob.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — Wymuszanie
Wyświetla monit o potwierdzenie przed nadpisaniem pliku wyjściowego, jeśli istnieje.

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

### -InputObject
Tajna, aby mieć kopię zapasową, potokowana na wyniku połączenia pobierania.

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

### — Nazwa
Określa nazwę tajnych kopii zapasowej.

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

### -OutputFile
Określa plik wyjściowy, w którym jest przechowywany obiekt blob kopii zapasowej.
Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje nazwę pliku.
Jeśli określisz nazwę istniejącego pliku wyjściowego, operacja nie zostanie ukończona i zostanie wyświetlony komunikat o błędzie informujący, że plik kopii zapasowej już istnieje.

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

### -VaultName
Określa nazwę magazynu kluczy zawierającego klucz tajny do kopii zapasowej.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## DANE WYJŚCIOWE

### System.String

## NOTATKI

## LINKI POKREWNE

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

