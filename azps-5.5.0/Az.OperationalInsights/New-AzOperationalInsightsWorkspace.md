---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 50920451ca96d21875352ff2ef460a5dcc989a20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186722"
---
# New-AzOperationalInsightsWorkspace

## SYNOPSIS
Powoduje utworzenie obszaru roboczego lub przywrócenie obszaru roboczego "miękkiego usunięcia".

## SKŁADNIA

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzOperationalInsightsWorkspace** tworzy obszar roboczy w określonej grupie zasobów i lokalizacji. Lub przywróć programowo usunięty obszar roboczy.

## PRZYKŁADY

### Przykład 1. Tworzenie obszaru roboczego według nazwy
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

To polecenie tworzy standardowy obszar roboczy SKU o nazwie MyWorkspace w grupie zasobów o nazwie ContosoResourceGroup.

### Przykład 2. Tworzenie obszaru roboczego i łączenie go z istniejącym kontem
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

Pierwsze polecenie używa polecenia cmdlet Get-AzOperationalInsightsLinkTargets w celu uzyskania celów docelowych linku do konta w szczegółowych informacjach operacyjnych, a następnie przechowuje je w $OILinkTargets danych.
Drugie polecenie przekazuje pierwszy element docelowy linku do konta w $OILinkTargets do polecenia cmdlet **New-AzOperationalInsightsWorkspace** przy użyciu operatora potoku.
Polecenie tworzy standardowy obszar roboczy SKU o nazwie MyWorkspace, który jest połączony z pierwszym kontem szczegółowych informacji operacyjnych w programie $OILinkTargets.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — Wymuszanie
Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.

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

### — Lokalizacja
Określa lokalizację, w której ma być tworzyć obszar roboczy, na przykład Wschód Stany Zjednoczone lub Europa Zachodnia.

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

### — Nazwa
Określa nazwę obszaru roboczego.

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

### -PublicNetworkAccessForIngestion
Typ dostępu sieciowego do uzyskiwania dostępu do obszaru roboczego ingestion. Wartość powinna być "Włączona" lub "Wyłączona"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNetworkAccessForQuery
Typ dostępu sieciowego do uzyskiwania dostępu do zapytania obszaru roboczego. Wartość powinna być "Włączona" lub "Wyłączona"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów platformy Azure.
Obszar roboczy zostanie utworzony w tej grupie zasobów.

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
Przechowywanie danych obszaru roboczego w dniach. 730 dni to maksimum dozwolone dla wszystkich pozostałych jednostki SKU.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - SKU
Określa warstwę usługi obszaru roboczego. Aby uzyskać więcej informacji dotyczących wartości, której należy użyć, https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers sprawdź.
Prawidłowe wartości to:
- bezpłatnie
- pergb2018
- pernode
- premium
- autonomiczny
- standardowy

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tag
Tagi zasobów dla obszaru roboczego.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Hashtable

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace

## NOTATKI

Opublikowano nowy model cen. Jeśli jesteś programem CSP, oznacza to, że musisz używać "autonomicznej" jednostki SKU. W tle wersja SKU zostanie zmieniona na pergb2018. Aby uzyskać więcej informacji, zobacz następujące informacje: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model

## LINKI POKREWNE

[Polecenia cmdlet usługi Azure Operational Insights](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsLinkTargets](./Get-AzOperationalInsightsLinkTargets.md)


