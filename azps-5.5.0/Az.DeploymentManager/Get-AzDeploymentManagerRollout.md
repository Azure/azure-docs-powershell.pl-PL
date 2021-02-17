---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198018"
---
# Get-AzDeploymentManagerRollout

## SYNOPSIS
Pobiera rozmówienie.

## SKŁADNIA

### Interakcyjna (domyślna)
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDeploymentManagerRollout** pobiera rzutowanie i zwraca obiekt reprezentujący to rzutowanie ze wszystkimi szczegółowymi informacjami o postępie tego rzutowania.
Określ wycofanie według jego nazwy i nazwy grupy zasobów. Ewentualnie możesz podać obiekt Rollout lub Identyfikator Zasobu.

Zwrócony obiekt wdrażania zawiera usługi, jednostki usługi i kroki, które zostały wdrożone, oraz te, które są w toku. Te, które jeszcze nie zostaną wdrożone, nie są w odpowiedzi.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie rozłożenia
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

To polecenie pobiera wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup. 

### Przykład 2. Uzyskiwanie i wyświetlanie szczegółów dotyczących rzutowania
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

To polecenie pobiera wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup. Przełącznik -Verbose wyświetla wszystkie szczegóły dotyczące rzutowania hierarchicznie; wyświetlając usługi, jednostki ServiceUnits oraz kroki w ramach poszczególnych jednostek ServiceUnit oraz informacje kontekstowe dla każdego kroku w widoku infektowania.

### Przykład 3. Uzyskiwanie wycofywania przy użyciu identyfikatora zasobu
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

To polecenie pobiera wykonanie o nazwie ContosoRollout w grupie ContosoResourceGroup.

### Przykład 4. Uzyskiwanie rzutowania przy użyciu obiektu rozsyłania.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

To polecenie pobiera rzutowanie, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $rolloutObject ResourceGroupName (Nazwa grupy zasobów).

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

### -InputObject
Obiekt Rollout.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa tego rozsyłania.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetryAttempt
Ponowna próba wykonania.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
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

### System.String

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

### Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout

## NOTATKI

## LINKI POKREWNE
