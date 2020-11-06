---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522929"
---
# Get-AzureRmDeploymentManagerRollout

## STRESZCZENIe
Umożliwia rozmieszczenie.

## POLECENIA

### Interaktywny (domyślnie)
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Zasobów
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Inputobject
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmDeploymentManagerRollout** pobiera i zwraca obiekt reprezentujący to rozmieszczenie wraz ze wszystkimi szczegółowymi informacjami na temat postępu wdrożenia.
Określanie rozmieszczenia według nazwy i nazwy grupy zasobów. Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.

### Przykład 2: uzyskiwanie rozmieszczenia przy użyciu identyfikatora zasobu
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.

### Przykład 3: uzyskiwanie rozmieszczenia przy użyciu obiektu do rozmieszczenia.
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

To polecenie pobiera rozmieszczenie, których nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.

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
Nazwa rozmieszczenia.

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

### -RetryAttempt
Próba ponowienia wdrożenia.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wprowadzanie
Rozmieszczanie obiektu.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout

## INFORMACYJN

## LINKI POKREWNE

[Zatrzymaj — AzureRmDeploymentManagerRollout](./Stop-AzureRmDeploymentManagerRollout.md)

[Restart-AzureRmDeploymentManagerRollout](./Restart-AzureRmDeploymentManagerRollout.md)

[Remove-AzureRmDeploymentManagerRollout](./Remove-AzureRmDeploymentManagerRollout.md)