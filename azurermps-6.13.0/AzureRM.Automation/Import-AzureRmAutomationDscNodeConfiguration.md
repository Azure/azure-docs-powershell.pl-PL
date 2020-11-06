---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 49cd2fdb2d482621ea52f1df88c9bcd95521badd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550367"
---
# Import-AzureRmAutomationDscNodeConfiguration

## STRESZCZENIe
Importuje dokument MOF jako konfigurację węzła DSC w automatyzacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Import-AzureRmAutomationDscConfiguration** importuje dokument konfiguracji Managed Object Format (MOF) do usługi Azure Automation jako konfigurację wybranego węzła konfiguracji stanu (DSC).
Określ ścieżkę pliku MOF.

## Przykłady

### Przykład 1: Importowanie konfiguracji węzła DSC do automatyzacji
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

To polecenie importuje konfigurację węzła DSC z pliku WebServer. MOF do konta usługi Automation o nazwie Contoso17 pod nazwą konfiguracji DSC ContosoConfiguration.
Polecenie określa parametr *Force* .
Jeśli istnieje konfiguracja węzła DSC o nazwie ContosoConfiguration. WebServer, to polecenie zamieni je.

### Przykład 2: Importowanie konfiguracji węzłów DSC do automatyzacji i tworzenie nowej wersji kompilacji bez zastępowania istniejących NodeConfiguration.
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

To polecenie importuje konfigurację węzła DSC z pliku WebServer. MOF do konta usługi Automation o nazwie Contoso17 pod nazwą konfiguracji DSC ContosoConfiguration.
Polecenie określa parametr *Force* .
Jeśli istnieje konfiguracja węzła DSC o nazwie ContosoConfiguration. WebServer, to polecenie doda nową wersję kompilacji o nazwie ContosoConfiguration [2]. WebServer.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji, do którego jest zaimportowana konfiguracja węzła DSC przy użyciu tego polecenia cmdlet.

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
Określa nazwę konfiguracji DSC w automatyzacji, która ma być używana jako obszar nazw i kontener konfiguracji węzła do zaimportowania.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Force
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

### -Path
Określa ścieżkę dokumentu konfiguracji MOF, który został zaimportowany za pomocą tego polecenia cmdlet.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. NodeConfiguration

## INFORMACYJN

## LINKI POKREWNE

[Eksportowanie — AzureRmAutomationDscConfiguration](./Export-AzureRmAutomationDscConfiguration.md)

[Get-AzureRmAutomationDscConfiguration](./Get-AzureRmAutomationDscConfiguration.md)


