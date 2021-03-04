---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: 1dcf881fbe0a3a616a7522236099f7698b50a1a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007777"
---
# Get-AzMlWebService

## SYNOPSIS
Pobiera informacje podsumowujące dla jednej lub większej liczby usług sieci Web.

## SKŁADNIA

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Pobiera informacje o definicji usługi sieci Web.
W zależności od przekazanych parametrów polecenie cmdlet zwraca definicję określonej usługi sieci Web, kolekcję definicji usług sieci Web dla określonej grupy zasobów w ramach bieżącej subskrypcji lub kolekcję definicji usług sieci Web w ramach bieżącej subskrypcji.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie szczegółowych informacji o konkretnej usłudze sieci Web
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### Przykład 2. Uzyskiwanie wszystkich zasobów usługi sieci Web w bieżącej subskrypcji
```
Get-AzMlWebService
```

### Przykład 3. Uzyskiwanie wszystkich usług sieci Web w bieżącej subskrypcji i danej grupy zasobów
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
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

### — Nazwa
Nazwa usługi sieci Web, dla której są pobierane szczegóły.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Region
Nazwa regionu

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów, z której są pobierane szczegóły usługi sieci Web.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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
