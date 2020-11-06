---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522934"
---
# Start-AzsStorageContainerMigration

## STRESZCZENIe
Rozpoczyna zadanie migracji kontenera w celu migrowania kontenerów do określonego udziału docelowego.

## POLECENIA

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Rozpoczyna zadanie migracji kontenera w celu migrowania kontenerów do określonego udziału docelowego.

## Przykłady

### --------------------------PRZYKŁAD 1--------------------------
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

Rozpoczynanie migracji kontenera.

## PARAMETRÓW

### -AsJob
Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationShareUncPath
Ścieżka UNC udziału docelowego do migracji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Farmname
Identyfikator farmy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Nie pytaj o potwierdzenie.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa kontenera, który ma zostać zmigrowany.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów, w której zarejestrowano dostawcę zasobów magazynu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nazwa_udziału
Nazwa udziału zawierającego kontener określony do migracji.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Nazwa konta magazynu, w którym znajduje się kontener.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

