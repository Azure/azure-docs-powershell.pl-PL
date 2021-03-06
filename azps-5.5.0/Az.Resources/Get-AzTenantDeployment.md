---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192763"
---
# Get-AzTenantDeployment

## SYNOPSIS
Uzyskaj wdrożenie w zakresie dzierżawy

## SKŁADNIA

### GetByDeploymentName (domyślna)
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzTenantDeployment** pobiera wdrożenia w zakresie dzierżawy.
Określ parametr *Name (Nazwa)* *lub Id (Identyfikator),* aby filtrować wyniki.
Domyślnie **get-azTenantDeployment** pobiera wszystkie wdrożenia w zakresie dzierżawy.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich wdrożeń w zakresie dzierżawy
```
PS C:\>Get-AzTenantDeployment
```

To polecenie pobiera wszystkie wdrożenia w bieżącym zakresie dzierżawy.

### Przykład 2. Uzyskiwanie wdrożenia według nazwy
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

To polecenie pobiera wdrożenie "Deploy01" w zakresie bieżącej dzierżawy.
Możesz przypisać nazwę do wdrożenia podczas jego tworzenia przy użyciu polecenia **cmdlet New-AzTenantDeployment.**
Jeśli nie przypiszesz nazwy, polecenia cmdlet będą używać domyślnej nazwy na podstawie szablonu użytego do utworzenia wdrożenia.

### Przykład 3. Uzyskiwanie wdrożenia według identyfikatora
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

To polecenie pobiera wdrożenie "Deploy01" w zakresie dzierżawy.

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

### — Id
W pełni kwalifikowany identyfikator zasobu wdrożenia.
przykład: /providers/Microsoft.Resources/deployments/{deploymentName}

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

### — Nazwa
Nazwa wdrożenia.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Przed
Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.

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

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## NOTATKI

## LINKI POKREWNE
