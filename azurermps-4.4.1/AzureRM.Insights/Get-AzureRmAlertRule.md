---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553860"
---
# Get-AzureRmAlertRule

## STRESZCZENIe
Pobiera reguły alertów.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Parametry polecenia cmdlet Get-AzureRmAlertRule
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Parametry polecenia cmdlet Get-AzureRmAlertRule przy użyciu nazwy
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Parametry polecenia cmdlet Get-AzureRmAlertRule przy użyciu identyfikatora URI zasobu docelowego
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmAlertRule** pobiera regułę alertu przy użyciu jej nazwy lub identyfikatora URI lub wszystkich reguł alertów z określonej grupy zasobów.

## Przykłady

### Przykład 1: uzyskiwanie reguł alertów dla grupy zasobów
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

To polecenie pobiera wszystkie reguły alertów dla grupy zasobów o nazwie Default-Web-Central.
Dane wyjściowe nie zawierają szczegółów dotyczących reguł, ponieważ nie określono parametru *DetailedOutput* .

### Przykład 2: uzyskiwanie reguły alertu według nazwy
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

To polecenie pobiera regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8.
Ponieważ parametr *DetailedOutput* nie jest określony, dane wyjściowe zawierają tylko podstawowe informacje na temat reguły alertu.

### Przykład 3: uzyskiwanie reguły alertu według nazwy z danymi szczegółowymi
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

To polecenie pobiera regułę alertu o nazwie mój alert — 7da64548-214d-42ca-b12b-b245bb8f0ac8.
Określono parametr *DetailedOutput* , więc dane wyjściowe są szczegółowe.

## PARAMETRÓW

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
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Określa nazwę grupy zasobów.

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

### -TargetResourceId
Określa identyfikator zasobu docelowego.

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
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

### System. Collections. Generic. list "1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSManagementItemDescriptor]

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Dodaj-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Dodaj-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Get-AzureRmAlertHistory](./Get-AzureRmAlertHistory.md)

[Remove-AzureRmAlertRule](./Remove-AzureRmAlertRule.md)


