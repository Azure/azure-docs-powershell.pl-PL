---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192322"
---
# Get-AzIntegrationAccount

## SYNOPSIS
Otrzymuje konta integracji.

## SKŁADNIA

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzIntegrationAccount** pobiera konta integracji z grupy zasobów. Określ nazwę konta integracji i nazwę grupy zasobów.
Ten moduł obsługuje parametry dynamiczne.
Aby użyć parametru dynamicznego, wpisz go w poleceniu.
Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.
Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie konta integracji według nazwy
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

To polecenie pobiera konto integracji o nazwie IntegrationAccount31 z określonej grupy zasobów.

### Przykład 2. Uzyskiwanie kont integracji w grupie zasobów
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

To polecenie pobiera konta integracji z grupy zasobów o nazwie ResourceGroup11.

### Przykład 3. Uzyskiwanie wszystkich kont integracji
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

To polecenie pobiera wszystkie konta integracji w subskrypcji platformy Azure.

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

### — Nazwa
Określa nazwę konta integracji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.Logic.Models.IntegrationAccount

## NOTATKI

## LINKI POKREWNE

[Get-AzIntegrationAccountCallbackUrl](./Get-AzIntegrationAccountCallbackUrl.md)

[New-AzIntegrationAccount](./New-AzIntegrationAccount.md)

[Remove-AzIntegrationAccount](./Remove-AzIntegrationAccount.md)

[Set-AzIntegrationAccount](./Set-AzIntegrationAccount.md)


