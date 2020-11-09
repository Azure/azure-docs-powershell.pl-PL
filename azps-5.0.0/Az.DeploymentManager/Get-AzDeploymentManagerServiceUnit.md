---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304987"
---
# Get-AzDeploymentManagerServiceUnit

## STRESZCZENIe
Pobiera jednostkę usługi.

## POLECENIA

### Interaktywny (domyślnie)
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByServiceObject
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByServiceResourceId
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTopologyObjectAndServiceName
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByTopologyResourceAndServiceName
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Zasobów
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Inputobject
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzDeploymentManagerServiceUnit** pobiera jednostkę usługi w usłudze.

Określ jednostkę usługi według jej nazwy, usługę, w której została ona zdefiniowana, nazwę topologii usług i nazwę grupy zasobów. Alternatywnie możesz podać obiekt serviceunit lub identyfikator zasobu.

Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do jednostki usługi za pomocą polecenia cmdlet Set-AzDeploymentManagerServiceUnit.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.

### Przykład 2: uzyskiwanie jednostki usługi przy użyciu identyfikatora zasobu.
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.

### Przykład 3: uzyskiwanie jednostki usługi przy użyciu obiektu jednostki usługi.
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

To polecenie uzyskuje jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i element źródła $serviceUnitObject danych są zgodne odpowiednio z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName.

## PARAMETRÓW

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

### -Inputobject
Obiekt zasobu jednostka usługi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa jednostki usługi.

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów.

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
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

### -ServiceName
Nazwa usługi, do której należy jednostka usługi.

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Serviceobject
Obiekt usługi, w którym ma zostać utworzona jednostka usługi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Serviceresourceid
Identyfikator zasobu usługi, w którym ma zostać utworzona jednostka usługi.

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servicetopologyname
Nazwa topologii usługi, do której należy jednostka usługi.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servicetopologyobject
Obiekt z topologią usług, w którym należy utworzyć jednostkę usługi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTopologyResourceId
Identyfikator zasobu topologii usług, w którym ma zostać utworzona jednostka usługi.

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource

## WYSYŁA

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource

## INFORMACYJN

## LINKI POKREWNE
