---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718929"
---
# New-AzureRmDataMigrationDatabaseInfo

## STRESZCZENIe
Tworzy obiekt DatabaseInfo dla usługi migracji bazy danych platformy Azure, która określa źródło bazy danych do migracji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## Opis
Polecenie cmdlet New-AzureRmDataMigrationDatabaseInfo tworzy obiekt DatabaseInfo, który określa wystąpienie źródłowej bazy danych, do której należy przeprowadzić migrację. Nazwa bazy danych jest pobierana jako parametr wejściowy.

## Przykłady

### Przykład 1
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

W powyższym przykładzie tworzony jest nowy obiekt DatabaseInfo dla źródłowej **AdventureWorks2016** bazy danych.

Ten skrypt zakłada, że użytkownik jest już zalogowany na koncie platformy Azure. Możesz potwierdzić stan logowania, korzystając z polecenia cmdlet Get-AzureSubscription.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
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

### -SourceDatabaseName
Nazwa źródłowej bazy danych.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
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

## WEJŚCIOWE

### Znaleziono


## WYSYŁA

### Microsoft. Azure. Management. datamigration. MODELES. DatabaseInfo


## INFORMACYJN

## LINKI POKREWNE


