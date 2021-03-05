---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3680d277addba29444f3f2955d7cca28505435a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014042"
---
# Import-AzAutomationDscNodeConfiguration

## SYNOPSIS
Importuje dokument MOF jako konfigurację węzła DSC w automatyzacji.

## SKŁADNIA

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Import-AzAutomationDscConfiguration** importuje dokument konfiguracji formatu zarządzanego obiektu (MOF, Managed Object Format) do konfiguracji węzła azure Automation jako konfiguracji żądanego stanu (DSC).
Określ ścieżkę pliku mof.

## PRZYKŁADY

### Przykład 1. Importowanie konfiguracji węzła dsc do automatyzacji
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

To polecenie importuje konfigurację węzła DSC z pliku o nazwie webserver.mof do konta automatyzacji o nazwie Contoso17 w ramach konfiguracji DSC ContosoConfiguration.
Polecenie określa parametr *Force.*
Jeśli istnieje konfiguracja węzła DSC o nazwie ContosoConfiguration.webserver, to polecenie zastępuje je.

### Przykład 2. Importowanie konfiguracji węzła dsc do automatyzacji i tworzenie nowej wersji kompilacji, a nie zastępowanie istniejącej konfiguracji NodeConfiguration.
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

To polecenie importuje konfigurację węzła DSC z pliku o nazwie webserver.mof do konta automatyzacji o nazwie Contoso17 w ramach konfiguracji DSC ContosoConfiguration.
Polecenie określa parametr *Force.*
Jeśli istnieje konfiguracja węzła DSC o nazwie ContosoConfiguration.webserver, to polecenie dodaje nową wersję kompilacji o nazwie ContosoConfiguration[2].webserver.

## PARAMETERS

### -AutomationAccountName
Określa nazwę konta automatyzacji, do którego to polecenie cmdlet importuje konfigurację węzła DSC.

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

### -ConfigurationName
Określa nazwę konfiguracji dsc w automatyzacji, która ma być określana jako przestrzeń nazw i kontener dla konfiguracji węzła do zaimportowania.

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
Wskazuje, że to polecenie cmdlet zastępuje istniejącą konfigurację węzła DSC w automatyzacji.

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

### -IncrementNodeConfigurationBuild
Tworzy nową wersję kompilacji konfiguracji węzła.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### — Ścieżka
Określa ścieżkę importowanego przez to polecenie cmdlet dokumentu konfiguracji MOF.

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

### -ResourceGroupName
Określa nazwę grupy zasobów, dla której to polecenie cmdlet importuje konfigurację węzła DSC.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Automation.Model.NodeConfiguration

## NOTATKI

## LINKI POKREWNE

[Export-AzAutomationDscConfiguration](./Export-AzAutomationDscConfiguration.md)

[Get-AzAutomationDscConfiguration](./Get-AzAutomationDscConfiguration.md)


