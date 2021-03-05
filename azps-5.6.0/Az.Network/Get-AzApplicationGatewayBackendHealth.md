---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: b5910352c8abcfb880a1007a3f2246ff7c12d9f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003617"
---
# Get-AzApplicationGatewayBackendHealth

## SYNOPSIS
Pobiera kondycję zaplecza bramy aplikacji.

## SKŁADNIA

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie Get-AzApplicationGatewayBackendHealth pobiera kondycję zaplecza bramy aplikacji.

## PRZYKŁADY

### Przykład 1. Kondycja zaplecza bez rozwiniętych zasobów.
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

To polecenie pobiera kondycję zaplecza bramy aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $BackendHealth zasobów.

### Przykład 2. Kondycja bazy danych z rozwiniętymi zasobami.
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

To polecenie ma kondycję zaplecza (z rozwiniętymi zasobami) bramy aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w $BackendHealth zasobów.

## PARAMETERS

### — AsJob
Uruchamianie polecenia cmdlet w tle

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -ExpandResource
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

### — Nazwa
Określa nazwę bramy aplikacji, która otrzymuje to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej bramę aplikacji.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth

## NOTATKI
Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking

## LINKI POKREWNE

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

