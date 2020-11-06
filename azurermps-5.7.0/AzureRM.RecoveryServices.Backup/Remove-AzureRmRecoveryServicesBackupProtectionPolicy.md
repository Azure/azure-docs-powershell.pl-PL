---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/remove-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d687834c41f354897f64ca3300c7c8eaa47940b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526682"
---
# Remove-AzureRmRecoveryServicesBackupProtectionPolicy

## STRESZCZENIe
Usuwa zasady ochrony kopii zapasowej z magazynu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### PolicyName (domyślnie)
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Policyobject
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** usuwa zasady tworzenia kopii zapasowych dla magazynu.

Przed usunięciem zasad ochrony kopii zapasowej zasady nie mogą zawierać żadnych elementów kopii zapasowej.
Przed usunięciem zasad upewnij się, że każdy skojarzony element jest skojarzony z innymi zasadami.
Aby skojarzyć inne zasady z elementem kopii zapasowej, użyj polecenia cmdlet Enable-AzureRmRecoveryServicesBackupProtection.

Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.

## Przykłady

### Przykład 1: usuwanie zasad
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

Pierwsze polecenie uzyskuje zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w zmiennej $Pol.

Drugie polecenie usuwa obiekt zasady w $Pol.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę zasad ochrony kopii zapasowych, które należy usunąć.

```yaml
Type: String
Parameter Sets: PolicyName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Zwraca zasady, które mają zostać usunięte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policy
Określa zasady ochrony kopii zapasowej do usunięcia.
Aby uzyskać obiekt **BackupPolicy** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.

```yaml
Type: PolicyBase
Parameter Sets: PolicyObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PolicyBase
Parametr "Policy" przyjmuje wartość typu "PolicyBase" z rurociągu

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Nowe — AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Set-AzureRmRecoveryServicesBackupProtectionPolicy](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


