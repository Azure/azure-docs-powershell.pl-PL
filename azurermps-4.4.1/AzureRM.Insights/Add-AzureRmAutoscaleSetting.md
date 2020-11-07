---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: ee249d7379198a28cad22bf78a6c9ac1bf48f920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719303"
---
# Add-AzureRmAutoscaleSetting

## STRESZCZENIe
Umożliwia utworzenie ustawienia skalowania automatycznego.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Parametry polecenia cmdlet Add-AzureRmAutoscaleSetting w semantyce aktualizacji
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Parametry polecenia cmdlet Add-AzureRmAutoscaleSetting w składni tworzenia semantyki
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzureRmAutoscaleSetting** powoduje utworzenie ustawienia skalowania automatycznego.

## Przykłady

### Przykład 1. Tworzenie ustawienia skalowania automatycznego
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroup "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

Dwa pierwsze polecenia używają New-AzureRmAutoscaleRule do tworzenia dwóch reguł autoskalowania $Rule 1 i $Rule 2.

W przypadku trzeciego i czwartego polecenia za pomocą New-AzureRmAutoscaleProfile utworzyć profile skalowania automatycznego, $Profile 1 i $Profile 2, używając $Rule 1 i $Rule 2.

Polecenie ostatnie powoduje utworzenie ustawienia skalowania automatycznego przy użyciu profilów w $Profile 1 i $Profile 2.

## PARAMETRÓW

### -AutoscaleProfiles
Określa listę profilów, które mają zostać dodane do ustawienia skalowania automatycznego, lub $Null, aby dodać pozycję bez profilu.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableSetting
Wyłącza istniejące ustawienie skalowania automatycznego.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację ustawienia skalowania automatycznego.

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę ustawienia skalowania automatycznego, które ma zostać utworzone.

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Powiadomienia
Określa listę oddzielonych przecinkami powiadomień.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Określa nazwę grupy zasobów dla zasobu skojarzonego z ustawieniem skalowania automatycznego.

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

### -SettingSpec
Określa obiekt **AutoscaleSetting** .
Za pomocą polecenia cmdlet Get-AzureRmAutoscaleSetting można uzyskać obiekt **AutoscaleSetting** lub utworzyć go w skrypcie programu Windows PowerShell.

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
Określa identyfikator zasobu do automatycznego skalowania.

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmAutoscaleSetting](./Get-AzureRmAutoscaleSetting.md)

[Nowe — AzureRmAutoscaleProfile](./New-AzureRmAutoscaleProfile.md)

[Nowe — AzureRmAutoscaleRule](./New-AzureRmAutoscaleRule.md)

[Remove-AzureRmAutoscaleSetting](./Remove-AzureRmAutoscaleSetting.md)


