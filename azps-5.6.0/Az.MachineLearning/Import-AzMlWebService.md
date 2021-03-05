---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: e30ecc151da5e4a202b8da63f8d57a8f25c387dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961873"
---
# Import-AzMlWebService

## SYNOPSIS
Importuje obiekt JSON do definicji usługi sieci Web.

## SKŁADNIA

### ImportFromJSONFile
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ImportFromJSONString.
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Import Import-AzMlWebService cmdlet określony bezpośrednio lub w pliku, do których odwołuje się odwołanie, i tworzy obiekt definicji usługi sieci Web, który może być przekazywany do New-AzMlWebService cmdlet.

## PRZYKŁADY

### Przykład 1. Importowanie z ciągu
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### Przykład 2. Importowanie ze ścieżki pliku
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

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

### -InputFile
Ścieżka do pliku zawierającego definicję usługi sieci Web do zaimportowania.

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JsonString
Sformatowany ciąg JSON zawierający definicję usługi sieci Web do zaimportowania.

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## NOTATKI
Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml

## LINKI POKREWNE
