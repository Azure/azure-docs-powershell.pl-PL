---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500698"
---
# New-AzDiagnosticSetting

## STRESZCZENIe
Utwórz obiekt PSServiceDiagnosticSettings.

## POLECENIA

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Utwórz obiekt PSServiceDiagnosticSettings.
Może służyć jako parametr `-InputObject` dla `Set-AzDiagnosticSetting`

## Przykłady

### Przykład 1
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

Utwórz obiekt PSServiceDiagnosticSettings. I Utwórz ustawienia diagnostyczne dla zasobu docelowego.

## PARAMETRÓW

### -DedicatedLogAnalyticsDestinationType
Wartość wskazująca, czy wyeksportować (do ODS) do specyficznych dla zasobów (jeśli istnieje) lub do AzureDiagnostics (domyślnie nie jest to obecne)

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventHubAuthorizationRuleId
Identyfikator reguły centrum zdarzeń

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventHubName
Identyfikator reguły usługi Service Bus

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa ustawienia diagnostycznego.
Wartość domyślna "usługa"

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

### -ServiceBusRuleId
Identyfikator reguły usługi Service Bus

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Setting
Ustawienia metryki lub ustawienia dziennika

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
Identyfikator konta magazynu

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
Identyfikator zasobu

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

### -WorkspaceId
Identyfikator zasobu obszaru roboczego Analiza dzienników, do którego mają być wysyłane dzienniki/metryki

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Management. Automation. SwitchParameter

### Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings []

## WYSYŁA

### Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings

## INFORMACYJN

## LINKI POKREWNE
