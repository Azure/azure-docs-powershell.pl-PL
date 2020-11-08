---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054549"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## STRESZCZENIe
Pobiera plan odzyskiwania witryny Azure w formacie XML.

## POLECENIA

### ByRPObject (domyślny)
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureSiteRecoveryRecoveryPlanFile** pobiera plan odzyskiwania witryny Azure w formacie XML.
Za pomocą tego pliku można zaktualizować plan odzyskiwania, a następnie przekazać go do serwera odzyskiwania witryny.

Plan odzyskiwania umożliwia zbieranie maszyn wirtualnych w grupie w celu przejęcia awaryjnego i odzyskiwania.

## Przykłady

### Przykład 1: Pobieranie pliku planu odzyskiwania
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

To polecenie korzysta z polecenia cmdlet **Get-AzureSiteRecoveryRecoveryPlan** w celu pobrania planu odzyskiwania, a następnie zapisu go w zmiennej $RecoveryPlan.

Drugie polecenie używa polecenia cmdlet **GetAzureSiteRecoveryRecoveryPlanFile** , aby uzyskać plik XML planu odzyskiwania witryny w $RecoveryPlan.
Polecenie zapisuje plik XML w określonej ścieżce.

## PARAMETRÓW

### -ID
Określa identyfikator planu odzyskiwania, który ma zostać wyświetlony.

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

### -Path
Określa pełną ścieżkę do przechowywania pliku XML planu odzyskiwania.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -RecoveryPlan
Określa obiekt **ASRRecoveryPlan** , z którego należy pobrać plan odzyskiwania.
Aby uzyskać obiekt **ASRRecoveryPlan** , użyj polecenia cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


