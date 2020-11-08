---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051523"
---
# New-AzDataMigrationConnectionInfo

## STRESZCZENIe
Tworzy nowy obiekt informacji o połączeniu określający typ serwera i nazwę dla połączenia.

## POLECENIA

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet New-AzDataMigrationConnectionInfo służy do tworzenia nowego obiektu informacji o połączeniu określającego typ serwera dla połączenia. 

## Przykłady

### Przykład 1
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

W powyższym przykładzie tworzony jest nowy obiekt informacji o połączeniu, który udostępnia parametry SQL jako parametr ServerType.

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

### -ServerType
Wyliczenie opisujące typ serwera, z którym ma zostać nawiązane połączenie. Obecnie obsługiwane wartości to SQL dla programu SQL Server, wystąpienia zarządzanego SQL Azure, MongoDb, CosmosDb i Azure SQL Database. 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
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

### Microsoft. Azure. Management. datamigration. MODELES. ConnectionInfo

## INFORMACYJN

## LINKI POKREWNE
