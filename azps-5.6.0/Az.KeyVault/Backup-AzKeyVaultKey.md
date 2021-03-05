---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 3123d0fa188e0e9a4c419ceaa567969fc3a2f8b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977018"
---
# Backup-AzKeyVaultKey

## SYNOPSIS
Kopię zapasową klucza w magazynie kluczy.

## SKŁADNIA

### ByKeyName (Domyślna)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmByKeyName
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Backup-AzKeyVaultKey** kopii zapasowej określonego klucza w magazynie kluczy, pobierając go i przechowując w pliku.
Jeśli istnieje wiele wersji klucza, wszystkie wersje są uwzględniane w kopii zapasowej.
Pobrana zawartość jest zaszyfrowana, więc nie można jej używać poza magazynem kluczy platformy Azure.
Możesz przywrócić klucz kopii zapasowej do dowolnego magazynu kluczy w subskrypcji, z których została utworzyć kopię zapasową.
Typowe powody, dla których należy używać tego polecenia cmdlet, to: 
- Chcesz usunąć kopię klucza, aby mieć kopię w trybie offline na wypadek przypadkowego usunięcia klucza w magazynie kluczy.
 
- Klucz został utworzony przy użyciu magazynu kluczy, a teraz chcesz go sklonować w innym regionie platformy Azure, aby można było go używać ze wszystkich wystąpień aplikacji rozproszonej.
Użyj polecenia cmdlet **Backup-AzKeyVaultKey,** aby pobrać klucz w postaci zaszyfrowanej, a następnie użyj polecenia cmdlet Restore-AzKeyVaultKey i określ magazyn kluczy w drugim regionie.

## PRZYKŁADY

### Przykład 1. Tworzy kopię zapasową klucza z automatycznie wygenerowaną nazwą pliku
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

To polecenie pobiera klucz o nazwie MyKey z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza w pliku, który jest automatycznie nazwany dla Ciebie, i wyświetla nazwę pliku.

### Przykład 2. Kopii zapasowej klucza pod określoną nazwą pliku
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

To polecenie pobiera klucz o nazwie MyKey z klucza o nazwie MyKeyVault i zapisuje kopię zapasową tego klucza w pliku o nazwie Backup.blob.

### Przykład 3. Kopię zapasową poprzednio pobranego klucza do określonej nazwy pliku i nadpisanie pliku docelowego bez monitu.
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

To polecenie tworzy kopię zapasową klucza o nazwie $key. Nazwa w magazynie o nazwie $key. Nazwa magazynu do pliku o nazwie Backup.blob, bezgłośnie nadpisując plik, jeśli już istnieje.

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
Zastępowanie danego pliku, jeśli istnieje

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

### -HsmName
Nazwa HSM. Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Key bundle to back up, pipelined in from the output of a retrieval call.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę klucza do kopii zapasowej.

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

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
Określa nazwę magazynu kluczy zawierającego klucz do kopii zapasowej.

```yaml
Type: System.String
Parameter Sets: ByKeyName
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## DANE WYJŚCIOWE

### System.String

## NOTATKI

## LINKI POKREWNE

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Restore-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

