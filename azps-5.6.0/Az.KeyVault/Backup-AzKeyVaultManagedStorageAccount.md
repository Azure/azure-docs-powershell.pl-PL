---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 75f5e487c7cb1d434d12d6c02122991195c01066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991145"
---
# Backup-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Kopii zapasowej konta magazynu zarządzanego przez usługę KeyVault.

## SKŁADNIA

### ByStorageAccountName (Domyślna)
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Backup-AzKeyVaultManagedStorageAccount** kopii zapasowej określonego zarządzanego konta magazynu w magazynie kluczy przez pobranie go i przechowywanie w pliku.
Pobrana zawartość jest zaszyfrowana, więc nie można jej używać poza magazynem kluczy platformy Azure.
Możesz przywrócić kopię zapasową konta magazynu do dowolnego magazynu kluczy w subskrypcji, z których została ona zbędna, o ile magazyn znajduje się w tej samej lokalizacji geograficznej platformy Azure.
Typowe powody, dla których należy używać tego polecenia cmdlet, to: 
- Chcesz zachować kopię offline konta magazynu na wypadek przypadkowego usunięcia oryginału z magazynu.
 
- Utworzono konto magazynu zarządzanego przy użyciu magazynu kluczy, a teraz chcesz sklonować obiekt w inny region platformy Azure, aby można było używać go ze wszystkich wystąpień aplikacji rozproszonej.
Użyj polecenia cmdlet **Backup-AzKeyVaultManagedStorageAccount,** aby pobrać konto magazynu zarządzanego w postaci zaszyfrowanej, a następnie użyj polecenia cmdlet **Restore-AzKeyVaultManagedStorageAccount** i określ magazyn kluczy w drugim regionie.

## PRZYKŁADY

### Przykład 1. Tworzy kopię zapasową zarządzanego konta magazynu z automatycznie wygenerowaną nazwą pliku
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

To polecenie pobiera konto magazynu zarządzanego o nazwie MyMSAK z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego zarządzanego konta magazynu w pliku, który jest automatycznie nazwany dla Ciebie, i wyświetla nazwę pliku.

### Przykład 2. Kopii zapasowej zarządzanego konta magazynu pod określoną nazwą pliku
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

To polecenie pobiera konto magazynu zarządzanego o nazwie MyMSAK z magazynu kluczy o nazwie MyKeyVault i zapisuje kopię zapasową tego zarządzanego konta magazynu w pliku o nazwie Backup.blob.

### Przykład 3. Kopię zapasową poprzednio pobranego zarządzanego konta magazynu pod określoną nazwą pliku i nadpisanie pliku docelowego bez monitu.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

To polecenie tworzy kopię zapasową zarządzanego konta magazynu o nazwie $msak. Nazwa w magazynie o nazwie $msak. Nazwa magazynu do pliku o nazwie Backup.blob, bezgłośnie nadpisując plik, jeśli już istnieje.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -InputObject
Pakiet konta magazynu, który ma zostać kopii zapasowej, potokowany z danych wyjściowych połączenia pobierania.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Tajna nazwa.
Polecenie cmdlet konstruuje nazwę FQDN tajemnicy przed nazwą magazynu, obecnie wybranym środowiskiem i nazwą tajną.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Plik wyjściowy.
Plik wyjściowy do przechowywania kopii zapasowej konta magazynu.
Jeśli nie zostanie określona, zostanie wygenerowana domyślna nazwa pliku.

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
Nazwa magazynu.
Polecenie cmdlet tworzy nazwę FQDN magazynu na podstawie nazwy i obecnie wybranego środowiska.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## DANE WYJŚCIOWE

### System.String

## NOTATKI

## LINKI POKREWNE
