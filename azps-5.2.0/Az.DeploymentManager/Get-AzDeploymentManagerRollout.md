---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324245"
---
# Get-AzDeploymentManagerRollout

## STRESZCZENIe
Pobiera rozmieszczenie.

## POLECENIA

### Interaktywny (domyślnie)
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Zasobów
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Inputobject
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzDeploymentManagerRollout** pobiera i zwraca obiekt reprezentujący to rozmieszczenie wraz ze wszystkimi szczegółowymi informacjami na temat postępu wdrożenia.
Określanie rozmieszczenia według nazwy i nazwy grupy zasobów. Alternatywnie możesz podać obiekt rozmieszczenia lub identyfikator zasobu ResourceId.

Zwrócony obiekt rozmieszczenia zawiera usługi, jednostki usług i kroki, które zostały wdrożone, i te, które są w toku. Te, które nie zostały jeszcze wdrożone, nie znajdują się w odpowiedzi.

## Przykłady

### Przykład 1 pobieranie rozmieszczenia
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup. 

### Przykład 2 pobieranie i wyświetlanie szczegółów rozmieszczenia
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup. Przełącznik-verbose umożliwia wyświetlanie wszystkich szczegółów dotyczących rozmieszczenia hierarchicznie; Pokazywanie usług, jednostek oraz kroków w poszczególnych jednostkach oraz informacje kontekstowe dla każdego kroku w celu uzyskania całościowego widoku rozmieszczenia.

### Przykład 3: uzyskiwanie rozmieszczenia przy użyciu identyfikatora zasobu
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

To polecenie uzyskuje rozmieszczenie o nazwie ContosoRollout w ContosoResourceGroup.

### Przykład 4: uzyskiwanie rozmieszczenia przy użyciu obiektu do rozmieszczenia.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

To polecenie pobiera rozmieszczenie, których nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $rolloutObject.

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

### -Name (nazwa)
Nazwa rozmieszczenia.

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
Próba ponowienia wdrożenia.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout

## WYSYŁA

### Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSRollout

## INFORMACYJN

## LINKI POKREWNE
