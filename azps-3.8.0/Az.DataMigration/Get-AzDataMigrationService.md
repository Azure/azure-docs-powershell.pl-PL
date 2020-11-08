---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051536"
---
# Get-AzDataMigrationService

## STRESZCZENIe
Pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych platformy Azure. 

## POLECENIA

### ResourceGroupSet (domyślny)
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ServiceNameGroupSet
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzDataMigrationService pobiera właściwości skojarzone z wystąpieniem usługi migracji bazy danych platformy Azure na podstawie nazwy usługi i nazwy grupy zasobów platformy Azure jako parametrów wejściowych. 

## Przykłady

### Przykład 1
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

Powyższy przykład pobiera właściwości wystąpienia usługi migracji bazy danych platformy Azure o nazwie testService. 

### Przykład 2
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

Powyższy przykład pobiera usługi migracji bazy danych platformy Azure w grupie zasobów o nazwie testResourceGroup. 

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa usługi migracji bazy danych.

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu DataMigrationService.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService

## INFORMACYJN

## LINKI POKREWNE
