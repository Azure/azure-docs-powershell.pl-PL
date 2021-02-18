---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180898"
---
# New-AzDataMigrationMongoDbCollectionSetting

## SYNOPSIS
Tworzy ustawienie kolekcji do migracji zgodnie z migracją mongoDb

## SKŁADNIA

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## OPIS
Polecenie New-AzDataMigrationMongoDbCollectionSetting cmdlet tworzy obiekt ustawień migracji określający zachowanie przepływności i usuwania.
Dane wyjściowe polecenia cmdlet to para wartości klucza z nazwą kolekcji i wartością ustawienia. Dane wyjściowe są używane podczas składania ustawień poziomu bazy danych w celu migracji.

## PRZYKŁADY

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

## PARAMETERS

### — Nazwa
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

### -Skey
Rozdzielona przecinkami lista klawiszy skrótów. W przypadku obiektu docelowego mongoDb możesz określić kolejność klucza sżdżu "Nazwa_klucza:Order", gdzie zamówienie ma wartość 1, -1 lub jest puste dla skrótu, na przykład "_id,email:-1".

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
Wartość jednostki dedykowanego żądania kolekcji. Jeśli nie jest ustawiona, ta kolekcja korzysta z udostępnionej bazy danych RU.

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

### -CanDelete
Czy dane docelowe powinny zostać usunięte, jeśli przełącznik jest ustawiony, podczas migracji zostaną one wyczyszczone

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## OUTPUTS

### Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting>

## NOTATKI

## LINKI POKREWNE
