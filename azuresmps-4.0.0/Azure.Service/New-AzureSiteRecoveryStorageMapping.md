---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054941"
---
# New-AzureSiteRecoveryStorageMapping

## STRESZCZENIe
Tworzy mapowanie między obiektem magazynu platformy Azure a obiektem magazynu odzyskiwania.

## POLECENIA

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureSiteRecoveryStorageMapping** tworzy mapowanie między obiektem magazynu podstawowego zarządzania witryną Azure i obiektem odzyskiwania.

## Przykłady

### Przykład 1. Tworzenie mapowania między obiektem magazynu a obiektem magazynu odzyskiwania
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryServer** .
Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.

Drugie polecenie pobiera magazyn odzyskiwania witryny dla pierwszego serwera w tablicy $Servers, a następnie przechowuje go w $Storages.

Ostatnie polecenie tworzy mapowanie między siecią podstawową a siecią odzyskiwania.
Polecenie Określa podstawowy obiekt magazynu jako pierwszy element $Storages.
Polecenie określa obiekt magazynu odzyskiwania jako drugi element $Storages.

## PARAMETRÓW

### -PrimaryStorage
Określa podstawowy magazyn do zamapowania na magazyn odzyskiwania.
Aby uzyskać obiekt **ASRStorage** , użyj polecenia cmdlet Get-AzureSiteRecoveryStorage.

```yaml
Type: ASRStorage
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

### -RecoveryStorage
Określa obiekt magazynu odzyskiwania.
To polecenie cmdlet mapuje obiekt magazynu podstawowego do obiektu magazynu, który określa ten parametr.
Aby uzyskać obiekt **ASRStorage** , użyj polecenie **Get-AzureSiteRecoveryStorage**.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
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

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[Get-AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[Remove-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


