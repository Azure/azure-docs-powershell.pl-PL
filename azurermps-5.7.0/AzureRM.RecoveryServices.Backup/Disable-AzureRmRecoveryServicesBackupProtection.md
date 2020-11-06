---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7235c70eae1ab7b93340e68bbb705c17b74c3408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526734"
---
# Disable-AzureRmRecoveryServicesBackupProtection

## STRESZCZENIe
Wyłącza ochronę elementu chronionego kopią zapasową.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **disable-AzureRmRecoveryServicesBackupProtection** wyłącza ochronę elementu chronionego usługą Kopia zapasowa Azure.
To polecenie cmdlet zatrzymuje regularne Planowanie kopii zapasowej elementu.
To polecenie cmdlet umożliwia również usunięcie istniejących punktów odzyskiwania dla elementu kopii zapasowej.

Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.

## Przykłady

### Przykład 1: Wyłączanie ochrony przed kopiami zapasowymi
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

Pierwsze polecenie uzyskuje tablicę kontenerów kopii zapasowych, a następnie zapisuje je w tablicy $Cont.

Drugie polecenie pobiera element kopii zapasowej odpowiadający pierwszemu kontenerowi, a następnie zapisuje go w zmiennej $PI.

Ostatnie polecenie wyłącza ochronę kopii zapasowych elementu w $PI \[ 0 \] , ale zachowuje dane.

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

### -Item
Określa element kopii zapasowej, dla którego to polecenie cmdlet wyłącza ochronę.
Aby uzyskać **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupItem.

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RemoveRecoveryPoints
Wskazuje, że to polecenie cmdlet usuwa istniejące punkty odzyskiwania.
Aby później usunąć zapisane punkty odzyskiwania, uruchom ponownie to polecenie cmdlet i określ ten parametr.

```yaml
Type: SwitchParameter
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

### ItemBase
Parametr "element" akceptuje wartość typu "ItemBase" z potoku

## WYSYŁA

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase

## INFORMACYJN

## LINKI POKREWNE

[Enable-AzureRmRecoveryServicesBackupProtection](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[Get-AzureRmRecoveryServicesBackupContainer](./Get-AzureRmRecoveryServicesBackupContainer.md)

[Get-AzureRmRecoveryServicesBackupItem](./Get-AzureRmRecoveryServicesBackupItem.md)


