---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e83f619bd14a2e0ba2012a206d0c3dffd5204863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710671"
---
# Get-AzureRmDeploymentManagerServiceUnit

## STRESZCZENIe
Pobiera jednostkę usługi.

## POLECENIA

### Interaktywny (domyślnie)
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByServiceObject
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByServiceResourceId
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTopologyObjectAndServiceName
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTopologyResourceAndServiceName
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Zasobów
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Inputobject
```
Get-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmDeploymentManagerServiceUnit** pobiera jednostkę usługi w usłudze.

Określ jednostkę usługi według jej nazwy, usługę, w której została ona zdefiniowana, nazwę topologii usług i nazwę grupy zasobów. Alternatywnie możesz podać obiekt serviceunit lub identyfikator zasobu.

Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do jednostki usługi za pomocą polecenia cmdlet Set-AzureRmDeploymentManagerServiceUnit.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.

### Przykład 2: uzyskiwanie jednostki usługi przy użyciu identyfikatora zasobu.
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

To polecenie uzyskuje jednostkę usługi o nazwie ContosoService1Storage w ramach usługi ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.

### Przykład 3: uzyskiwanie jednostki usługi przy użyciu obiektu jednostki usługi.
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

To polecenie uzyskuje jednostkę usługi, której nazwa, nazwa usługi, nazwa topologii usługi i element źródła $serviceUnitObject danych są zgodne odpowiednio z właściwościami Name, ServiceName, servicetopologyname i ResourceGroupName.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa jednostki usługi.

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
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

### -Service
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

### -ServiceName
Nazwa usługi, do której należy jednostka usługi.

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Servicetopology
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

### -Servicetopologyname
Nazwa topologii usługi, do której należy jednostka usługi.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Serviceunit
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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmDeploymentManagerServiceUnit](./New-AzureRmDeploymentManagerServiceUnit.md)

[Remove-AzureRmDeploymentManagerServiceUnit](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[Set-AzureRmDeploymentManagerServiceUnit](./Set-AzureRmDeploymentManagerServiceUnit.md)