---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: f1328b71564b0fd839d3481a87b23a2a8b24ab55
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342745"
---
# Get-AzAutomationDscNode

## STRESZCZENIe
Pobiera węzły DSC z automatyzacji.

## POLECENIA

### ByAll (domyślny)
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNodeConfiguration
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfiguration
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzAutomationDscNode** pobiera węzły konfiguracji stanu żądanego (DSC) z usługi Azure Automation.

## Przykłady

### Przykład 1: uzyskiwanie wszystkich węzłów DSC
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

To polecenie pobiera metadane wszystkich węzłów DSC na koncie usługi Automation o nazwie Contoso17.

### Przykład 2: uzyskiwanie wszystkich węzłów DSC dla konfiguracji DSC
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

To polecenie pobiera metadane wszystkich węzłów DSC na koncie usługi Automation o nazwie Contoso17, które są mapowane na konfigurację węzła DSC wygenerowaną przez ContosoConfiguration konfiguracji DSC.

### Przykład 3: pobieranie węzła DSC o IDENTYFIKATORze
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

To polecenie pobiera metadane z węzła DSC o określonym IDENTYFIKATORze w koncie automatyzacji o nazwie Contoso17.

### Przykład 4: pobieranie węzła DSC według nazwy
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

To polecenie pobiera metadane z węzła DSC o nazwie Computer14 na koncie usługi Automation o nazwie Contoso17.

### Przykład 5: uzyskiwanie wszystkich węzłów DSC zamapowanych na konfigurację węzła DSC
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

To polecenie pobiera metadane we wszystkich węzłach DSC na koncie usługi Automation o nazwie Contoso17, które są mapowane na konfigurację węzła DSC o nazwie ContosoConfiguration. WebServer.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji zawierającego węzły DSC, które są dostępne w tym poleceniu cmdlet.

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
Określa nazwę konfiguracji DSC.
To polecenie cmdlet spowoduje wyświetlenie węzłów DSC zgodnych z konfiguracją węzła wygenerowaną na podstawie konfiguracji, którą określa ten parametr.

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ID
Określa unikatowy identyfikator węzła DSC, który jest pobierany przez to polecenie cmdlet.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę węzła DSC, który ma być pobierany przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NodeConfigurationName
Określa nazwę konfiguracji węzła, którą to polecenie cmdlet pobiera.

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, w której ten aplet polecenia pobiera węzły DSC.

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

### -Status
Określa stan węzłów DSC, które są pobierane przez to polecenie cmdlet.
Prawidłowe wartości: 
- Star 
- NotCompliant
- Nie powiodło się
- Wybranego 
- Odebrał
- Odpowiadać

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. GUID

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. DscNode

## INFORMACYJN

## LINKI POKREWNE

[Rejestr — AzAutomationDscNode](./Register-AzAutomationDscNode.md)

[Set-AzAutomationDscNode](./Set-AzAutomationDscNode.md)

[Wyrejestrowanie — AzAutomationDscNode](./Unregister-AzAutomationDscNode.md)


