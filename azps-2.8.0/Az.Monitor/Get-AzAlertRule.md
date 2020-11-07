---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 9e1a0035a9736ac01963d150f06db9e510e51e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704825"
---
# Get-AzAlertRule

## STRESZCZENIe
Pobiera reguły alertów.

## POLECENIA

### GetByResourceGroup
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceUri
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzAlertRule** pobiera regułę alertu przy użyciu jej nazwy lub identyfikatora URI lub wszystkich reguł alertów z określonej grupy zasobów.

## Przykłady

### Przykład 1: uzyskiwanie reguł alertów dla grupy zasobów
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

To polecenie pobiera wszystkie reguły alertów dla grupy zasobów o nazwie Default-Web-Central.
Dane wyjściowe nie zawierają szczegółów dotyczących reguł, ponieważ nie określono parametru *DetailedOutput* .

### Przykład 2: uzyskiwanie reguły alertu według nazwy
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

To polecenie pobiera regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8.
Ponieważ parametr *DetailedOutput* nie jest określony, dane wyjściowe zawierają tylko podstawowe informacje na temat reguły alertu.

### Przykład 3: uzyskiwanie reguły alertu według nazwy z danymi szczegółowymi
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

To polecenie pobiera regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8.
Określono parametr *DetailedOutput* , więc dane wyjściowe są szczegółowe.

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

### -DetailedOutput
Wyświetla wszystkie szczegóły w wynikach.

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

### -Name (nazwa)
Określa nazwę reguły alertu, którą należy uzyskać.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
Określa identyfikator zasobu docelowego.

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzLogAlertRule](./Add-AzLogAlertRule.md)

[Dodaj-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Dodaj-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[Get-AzAlertHistory](./Get-AzAlertHistory.md)

[Remove-AzAlertRule](./Remove-AzAlertRule.md)


