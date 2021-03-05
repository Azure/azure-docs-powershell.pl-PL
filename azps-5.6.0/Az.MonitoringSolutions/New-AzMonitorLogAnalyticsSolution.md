---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: ff9a54852d84d7c1183e81cb8b597279f357ebe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965738"
---
# New-AzMonitorLogAnalyticsSolution

## SYNOPSIS
Tworzy rozwiązanie do analizy dziennika.

## SKŁADNIA

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## OPIS
Tworzy rozwiązanie do analizy dziennika.

## PRZYKŁADY

### Przykład 1. Tworzenie rozwiązania do analizy dzienników monitorów dla obszaru roboczego analizy dziennika
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

To polecenie tworzy rozwiązanie do analizy dzienników monitorów dla obszaru roboczego analizy dziennika.

Najczęściej używane typy:

| Typ | Opis |
| :-----| :----- |
| SecurityCenterFree |  Azure Security Center — wersja bezpłatna |
| Zabezpieczenia | Azure Security Center |
| Aktualizacje | Zarządzanie aktualizacjami |
| ContainerInsights | Azure Monitor for Containers |
| ServiceMap | Mapa usługi |
| AzureActivity | Analiza dziennika aktywności |
| ChangeTracking | Śledzenie zmian i spis |
| VMInsights | Azure Monitor dla maszyn wirtualnych |
| SecurityInsights | Azure Sentinel |
| NetworkMonitoring | Monitor wydajności sieci |
| SQLVulnerabilityAssessment | Ocena luk w zabezpieczeniach języka SQL |
| SQLAdvancedThreatProtection | Zaawansowana ochrona przed zagrożeniami w języku SQL |
| Ochrona przed złośliwym oprogramowaniem | Ocena oprogramowania w celu ochrony przed złośliwym oprogramowaniem |
| AzureAutomation | Pracownik hybrydowy automatyzacji |
| LogicAppsManagement | Zarządzanie aplikacjami logic |
| SQLDataClassification | Klasyfikacja & odnajdowania danych SQL |

## PARAMETERS

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

### — Lokalizacja
Lokalizacja zasobu.
Musi być taki sam jak obszar roboczy analityczny dziennika.

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

### -ResourceGroupName
Nazwa grupy zasobów do uzyskania.
W nazwie nie jest uwzględniania liter.

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

### - SubscriptionId
Pobiera poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.
Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tag
Tagi zasobów

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Wpisz
Typ rozwiązania do utworzenia.
Na przykład "Kontener".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceResourceId
Identyfikator zasobu Azure dla obszaru roboczego, w którym rozwiązanie zostanie wdrożone/włączone.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

## DANE WYJŚCIOWE

### Microsoft.Azure.PowerShell.Cmdlet.MonitoringSolutions.Models.Api20151101Preview.ISolution

## NOTATKI

ALIASY

## LINKI POKREWNE



[Get-AzOperationalInsightsWorkspace](https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

