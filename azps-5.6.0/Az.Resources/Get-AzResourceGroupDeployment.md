---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: eb79b6a46f2eaadfc6a42159706c37017cdac8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988933"
---
# Get-AzResourceGroupDeployment

## SYNOPSIS
Pobiera wdrożenia do grupy zasobów.

## SKŁADNIA

### GetByResourceGroupDeploymentName (Domyślna)
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzResourceGroupDeployment** pobiera wdrożenia w grupie zasobów platformy Azure.
Określ parametr *Name (Nazwa)* *lub Id (Identyfikator),* aby filtrować wyniki.
Domyślnie **Get-AzResourceGroupDeployment** pobiera wszystkie wdrożenia dla określonej grupy zasobów.
Zasób platformy Azure to jednostka platformy Azure zarządzana przez użytkownika, taka jak serwer bazy danych, baza danych lub witryna internetowa.
Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.
Wdrożenie to operacja, która udostępnia do użycia zasoby w grupie zasobów.
Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz New-AzResourceGroup cmdlet.
To polecenie cmdlet umożliwia śledzenie.
Do debugowania użyj tego polecenia cmdlet z Get-AzLog cmdlet.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich wdrożeń dla grupy zasobów
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

To polecenie pobiera wszystkie wdrożenia dla grupy zasobów ContosoLabsRG.
W wynikach przedstawiono wdrożenie blogu WordPress, które używało szablonu galerii.

### Przykład 2. Uzyskiwanie wdrożenia według nazwy
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

To polecenie pobiera wdrożenie DeployWebsite01 grupy zasobów ContosoLabsRG.
Nazwę do wdrożenia można przypisać podczas jego tworzenia przy użyciu polecenia cmdlet **New-AzResourceGroup** lub **New-AzResourceGroupDeployment.**
Jeśli nie przypiszesz nazwy, polecenia cmdlet będą mieć nazwę domyślną opartą na szablonie używanym do tworzenia wdrożenia.

### Przykład 3. Uzyskiwanie wdrożeń wszystkich grup zasobów
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

To polecenie pobiera wszystkie grupy zasobów w subskrypcji za pomocą Get-AzResourceGroup cmdlet.
Polecenie przekazuje grupy zasobów do bieżącego polecenia cmdlet przy użyciu operatora potoku.
Bieżące polecenie cmdlet pobiera wszystkie wdrożenia wszystkich grup zasobów w subskrypcji i przekazuje wyniki do polecenia cmdlet Format-Table w celu wyświetlenia wartości właściwości **ResourceGroupName,** **DeploymentName** i **ProvisioningState.**

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

### — Identyfikator
Określa identyfikator wdrożenia grupy zasobów do uzyskania.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę wdrożenia do uzyskania.
Symbole wieloznaczne są niedozwolone.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Przed
Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.

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
Określa nazwę grupy zasobów.
Polecenie cmdlet pobiera wdrożenia grupy zasobów, które określa ten parametr.
Symbole wieloznaczne są niedozwolone.
Ten parametr jest wymagany i w każdym z poleceń można określić tylko jedną grupę zasobów.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroupDeployment

## NOTATKI

## LINKI POKREWNE

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


