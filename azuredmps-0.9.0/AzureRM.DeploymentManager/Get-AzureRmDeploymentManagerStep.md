---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523182"
---
# Get-AzureRmDeploymentManagerStep

## STRESZCZENIe
Pobiera krok wdrożenia.

## POLECENIA

### Interaktywny (domyślnie)
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Zasobów
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Inputobject
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmDeploymentManagerStep** Pobiera krok i zwraca obiekt reprezentujący ten krok.
Określ krok, podając jego nazwę i nazwę grupy zasobów. Alternatywnie możesz podać obiekt Step lub ResourceId.

Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w źródle artefaktów, korzystając z polecenia cmdlet Set-AzureRmDeploymentManagerStep.

## Przykłady

### Przykład 1: uzyskiwanie kroku
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

To polecenie pobiera krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.

### Przykład 2: uzyskiwanie kroku przy użyciu identyfikatora zasobu
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

To polecenie pobiera krok o nazwie ContosoService1WaitStep w ContosoResourceGroup.

### Przykład 3: uzyskiwanie kroku przy użyciu obiektu zwróconego przez New-AzureRmDeploymentManagerStep
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 To polecenie pobiera krok, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $stepObject.


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
Nazwa kroku.

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

### -ResourceGroupName
Grupa zasobów.

```yaml
Type: System.String
Parameter Sets: Interactive
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

### -Krok
Obiekt zasobu kroku.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.
Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource

## WYSYŁA

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource

## INFORMACYJN

## LINKI POKREWNE
