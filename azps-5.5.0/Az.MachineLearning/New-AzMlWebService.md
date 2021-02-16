---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190298"
---
# New-AzMlWebService

## SYNOPSIS
Tworzy nową usługę sieci Web.

## SKŁADNIA

### CreateFromFile
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Tworzy usługę internetową Azure Machine Learning w istniejącej grupie zasobów.
Jeśli w grupie zasobów istnieje usługa sieci Web o takiej samej nazwie, połączenie działa jako operacja aktualizacji, a istniejąca usługa sieci Web jest zastępowana.

## PRZYKŁADY

### Przykład 1. Tworzenie nowej usługi na podstawie definicji pliku Jsona
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Tworzy nową usługę internetową Azure Machine Learning o nazwie "mywebservicename" w grupie "myresourcegroup" i regionie Południowo-środkowych Stanów Zjednoczonych na podstawie definicji z pliku json, do których następuje odwołanie.

### Przykład 2. Tworzenie nowej usługi z wystąpienia obiektu
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Wystąpienie obiektu usługi sieci Web można uzyskać w celu dostosowania przed opublikowaniem jako zasób za pomocą Import-AzMlWebService cmdlet.

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

### -DefinitionFile
Określa ścieżkę do pliku zawierającego definicję formatu JSON usługi sieci Web.
Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji swaggera w obszarze https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Wymuszanie
Nie pytaj o potwierdzenie.

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

### — Lokalizacja
Region usługi sieci Web.
Wprowadź region centrum danych platformy Azure, na przykład "Stany Zjednoczone Zachód" lub "Azja Południowo-Wschodnia".
Usługę sieci Web można umieścić w dowolnym regionie, który obsługuje zasoby tego typu.
Usługa sieci Web nie musi być w tym samym regionie, w których jest subskrybowanie platformy Azure, ani w tym samym regionie co grupa zasobów.
Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.
Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzResourceProvider z poleceniem cmdlet parametru ProviderNamespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Nazwa usługi sieci Web.
Nazwa musi być unikatowa w grupie zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
Definicja nowej usługi sieci Web zawierająca wszystkie właściwości, które ją zawierają.
Ten parametr jest wymagany i reprezentuje wystąpienie klasy Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.
Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji swaggera w obszarze https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów, w której ma być umieszczana usługa sieci Web.
Wprowadź region centrum danych platformy Azure, na przykład "Stany Zjednoczone Zachód" lub "Azja Południowo-Wschodnia".
Usługę sieci Web można umieścić w dowolnym regionie, który obsługuje zasoby tego typu.
Usługa sieci Web nie musi być w tym samym regionie, w których jest subskrybowanie platformy Azure, ani w tym samym regionie co grupa zasobów.
Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.
Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzResourceProvider z poleceniem cmdlet parametru ProviderNamespace.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## NOTATKI
Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml

## LINKI POKREWNE
