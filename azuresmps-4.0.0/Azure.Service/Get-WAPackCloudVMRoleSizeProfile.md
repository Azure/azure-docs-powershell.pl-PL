---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055474"
---
# Get-WAPackCloudVMRoleSizeProfile

## STRESZCZENIe
Pobiera obiekty profilu rozmiaru roli maszyny wirtualnej chmury.

## POLECENIA

### Empty (domyślnie)
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Odname
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-WAPackCloudVMRoleSizeProfile** Pobiera obiekty profilu rozmiaru roli maszyny wirtualnej w chmurze dla maszyn wirtualnych.

## Przykłady

### Przykład 1: uzyskiwanie profilu rozmiaru roli maszyny wirtualnej w chmurze przy użyciu nazwy
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

To polecenie pobiera profil rozmiaru o nazwie małe.

### Przykład 2: uzyskiwanie wszystkich profilów rozmiaru roli maszyny wirtualnej w chmurze
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

To polecenie pobiera wszystkie profile rozmiaru.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę profilu rozmiaru roli maszyny wirtualnej w chmurze.

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Get-WAPackVM](./Get-WAPackVM.md)


