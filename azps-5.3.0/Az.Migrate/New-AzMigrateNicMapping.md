---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385772"
---
# New-AzMigrateNicMapping

## STRESZCZENIe
Umożliwia utworzenie obiektu w celu zaktualizowania właściwości karty sieciowej serwera replikacji.

## POLECENIA

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet New-AzMigrateNicMapping tworzy mapowanie źródłowej karty sieciowej podłączonej do serwera, który ma zostać zmigrowany.
Ten obiekt jest dostarczany jako wejście do polecenia cmdlet Set-AzMigrateServerReplication w celu zaktualizowania karty NIC i jej właściwości dla serwera replikowanego.

## Przykłady

### Przykład 1. Tworzenie obiektu karty interfejsu sieciowego
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

Tworzy obiekt aktualizacji karty sieciowej.

## PARAMETRÓW

### -NicID
Określa identyfikator karty sieciowej, która ma zostać zaktualizowana.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicIP
Określa adres IP w podsieci docelowej, który ma być wykorzystywany przez kartę NIC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicSelectionType
Określa, czy karta sieciowa do zaktualizowania będzie podstawowa, pomocnicza, czy nie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicSubnet
Określa nazwę podsieci dla karty sieciowej w docelowej sieci wirtualnej, do której należy przeprowadzić migrację serwera.

```yaml
Type: System.String
Parameter Sets: (All)
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

## WYSYŁA

### Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IVMwareCbtNicInput

## INFORMACYJN

PISUJE

## LINKI POKREWNE

