---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 5ea6e36adeb1c0b220b87d516e9c236907bc2c63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051291"
---
# Get-AzDeployment

## STRESZCZENIe
Pobierz wdrożenie

## POLECENIA

### GetByDeploymentName (domyślny)
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzDeployment** pobiera wdrożenia w bieżącym zakresie subskrypcji.
Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.
Domyślnie polecenie **Get-AzDeployment** pobiera wszystkie wdrożenia w bieżącym zakresie subskrypcji.

## Przykłady

### Przykład 1: pobieranie wszystkich wdrożeń w zakresie subskrypcji
```
PS C:\>Get-AzDeployment
```

To polecenie pobiera wszystkie wdrożenia w bieżącym zakresie subskrypcji.

### Przykład 2: uzyskiwanie wdrożenia według nazwy
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

To polecenie pobiera wdrożenie DeployRoles01 w bieżącym zakresie subskrypcji.
Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzDeployment** .
Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.

## PARAMETRÓW

### -ApiVersion
Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.
Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ID
W pełni kwalifikowany identyfikator zasobu wdrożenia.
przykład:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa wdrożenia.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## INFORMACYJN

## LINKI POKREWNE
