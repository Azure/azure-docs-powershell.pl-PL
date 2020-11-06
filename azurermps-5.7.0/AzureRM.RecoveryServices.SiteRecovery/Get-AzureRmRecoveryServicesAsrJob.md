---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 233a6a7c7fd7b2bfe96ed9cc0df6a88bdb9d8747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526657"
---
# Get-AzureRmRecoveryServicesAsrJob

## STRESZCZENIe
Pobiera szczegóły określonego zadania ASR lub listę ostatnich zadań ASR w magazynie usług Recovery Services.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ByParam (domyślny)
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByObject
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrJob** pobiera zadania odzyskiwania witryny Azure.
Za pomocą tego polecenia cmdlet można wyświetlać zadania ASR w magazynie usług Recovery Services.

## Przykłady

### Przykład 1
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

Zwraca wszystkie zadania określonego obiektu ASR (odwołanie do obiektu ASR, takiego jak replikowany element lub plan odzyskiwania) za pomocą identyfikatora. 

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

### -EndTime
Określa czas zakończenia zadań.
To polecenie cmdlet umożliwia pobieranie wszystkich zadań rozpoczętych przed określonym terminem.
Aby uzyskać obiekt **DateTime** dla tego parametru, użyj polecenia cmdlet Get-Date.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zadanie
Określa obiekt zadania ASR, dla którego mają zostać zaktualizowane szczegóły.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Określ zadanie ASR według nazwy.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Określa czas rozpoczęcia zadań.
To polecenie cmdlet umożliwia pobieranie wszystkich zadań uruchomionych po określonym czasie.

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
Określa stan zadania ASR.
To polecenie cmdlet umożliwia pobieranie wszystkich zadań zgodnych z określonym stanem.
Dopuszczalne wartości tego parametru to:

- NotStarted
- W trakcie
- Doszło
- Pozostałe
- Nie powiodło się
- Anulowania
- Zawiesin

```yaml
Type: String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
Określa identyfikator obiektu. Umożliwia wyszukiwanie zadań na określonym obiekcie.

```yaml
Type: String
Parameter Sets: ByParam
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## WYSYŁA

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]

## INFORMACYJN

## LINKI POKREWNE

[Restart-AzureRmRecoveryServicesAsrJob](./Restart-AzureRmRecoveryServicesAsrJob.md)

[Życiorys — AzureRmRecoveryServicesAsrJob](./Resume-AzureRmRecoveryServicesAsrJob.md)

[Zatrzymaj — AzureRmRecoveryServicesAsrJob](./Stop-AzureRmRecoveryServicesAsrJob.md)
