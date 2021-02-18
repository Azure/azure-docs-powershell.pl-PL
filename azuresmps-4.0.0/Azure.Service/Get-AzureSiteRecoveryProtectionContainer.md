---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405826"
---
# Get-AzureSiteRecoveryProtectionContainer

## SYNOPSIS
Pobiera kontenery ochrony dla magazynu odzyskiwania witryny.

## SKŁADNIA

### Domyślne (domyślne)
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzureSiteRecoveryProtectionContainer** pobiera kontenery ochrony dla bieżącego magazynu usługi Azure Site Recovery.
Kontener ochrony to kontener logiczny dla chronionych obiektów, takich jak maszyny wirtualne.
Zasady ochrony definiują ustawienia replikacji elementów chronionych i mogą być skojarzone z kontenerem ochrony i stosowane do chronionej jednostki.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie kontenerów chronionych
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

To polecenie pobiera kontenery chronione dla bieżącego magazynu.

## PARAMETERS

### — Identyfikator
Określa identyfikator chronionego kontenera do uzyskania.

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

### — Nazwa
Określa nazwę kontenera ochrony do uzyskania.

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

### — Profil
Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.
Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

## DANE WYJŚCIOWE

## NOTATKI

## LINKI POKREWNE




