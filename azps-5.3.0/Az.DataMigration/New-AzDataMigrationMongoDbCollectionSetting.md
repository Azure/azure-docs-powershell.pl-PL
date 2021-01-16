---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387564"
---
# New-AzDataMigrationMongoDbCollectionSetting

## STRESZCZENIe
Umożliwia utworzenie ustawienia kolekcji dla migracji zgodnie z migracją mongoDb.

## POLECENIA

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## Opis
Polecenie cmdlet New-AzDataMigrationMongoDbCollectionSetting tworzy obiekt ustawienia migracji, który określa przepływność i zachowanie usuwania.
Dane wyjściowe polecenie cmdlet to para wartości klucza z nazwą kolekcji oraz wartością ustawienia. Wyniki są używane w asemblerze ustawień poziomu bazy danych do migracji.

## Przykłady

### Przykład 1
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## PARAMETRÓW

### -Name (nazwa)
Nazwa kolekcji

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShardKey
Lista rozdzielanych przecinkami kluczy Shard. W przypadku elementu docelowego mongoDb można określić kolejność kluczy Shard "ShardKeyName: Order", gdzie LP jest 1,-1 lub pusta w celu utworzenia skrótu, na przykład "_id, poczta e-mail:-1".

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

### -TargetRequestUnit
Dedykowana wartość jednostki żądania kolekcji. Jeśli ta funkcja nie jest ustawiona, kolekcja używa współużytkowanej bazy danych RU.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Usuń
Czy chcesz, aby dane docelowe były usuwane, jeśli przełącznik jest ustawiony, zostanie oczyszczony po migracji.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. datamigration. MODELES. MongoDbCollectionSetting>

## INFORMACYJN

## LINKI POKREWNE
