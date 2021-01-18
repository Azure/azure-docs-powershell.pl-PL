---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499365"
---
# Update-AzSqlDatabaseAdvancedThreatProtectionSetting

## STRESZCZENIe
Ustawia zaawansowane ustawienia ochrony przed zagrożeniami w bazie danych.

## POLECENIA

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** ustawia zaawansowane ustawienia ochrony przed zagrożeniami w bazie danych Azure SQL.
Aby włączyć zaawansowaną ochronę przed zagrożeniami w bazie danych, muszą być włączone ustawienia inspekcji w tej bazie danych.
Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName*, *nazwa_serwera* i *DatabaseName* , które identyfikują bazę danych.
To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.

## Przykłady

### Przykład 1: Ustawianie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

To polecenie ustawia zaawansowane ustawienia ochrony przed zagrożeniami dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.

## PARAMETRÓW

### -DatabaseName
Określa nazwę bazy danych, w której ustawiono ustawienia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -EmailAdmins
Określa, czy ustawienia zaawansowanego ochrony przed zagrożeniami mają kontakt z administratorami za pomocą poczty e-mail.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExcludedDetectionType
Określa tablicę typów wykrywania, które należy wykluczyć z ustawień.
Dopuszczalne wartości tego parametru to:
- Sql_Injection 
- Sql_Injection_Vulnerability 
- Access_Anomaly 
- Znaleziono

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationRecipientsEmails
Określa rozdzielaną średnikami listę adresów e-mail, do których mają być wysyłane powiadomienia o ustawieniach.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Zwraca obiekt reprezentujący element, z którym pracujesz.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której jest przypisany serwer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Liczba dni przechowywania dzienników inspekcji

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nazwa_serwera
Określa nazwę serwera.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Określa nazwę konta magazynu, które ma być używane. Używanie symboli wieloznacznych jest niedozwolone. Ten parametr nie jest wymagany. Jeśli nie podano tego parametru, polecenie cmdlet będzie korzystać z konta magazynu, które zostało zdefiniowane wcześniej jako część zaawansowanego ustawienia ochrony przed zagrożeniami w bazie danych. Jeśli jest to pierwsza definicja zaawansowanego ustawienia ochrony przed zagrożeniami dla bazy danych i nie zostanie podany ten parametr, polecenie cmdlet nie powiedzie się.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### Microsoft. Azure. Commands. SQL. ThreatDetection. model. Detecttype []

### System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## WYSYŁA

### Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseThreatDetectionsettingsModel

## INFORMACYJN

## LINKI POKREWNE

[Get-AzSqlDatabaseThreatDetectionsettings](./Get-AzSqlServerThreatDetectionsettings.md)

[Remove-AzSqlDatabaseThreatDetectionsettings](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)


