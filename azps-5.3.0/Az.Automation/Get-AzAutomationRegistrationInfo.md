---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502362"
---
# Get-AzAutomationRegistrationInfo

## STRESZCZENIe
Pobiera informacje rejestracyjne dotyczące dołączania węzła DSC lub hybrydowego pracownika do automatyzacji.

## POLECENIA

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzAutomationRegistrationInfo** Pobiera punkt końcowy i klucze wymagane do dołączania węzła konfiguracji stanu (DSC) lub hybrydowego pracownika do konta usługi Azure Automation.

## Przykłady

### Przykład 1: uzyskiwanie informacji o rejestracji
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

To polecenie pobiera informacje rejestracyjne dla konta usługi Automation o nazwie AutomationAccount01 w grupie zasobów o nazwie ResourceGroup01.

## PARAMETRÓW

### -AutomationAccountName
Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera informacje rejestracyjne.

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

### -ResourceGroupName
Określa nazwę grupy zasobów.
To polecenie cmdlet umożliwia pobieranie informacji o rejestracji dla grupy zasobów, którą określa ten parametr.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Automation. model. AgentRegistration

## INFORMACYJN

## LINKI POKREWNE

[Get-AzAutomationAccount](./Get-AzAutomationAccount.md)

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Nowe — AzAutomationKey](./New-AzAutomationKey.md)


