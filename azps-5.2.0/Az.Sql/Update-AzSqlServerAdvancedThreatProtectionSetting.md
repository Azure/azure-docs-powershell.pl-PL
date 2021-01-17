---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: e46ddc53ff7abd7faeee908cf3689683f3575069
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347590"
---
# Update-AzSqlServerAdvancedThreatProtectionSetting

## STRESZCZENIe
Ustawia zaawansowane ustawienia ochrony przed zagrożeniami na serwerze.

## POLECENIA

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Update-AzSqlServerAdvancedThreatProtectionSetting** ustawia zaawansowane ustawienia ochrony przed zagrożeniami na platformie Azure SQL Server.
Aby włączyć zaawansowaną ochronę przed zagrożeniami na serwerze, na tym serwerze muszą być włączone ustawienia inspekcji.
Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz nazwa_serwera identyfikujące serwer.

## Przykłady

### Przykład 1: Ustawianie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych
```powershell
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

To polecenie ustawia zaawansowane ustawienia ochrony przed zagrożeniami dla serwera o nazwie Server01.

### Przykład 2

Ustawia zaawansowane ustawienia ochrony przed zagrożeniami na serwerze. (autogenerowana)

```powershell
<!-- Aladdin Generated Example --> 
Update-AzSqlServerAdvancedThreatProtectionSetting -EmailAdmins $false -ResourceGroupName 'ResourceGroup11' -RetentionInDays <UInt32> -ServerName 'Server01' -StorageAccountName 'mystorageAccount'
```

## PARAMETRÓW

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
Określa nazwę grupy zasobów, do której należy serwer.

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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Określa nazwę konta magazynu, które ma być używane. Używanie symboli wieloznacznych jest niedozwolone. Ten parametr nie jest wymagany. Jeśli nie podano tego parametru, polecenie cmdlet będzie korzystać z konta magazynu, które zostało zdefiniowane wcześniej jako część zaawansowanego ustawienia ochrony przed zagrożeniami w bazie danych. Jeśli po raz pierwszy jest zdefiniowane ustawienie wykrywania zagrożeń dla bazy danych i ten parametr nie zostanie podany, polecenie cmdlet nie powiedzie się.

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

### Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerThreatDetectionsettingsModel

## INFORMACYJN

## LINKI POKREWNE

[Get-AzSqlServerThreatDetectionsettings](./Get-AzSqlServerThreatDetectionsettings.md)

[Remove-AzSqlServerThreatDetectionsettings](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)
