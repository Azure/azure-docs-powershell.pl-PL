---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374255"
---
# Test-AzStackHCIConnection

## STRESZCZENIe
Test-AzStackHCIConnection weryfikuje łączność z lokalnych węzłów klastrowanych z usługami platformy Azure wymaganymi przez stos HCL stosu platformy Azure.

## POLECENIA

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## Opis
Test-AzStackHCIConnection weryfikuje łączność z lokalnych węzłów klastrowanych z usługami platformy Azure wymaganymi przez stos HCL stosu platformy Azure.

## Przykłady

### PRZYKŁAD 1
```
Invoking on one of the cluster node. Success case.
```

Test C:\PS \> -AzStackHCIConnection: Nawiązywanie połączenia z usługą Azure Stack HCL EndpointTested: https://azurestackhci-df.azurefd.net/health isrequireded: prawda wyniku: powodzenie

### PRZYKŁAD 2
```
Invoking on one of the cluster node. Failed case.
```

Test C:\PS \> -AzStackHCIConnection: Nawiązywanie połączenia z usługą Azure Stack HCL EndpointTested: https://azurestackhci-df.azurefd.net/health isrequireded: prawda wyniku: niepowodzenie FailedNodes: Node1inClus2, Node2inClus3

## PARAMETRÓW

### -ComputerName
Umożliwia określenie jednego węzła klastra w klastrze lokalnym, który jest rejestrowany na platformie Azure.

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

### — Poświadczenie
Określa poświadczenie dla komputera ComputerName.
Domyślnie jest to bieżący użytkownik wykonujący polecenie cmdlet.

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
Określa środowisko Azure.
Domyślna to AzureCloud.
Prawidłowe wartości to AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

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

### -Region
Określa region, z którym ma zostać nawiązane połączenie.
Nieużywane, chyba że jest to region Kanaryjskie.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

## WYSYŁA

### PSCustomObject. Zwraca następujące właściwości w PSCustomObject
### Test: Nazwa przeprowadzonego testu.
### EndpointTested: punkt końcowy stosowany w teście.
### IsRequired: prawda lub FAŁSZ
### Wynik: powodzenie lub niepowodzenie
### FailedNodes: lista węzłów, których test nie powiódł się.
## INFORMACYJN

## LINKI POKREWNE
