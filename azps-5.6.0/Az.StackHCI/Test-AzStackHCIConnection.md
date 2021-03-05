---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 4de1e1467e1bc422666b7144f5d5fcd6c30c0c63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976209"
---
# Test-AzStackHCIConnection

## SYNOPSIS
Test-AzStackHCIConnection sprawdza łączność lokalnych węzłów grupowanych z usługami Azure wymaganymi przez usługę Azure Stack HCI.

## SKŁADNIA

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## OPIS
Test-AzStackHCIConnection sprawdza łączność lokalnych węzłów grupowanych z usługami Azure wymaganymi przez usługę Azure Stack HCI.

## PRZYKŁADY

### PRZYKŁAD 1
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
Wywołuj w jednym z węźle klastrów. Przypadek sukcesu.

### PRZYKŁAD 2
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
Wywołuj w jednym z węźle klastrów. Nie powiodła się sprawa.

## PARAMETERS

### — Nazwa_komputera
Określa jeden z węzła klastrów w klastrze lokalnym, który jest zarejestrowany na platformie Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Credential
Określa poświadczenia dla parametru Nazwa_komputera.
Wartość domyślna to bieżący użytkownik wykonujący polecenie cmdlet.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Określa środowisko platformy Azure.
Wartością domyślną jest usługa AzureCloud.
Prawidłowe wartości to: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### — Region
Określa region, z który ma nawiązać połączenie.
Nie jest używany, chyba że jest to region Canary.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

## DANE WYJŚCIOWE

### PSCustomObject. Zwraca następujące właściwości w programie PSCustomObject.
### Test: nazwa wykonanego testu.
### EndpointTested: Punkt końcowy używany w teście.
### IsRequired: True or False
### Wynik: powodzenie lub niepowodzenie
### FailedNodes: lista węzłów, w których test zakończył się niepowodzeniem.
## NOTATKI

## LINKI POKREWNE
