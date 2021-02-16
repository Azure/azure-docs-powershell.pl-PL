---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185146"
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
Import Import-AzMlWebService cmdlet, określony bezpośrednio lub w pliku odwołania, i tworzy obiekt definicji usługi sieci Web, który może być przekazywany do New-AzMlWebService cmdlet.

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

## OUTPUTS

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## NOTATKI
Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml

## LINKI POKREWNE
