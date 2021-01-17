---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335278"
---
# Update-AzNetAppFilesSnapshotPolicy

## STRESZCZENIe
Umożliwia zaktualizowanie zasad migawki plików usługi Azure NetApp (ANF) do dodanych opcjonalnych modyfikatorów.

## POLECENIA

### ByFieldsParameterSet (domyślny)
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByParentObjectParameterSet
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Update-AzNetAppFilesSnapshotPolicy** modyfikuje zasady migawki ANF.

## Przykłady

### Przykład 1
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

To polecenie powoduje zmianę zasad tworzenia kopii zapasowej ANF "MySnapshotPolicy", aby uzyskać dane HourlySchedule.

## PARAMETRÓW

### -AccountName
Nazwa konta usługi ANF

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Accountobject
Konto nowego obiektu zasad migawki

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DailySchedule
Tablica Hashtable, która reprezentuje harmonogram dzienny

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Enabled
Właściwość decydowania o zasadach jest włączona lub nie

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HourlySchedule
Tablica Hashtable, która reprezentuje harmonogram godzinowy

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Obiekt migawki do usunięcia

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja zasobu

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlySchedule
Tablica Hashtable przedstawiająca Harmonogram miesięczny

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa zasady migawki ANF

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów konta ANF

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu w zasadach migawki ANF

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Tablica Hashtable przedstawiająca znaczniki zasobów

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeeklySchedule
Tablica Hashtable przedstawiająca Harmonogram miesięczny

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount

### Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshotPolicy

## WYSYŁA

### Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesSnapshotPolicy

## INFORMACYJN

## LINKI POKREWNE
