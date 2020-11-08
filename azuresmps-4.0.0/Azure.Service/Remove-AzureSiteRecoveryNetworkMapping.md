---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055076"
---
# Remove-AzureSiteRecoveryNetworkMapping

## STRESZCZENIe
Usuwa mapowanie sieci z magazynu odzyskiwania witryny.

## POLECENIA

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureSiteRecoveryNetworkMapping** usuwa mapowanie sieci z bieżącego magazynu usługi Azure Site Recovery.

## Przykłady

### Przykład 1: Usuwanie mapowania między siecią a siecią odzyskiwania
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryServer** .
Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.

Drugie polecenie uzyskuje mapowanie między siecią podstawową a siecią odzyskiwania, a następnie zapisuje je w zmiennej $NetworkMapping.
Polecenie Określa podstawowy serwer mapowania sieci jako pierwszy element $Servers.
To polecenie Określa serwer sieci odzyskiwania jako drugi element $Servers.

Polecenie ostatnie usuwa mapowanie sieci w $NetworkMapping.

### Przykład 2: Usuwanie mapowania między siecią a siecią maszyny wirtualnej platformy Azure
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu odzyskiwania witryny.
Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.

Drugie polecenie uzyskuje mapowanie między siecią podstawową a siecią maszyny wirtualnej Azure, a następnie zapisuje je w zmiennej $NetworkMapping.
Polecenie Określa serwer podstawowy dla sieci jako pierwszy element $Servers.
Polecenie określa parametr *platformy Azure* .
Dlatego polecenie uzyskuje mapowanie do sieci maszyny wirtualnej platformy Azure.

Polecenie ostatnie usuwa mapowanie sieci w $NetworkMapping.

## PARAMETRÓW

### -NetworkMapping
Określa mapowanie sieci, które ma zostać usunięte.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
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

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[Nowe — AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


