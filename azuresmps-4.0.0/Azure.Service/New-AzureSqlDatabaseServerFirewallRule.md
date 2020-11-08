---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054935"
---
# New-AzureSqlDatabaseServerFirewallRule

## STRESZCZENIe
Tworzy regułę zapory na serwerze bazy danych SQL Azure.

## POLECENIA

### IpRange (domyślny)
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AllowAllAzureServices
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureSqlDatabaseServerFirewallRule** powoduje utworzenie reguły zapory w określonym wystąpieniu serwera bazy danych SQL Azure w bieżącej subskrypcji.

Parametry *StartIpAddress* i *EndIpAddress* służą do określenia zakresu adresów IP, które ta reguła zezwala na łączenie się z serwerem bazy danych SQL Azure.

Określ parametr *AllowAllAzureServices* , aby utworzyć regułę umożliwiającą nawiązywanie połączeń platformy Azure z serwerem.
Reguła ma początkowe i końcowe wartości adresów IP 0.0.0.0.
Jeśli nie określisz nazwy reguły zapory, to polecenie cmdlet przypisze domyślną nazwę AllowAllAzureServices.

## Przykłady

### Przykład 1. Tworzenie reguły zapory
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

To polecenie tworzy regułę zapory FirewallRule24 na serwerze bazy danych SQL Azure o nazwie lpqd0zbr8y.
Polecenie określa zakres adresów IP.

### Przykład 2: Tworzenie reguły umożliwiającej korzystanie ze wszystkich usług platformy Azure
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

To polecenie tworzy regułę zapory o nazwie AzureConnections na serwerze o nazwie lpqd0zbr8y, który umożliwia nawiązywanie połączeń platformy Azure.

### Przykład 3: Tworzenie reguły pozwalającej wszystkim usługom platformy Azure używającym domyślnej nazwy utworzyć regułę umożliwiającą wszystkim usługom Azure używającym domyślnej nazwy
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

To polecenie tworzy regułę zapory na określonym serwerze o nazwie lpqd0zbr8y, który umożliwia nawiązywanie połączeń platformy Azure.
Polecenie przypisuje domyślną nazwę reguły AllowAllAzureServices.

## PARAMETRÓW

### -AllowAllAzureServices
Wskazuje, że ta reguła zapory umożliwia dostęp do serwera wszystkim adresom IP platformy Azure.

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndIpAddress
Określa wartość końcową zakresu adresów IP dla tej reguły.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -RuleName
Określa nazwę nowej reguły zapory.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nazwa_serwera
Określa nazwę serwera.
To polecenie cmdlet powoduje utworzenie reguły zapory na serwerze, który określi to polecenie cmdlet.
Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartIpAddress
Określa wartość początkową zakresu adresów IP dla reguły zapory.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerFirewallRuleContext

## INFORMACYJN

## LINKI POKREWNE

[Baza danych SQL Azure](https://azure.microsoft.com/en-us/services/sql-database/)

[Tworzenie reguły zapory](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[Operacje dotyczące baz danych platformy Azure SQL](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseServerFirewallRule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[Remove-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Set-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


