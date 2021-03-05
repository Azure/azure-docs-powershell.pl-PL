---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: a1f5c89b33ad4d547907bd63427a45ef262518c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011953"
---
# Get-AzMySqlFlexibleServerConnectionString

## SYNOPSIS
Pobierz parametrów połączenia według dostawcy połączenia klienta.

## SKŁADNIA

### Pobierz (domyślne)
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## OPIS
Pobierz parametrów połączenia według dostawcy połączenia klienta.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie parametrów połączenia według nazwy
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

To polecenie cmdlet wyświetla ciąg połączenia klienta według nazwy serwera.

### Przykład 2. Uzyskiwanie parametrów połączenia serwera MySql według tożsamości
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

To polecenie cmdlet pobiera ciąg połączenia serwera MySql według tożsamości.

## PARAMETERS

### —Klient
Dostawca połączenia klienta.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Serwer parametrów połączenia.
Aby skonstruować, zobacz sekcję NOTES, aby uzyskać informacje o właściwościach INPUTOBJECT i utworzyć tabelę skrótu.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa serwera.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów zawierającej zasób. Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SubscriptionId
Identyfikator subskrypcji identyfikujący subskrypcję platformy Azure.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.MySql.Models.IMySqlIdentity

## DANE WYJŚCIOWE

### System.String

## NOTATKI

ALIASY

ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW

Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości. Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.


INPUTOBJECT: <IMySqlIdentity> Serwer parametrów połączenia.
  - `[ConfigurationName <String>]`: nazwa konfiguracji serwera.
  - `[DatabaseName <String>]`: nazwa bazy danych.
  - `[FirewallRuleName <String>]`: nazwa reguły zapory serwera.
  - `[Id <String>]`: ścieżka tożsamości zasobu
  - `[KeyName <String>]`: nazwa klucza serwera.
  - `[LocationName <String>]`: nazwa lokalizacji.
  - `[ResourceGroupName <String>]`: nazwa grupy zasobów. W nazwie nie jest uwzględniania liter.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nazwa zasad alertów zabezpieczeń.
  - `[ServerName <String>]`: nazwa serwera.
  - `[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.
  - `[VirtualNetworkRuleName <String>]`: nazwa reguły sieci wirtualnej.

## LINKI POKREWNE

