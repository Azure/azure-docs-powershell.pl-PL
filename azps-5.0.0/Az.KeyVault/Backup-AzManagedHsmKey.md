---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304626"
---
# Backup-AzManagedHsmKey

## STRESZCZENIe
Wykonywanie kopii zapasowej klucza w zarządzanym modułu HSM.

## POLECENIA

### ByKeyName (domyślny)
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Backup-AzManagedHsmKey** wykonuje kopię zapasową określonego klucza w zarządzanym modułu HSM przez pobranie go i zapisanie go w pliku.
Jeśli istnieje wiele wersji klucza, wszystkie wersje są uwzględniane w kopii zapasowej.
Ponieważ pobrana zawartość jest szyfrowana, nie można jej użyć poza oknem HSM zarządzanym na platformie Azure.
Klucz kopii zapasowej można przywrócić do dowolnego zarządzanego modułu HSM w subskrypcji, z której wykonano kopię zapasową.
Typowe przyczyny korzystania z tego polecenia cmdlet: 
- Chcesz zalogować się do kopii klucza, aby uzyskać kopię w trybie offline, na wypadek przypadkowego usunięcia klucza z zarządzanego modułu HSM.
 
- Utworzono klucz przy użyciu zarządzanego modułu HSM i teraz chcę sklonować klucz do innego obszaru platformy Azure, aby można go było używać we wszystkich wystąpieniach aplikacji rozproszonej.
Użyj polecenia cmdlet **Backup-AzManagedHsmKey** , aby pobrać klucz w zaszyfrowanym formacie, a następnie użyj polecenia cmdlet Restore-AzManagedHsmKey i określeniu zarządzanego modułu HSM w drugim regionie.

## Przykłady

### Przykład 1. Tworzenie kopii zapasowej klucza z automatycznie wygenerowaną nazwą pliku
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

To polecenie pobiera klucz o nazwie TestKey z zarządzanego modułu HSM o nazwie testmhsm i zapisuje kopię zapasową tego klucza w pliku, którego nazwa jest automatycznie nazywana, i wyświetla nazwę pliku.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -HsmName
Nazwa modułu HSM. Polecenie cmdlet tworzy nazwę FQDN zarządzanego modułu HSM na podstawie nazwy i obecnie wybranego środowiska.

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

### -Inputobject
Kluczowy pakiet do utworzenia kopii zapasowej, który połączył się z wyników rozmowy o pobraniu.

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

### -Name (nazwa)
Nazwa klucza.
Polecenie cmdlet tworzy nazwę FQDN klucza na podstawie nazwa zarządzanego modułu HSM, obecnie wybranego środowiska i nazwy klucza.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plik_wyjściowy
Plik wyjściowy.
Plik wyjściowy, w którym ma zostać zapisany obiekt BLOB klucza kopii zapasowej.
Jeśli nie jest obecny, wybierana jest domyślna nazwa pliku.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. platforming. models. PSKeyVaultKeyIdentityItem

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzManagedHsmKey](./Add-AzManagedHsmKey.md)

[Get-AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[Remove-AzManagedHsmKey](./Remove-AzManagedHsmKey.md)

[Cofanie — AzManagedHsmKeyRemoval](./Undo-AzManagedHsmKeyRemoval.md)

[Update-AzManagedHsmKey](./Update-AzManagedHsmKey.md)

[Restore-AzManagedHsmKey](./Restore-AzManagedHsmKey.md)