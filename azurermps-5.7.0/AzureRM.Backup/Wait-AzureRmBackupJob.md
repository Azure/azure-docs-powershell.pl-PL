---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/wait-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: ce44ac04914419fa2551062b28108abeca9d4249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719578"
---
# Wait-AzureRmBackupJob

## STRESZCZENIe
Oczekuje na zakończenie zadania kopii zapasowej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **wait-AzureRmBackupJob** oczekuje na zakończenie zadania kopii zapasowej Azure.
Zadania tworzenia kopii zapasowej mogą trwać długo.
Jeśli uruchomisz zadanie kopii zapasowej w ramach skryptu, możesz wymusić, że skrypt będzie czekał na zakończenie zadania, zanim przełączy się do innych zadań.

Skrypt zawierający to polecenie cmdlet może być łatwiejszy niż ten, który sonduje usługę kopii zapasowej dla stanu zadania.

## Przykłady

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

### — Zadanie
Określa zadanie, które zostanie anulowane przez to polecenie cmdlet.
Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TimeOut
Określa maksymalny czas (w sekundach) oczekiwania na zakończenie zadania.
Zalecamy określenie wartości limitu czasu.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### AzureRmBackupJob

## WYSYŁA

### AzureRmBackupJob[]

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Zatrzymaj — AzureRmBackupJob](./Stop-AzureRmBackupJob.md)


