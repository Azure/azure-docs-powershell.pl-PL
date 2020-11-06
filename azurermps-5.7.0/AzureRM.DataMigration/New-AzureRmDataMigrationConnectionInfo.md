---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528150"
---
# New-AzureRmDataMigrationConnectionInfo

## STRESZCZENIe
Tworzy nowy obiekt informacji o połączeniu określający typ serwera i nazwę dla połączenia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## Opis
Polecenie cmdlet New-AzureRmDataMigrationConnectionInfo służy do tworzenia nowego obiektu informacji o połączeniu określającego typ serwera dla połączenia. 



## Przykłady

### Przykład 1
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
W powyższym przykładzie tworzony jest nowy obiekt informacji o połączeniu, który udostępnia parametry SQL jako parametr ServerType.


## PARAMETRÓW

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

### -ServerType
Wyliczenie opisujące typ serwera, z którym ma zostać nawiązane połączenie. Obecnie obsługiwane są wartości SQL dla programu SQL Server i SQLDB dla bazy danych SQL Azure. 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -AuthType
Typ uwierzytelniania, który ma być używany do połączeń. Możliwe wartości to sqlauthentication and WindowsAuthentication

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataSource
Serwer address\name, z którym chcesz się połączyć. 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustServerCertificate
Wartość logiczna wskazująca na zagwarantowanie, że szyfrowanie ma miejsce.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

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

### Microsoft. Azure. Management. datamigration. MODELES. ConnectionInfo


## INFORMACYJN

## LINKI POKREWNE

