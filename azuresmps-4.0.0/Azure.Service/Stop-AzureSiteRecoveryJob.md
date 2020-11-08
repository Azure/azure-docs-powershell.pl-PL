---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055373"
---
# Stop-AzureSiteRecoveryJob

## STRESZCZENIe
Zatrzymuje zadanie odzyskiwania witryny.

## POLECENIA

### ByObject (domyślny)
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **stop-AzureSiteRecoveryJob** zatrzymuje zadanie odzyskiwania witryny Azure.

## Przykłady

### Przykład 1. Zatrzymaj wszystkie zadania
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

Pierwsze polecenie pobiera zadania odzyskiwania witryny Azure dla bieżącego magazynu usługi Azure Site Recovery przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryJob** , a następnie zapisuje wyniki w zmiennej $jobs.

Drugie polecenie zatrzymuje zadania określone przez $Jobs.

## PARAMETRÓW

### -ID
Określa identyfikator zadania, które ma zostać zatrzymane.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zadanie
Określa zadanie, które ma zostać zatrzymane.

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

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
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

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureSiteRecoveryJob](./Get-AzureSiteRecoveryJob.md)

[Restart-AzureSiteRecoveryJob](./Restart-AzureSiteRecoveryJob.md)

[Życiorys — AzureSiteRecoveryJob](./Resume-AzureSiteRecoveryJob.md)


