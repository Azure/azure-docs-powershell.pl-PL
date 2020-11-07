---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: d85767623d88c9fd7d0a00ea98e575953132d3f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719290"
---
# Import-AzureRmMlWebService

## STRESZCZENIe
Importuje obiekt JSON do definicji usługi sieci Web.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### Importowanie z pliku JSON.
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Importowanie z ciągu JSON.
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Import-AzureRmMlWebService polecenia cmdlet Imports, określonego bezpośrednio lub w pliku, do którego istnieje odwołanie, oraz tworzenie obiektu definicji usługi sieci Web, który może zostać przekazany do New-AzureRmMlWebService polecenia cmdlet.

## Przykłady

### --------------------------Przykład 1: Importowanie z ciągu--------------------------
@ {Paragraph = PS C: \\ \> }





```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### --------------------------Przykład 2: Importowanie z ścieżki pliku--------------------------
@ {Paragraph = PS C: \\ \> }





```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## PARAMETRÓW

### -Plik_wejściowy
Ścieżka do pliku zawierającego definicję usługi sieci Web do zaimportowania.

```yaml
Type: System.String
Parameter Sets: Import from JSON file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JsonString
Ciąg sformatowany w notacji JSON zawierający definicję usługi sieci Web do zaimportowania.

```yaml
Type: System.String
Parameter Sets: Import from JSON string.
Aliases: 

Required: True
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

## WYSYŁA

### Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure

## LINKI POKREWNE

