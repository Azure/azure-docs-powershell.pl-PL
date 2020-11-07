---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: b71c9a5da3c89916b18bdb5446f311e3d71615bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894361"
---
# Get-AzRecoveryServicesAsrJob

## STRESZCZENIe
Pobiera szczegóły określonego zadania ASR lub listę ostatnich zadań ASR w magazynie usług Recovery Services.

## POLECENIA

### ByParam (domyślny)
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzRecoveryServicesAsrJob** pobiera zadania odzyskiwania witryny Azure.
Za pomocą tego polecenia cmdlet można wyświetlać zadania ASR w magazynie usług Recovery Services.

## Przykłady

### Przykład 1
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

Zwraca wszystkie zadania określonego obiektu ASR (odwołanie do obiektu ASR, takiego jak replikowany element lub plan odzyskiwania) za pomocą identyfikatora. 

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

### -EndTime
Określa czas zakończenia zadań.
To polecenie cmdlet umożliwia pobieranie wszystkich zadań rozpoczętych przed określonym terminem.
Aby uzyskać obiekt **DateTime** dla tego parametru, użyj polecenia cmdlet Get-Date.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
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
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
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
Type: System.String
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
Type: System.Nullable`1[System.DateTime]
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
Type: System.String
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
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## WYSYŁA

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## INFORMACYJN

## LINKI POKREWNE

[Restart-AzRecoveryServicesAsrJob](./Restart-AzRecoveryServicesAsrJob.md)

[Życiorys — AzRecoveryServicesAsrJob](./Resume-AzRecoveryServicesAsrJob.md)

[Zatrzymaj — AzRecoveryServicesAsrJob](./Stop-AzRecoveryServicesAsrJob.md)
