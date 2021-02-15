---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182402"
---
# Restart-AzAnalysisServicesInstance

## SYNOPSIS
Ponowne uruchamianie wystąpienia serwera usług Analysis Services w obecnie zalogowanym środowisku zgodnie z Add-AzAnalysisServicesAccount programu

## SKŁADNIA

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie Restart-AzAnalysisServicesInstance powoduje ponowne uruchomienie wystąpienia serwera usług Azure Analysis Services

## PRZYKŁADY

### Przykład 1
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

To polecenie spowoduje ponowne uruchomienie serwera "serwer testowy" w środowisku określonym przez Add-AzAnalysisServicesAccount serwera

## PARAMETERS

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## OUTPUTS

### System.Boolean

## NOTATKI
Alias: Restart-AzAsInstance

## LINKI POKREWNE
