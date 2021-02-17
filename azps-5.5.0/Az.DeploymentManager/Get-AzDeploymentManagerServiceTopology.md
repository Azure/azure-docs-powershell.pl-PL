---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177003"
---
# Get-AzDeploymentManagerServiceTopology

## SYNOPSIS
Pobiera topologię usługi.

## SKŁADNIA

### Interakcyjna (domyślna)
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceId
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzDeploymentManagerServiceTopology** uzyskuje topologię usługi.

Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do topologii za pomocą Set-AzDeploymentManagerServiceTopology cmdlet.
Określanie topologii usługi według jej nazwy i nazwy grupy zasobów. Ewentualnie można udostępnić obiekt ServiceTopology lub identyfikator Zasobu.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

To polecenie pobiera topologię usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.

### Przykład 2. Uzyskiwanie topologii usługi przy użyciu identyfikatora zasobu.
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

To polecenie pobiera topologię usługi o nazwie ContosoServiceTopology w grupie ContosoResourceGroup.

### Przykład 3. Uzyskiwanie topologii usługi przy użyciu obiektu topologii usługi.
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

To polecenie pobiera topologię usługi, której nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $serviceTopologyObject ResourceGroupName (Nazwa grupy zasobów).

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
Obiekt zasobu topologii usługi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Nazwa
Nazwa topologii usługi.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource

## NOTATKI

## LINKI POKREWNE
