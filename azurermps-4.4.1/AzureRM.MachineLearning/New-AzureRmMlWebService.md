---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 1fe6476836622445337ea0b4741b361504a57302
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553839"
---
# New-AzureRmMlWebService

## STRESZCZENIe
Tworzy nową usługę sieci Web.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Utwórz nową usługę sieci Web usługi Azure ML z pliku Definiton JSON.
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Utwórz nową usługę sieci Web Azure ML z definicji wystąpienia usługi WebService.
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Tworzy usługę sieci Web Azure Machine Learning w istniejącej grupie zasobów.
Jeśli w grupie zasobów istnieje usługa sieci Web o tej samej nazwie, to połączenie działa jako operacja aktualizacji, a istniejąca usługa sieci Web zostanie zastąpiona.

## Przykłady

### --------------------------Przykład 1: Tworzenie nowej usługi na podstawie definicji pliku JSON--------------------------
@ {Paragraph = PS C: \\ \> }





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Tworzy nową usługę sieci Web Azure Machine Learning o nazwie "" w grupie "Moja zasobów" i w Południowo-środkowe region w Stanach Zjednoczonych na podstawie definicji obecnej w pliku JSON odwołania.

### --------------------------Przykład 2: Tworzenie nowej usługi z wystąpienia obiektu--------------------------
@ {Paragraph = PS C: \\ \> }





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Za pomocą polecenia cmdlet Import-AzureRmMlWebService można uzyskać wystąpienie obiektu usługi sieci Web w celu dostosowania przed opublikowaniem jako zasobu.

## PARAMETRÓW

### -DefinitionFile
Specifes ścieżkę do pliku zawierającego definicję formatu JSON usługi sieci Web.
Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji struktury Swagger w obszarze https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: System.String
Parameter Sets: Create a new Azure ML webservice from a JSON definiton file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
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
Wprowadź region centrum danych platformy Azure, na przykład "zachodni USA" lub "Południowo-Wschodnia".
Usługę sieci Web można umieścić w dowolnym regionie obsługującym zasoby tego typu.
Usługa sieci Web nie musi znajdować się w tym samym regionie subskrypcji platformy Azure ani w tym samym regionie co grupa zasobów.
Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.
Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzureRmResourceProvider za pomocą polecenia cmdlet parametru ProviderNamespace.

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

### -Name (nazwa)
Nazwa usługi sieci Web.
Nazwa musi być unikatowa w grupie zasób.

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
Definicja nowej usługi sieci Web zawierająca wszystkie właściwości, które tworzą usługę.
Ten parametr jest wymagany i reprezentuje wystąpienie klasy Microsoft. Azure. Management. MachineLearning. WebServices. models. WebService.
Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji struktury Swagger w obszarze https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów, w której ma zostać umieszczona usługa sieci Web.
Wprowadź region centrum danych platformy Azure, na przykład "zachodni USA" lub "Południowo-Wschodnia".
Usługę sieci Web można umieścić w dowolnym regionie obsługującym zasoby tego typu.
Usługa sieci Web nie musi znajdować się w tym samym regionie subskrypcji platformy Azure ani w tym samym regionie co grupa zasobów.
Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.
Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzureRmResourceProvider za pomocą polecenia cmdlet parametru ProviderNamespace.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Usług
Parametr "NewWebServiceDefinition" akceptuje wartość typu "WebService" z procesu

## WYSYŁA

### Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService
Skrócony opis usługi sieci Web Azure Machine Learning.
Podobny do opisu zwróconego przez wywołanie polecenia cmdlet Get-AzureRmMlWebService w istniejącej usłudze sieci Web.
Ten opis nie zawiera poufnych właściwości, takich jak poświadczenia konta magazynu i klucze dostępu usługi.

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure

## LINKI POKREWNE

