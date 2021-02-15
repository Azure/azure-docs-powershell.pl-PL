---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182379"
---
# Sync-AzAnalysisServicesInstance

## SYNOPSIS

Synchronizuje określoną bazę danych na określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami skalowania zapytania w obecnie zalogowanym środowisku zgodnie z Add-AzAnalysisServicesAccount polecenia

## SKŁADNIA

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS

Polecenie cmdlet Sync-AzAnalysisServicesInstance synchronizuje określoną bazę danych w określonym wystąpieniu serwera usług Analysis Services ze wszystkimi wystąpieniami skalowania zapytania w obecnie zalogowanym środowisku zgodnie z poleceniem Add-AzAnalysisServicesAccount

## PRZYKŁADY

### Przykład 1

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

To polecenie zsynchronizuje bazę danych o nazwie ZamówieniaSprzedaży na serwerze o nazwie "contoso" w środowisku westus.asazure.windows.net pod warunkiem, że użytkownik zalogował się do tego środowiska przy użyciu Add-AzAnalysisServicesAccount.

## PARAMETERS

### — Baza danych

Tożsamość bazy danych do zsynchronizowania

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### —Instance

Nazwa wystąpienia serwera usług Analysis Services do ponownego uruchomienia

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails

## NOTATKI

Alias: Sync-AzAsInstance

## LINKI POKREWNE
