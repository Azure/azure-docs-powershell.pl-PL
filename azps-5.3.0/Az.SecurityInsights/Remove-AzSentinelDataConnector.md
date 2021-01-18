---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: 19e9dd843cd428a65b371ae933d00c58233de35b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502957"
---
# Remove-AzSentinelDataConnector

## STRESZCZENIe
Usuwanie łącznika danych.

## POLECENIA

### DataConnectorId (domyślny)
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Inputobject
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzSentinelDataConnector** powoduje trwałe usunięcie łącznika danych z określonego obszaru roboczego.
Obiekt programu **dataconnect** można przekazać za pomocą operatora potoku lub można też określić parametry wymagane.
Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.

## Przykłady

### Przykład 1
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

To polecenie powoduje usunięcie programu dataconnect z obszaru roboczego.

## PARAMETRÓW

### -DataConnectorId
Identyfikator łącznika danych.

```yaml
Type: System.String
Parameter Sets: DataConnectorId
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Inputobject.

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
PassThru

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

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nazwa_obszaru_roboczego
Nazwa obszaru roboczego.

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String
### Microsoft. Azure. Commands. SecurityInsights. models. dataconnects. PSSentinelDataConnector
## WYSYŁA

### Microsoft. Azure. Commands. SecurityInsights. models. dataconnects. PSSentinelDataConnector
## INFORMACYJN

## LINKI POKREWNE
