---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: f4f2e76a9354ee6ed796b64cbdd83f21d70ff954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978385"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## SYNOPSIS
Pobierz obsługiwane zmienne serwera oraz dostępne nagłówki żądań i odpowiedzi.

## SKŁADNIA

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzApplicationGatewayAvailableServerVariableAndHeader** pobiera obsługiwane zmienne serwera oraz dostępne nagłówki żądań i odpowiedzi. Parametry mogą być używane do odejmowania zmiennych lub list nagłówków.

## PRZYKŁADY

### Przykład 1
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

To polecenia zwraca wszystkie dostępne zmienne serwera.

### Przykład 2
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

To polecenia zwraca wszystkie dostępne nagłówki żądań.

### Przykład 3
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

To polecenia zwraca wszystkie dostępne nagłówki odpowiedzi.

### Przykład 4
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

To polecenia zwraca wszystkie dostępne zmienne serwera, nagłówki żądań i odpowiedzi.

### Przykład 5
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

To polecenia zwraca wszystkie dostępne zmienne serwera, nagłówki żądań i odpowiedzi.

## PARAMETERS

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

### -RequestHeader
Dostępne nagłówki żądań bramy aplikacji.

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

### -ResponseHeader
Brama aplikacji zawiera nagłówki odpowiedzi.

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

### -ServerVariable
Dostępne zmienne serwera bramy aplikacji.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult

## NOTATKI
**List-AzApplicationGatewayAvailableServerVariableAndHeader** to alias polecenia cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader.**

## LINKI POKREWNE
