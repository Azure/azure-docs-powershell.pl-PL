---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240075"
---
# Get-AzTag

## SYNOPSIS
Pobiera wstępnie zdefiniowane tagi platformy Azure | Pobiera cały zestaw tagów do zasobu lub subskrypcji.

## SKŁADNIA

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS

**GetPredefinedTagSet:** Polecenie cmdlet **Get-AzTag** pobiera wstępnie zdefiniowane tagi platformy Azure w subskrypcji.
To polecenie cmdlet zwraca podstawowe informacje o tagach lub szczegółowe informacje o tagach i ich wartościach.
Wszystkie obiekty wyjściowe zawierają właściwość Count reprezentującą liczbę zasobów i grup zasobów, do których zastosowano tagi i wartości.
Moduł Azure Tags, do których należy **Get-AzTag,** może ułatwić zarządzanie wstępnie zdefiniowanymi tagami platformy Azure.
Tag Azure to para wartości nazw, za pomocą których można kategoryzować zasoby platformy Azure i grupy zasobów, na przykład według działów lub centrum kosztów, a także śledzić notatki i komentarze dotyczące zasobów i grup.
Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane tagi pozwalają ustalić standardowe, spójne i przewidywalne nazwy oraz wartości tagów w subskrypcji.
Aby utworzyć wstępnie zdefiniowany tag, użyj New-AzTag cmdlet.
Aby zastosować wstępnie zdefiniowany tag do grupy zasobów, użyj parametru *Tag* New-AzTag cmdlet.
Aby wyszukać określoną nazwę tagu lub nazwę i wartość w grupach zasobów, użyj parametru *Tag* Get-AzResourceGroup cmdlet.

**GetByResourceIdParameterSet:** Polecenie cmdlet **Get-AzTag** z tagiem **ResourceId** pobiera cały zestaw tagów dla zasobu lub subskrypcji.

## PRZYKŁADY

### Przykład 1. Pobierz wszystkie wstępnie zdefiniowane tagi
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

To polecenie pobiera wszystkie wstępnie zdefiniowane tagi w subskrypcji.
Właściwość Count pokazuje, ile razy tag został zastosowany do zasobów i grup zasobów w subskrypcji.

### Przykład 2. Uzyskiwanie tagu według nazwy
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

To polecenie pobiera szczegółowe informacje o tagu Dział i jego wartościach.
Właściwość Count pokazuje, ile razy tag i każda z jego wartości zostały zastosowane do zasobów i grup zasobów w subskrypcji.

### Przykład 3. Uzyskiwanie wartości wszystkich tagów
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

To polecenie używa *parametru Szczegółowe* w celu uzyskania szczegółowych informacji o wszystkich wstępnie zdefiniowanych tagach w subskrypcji.
Użycie *parametru Szczegóły* jest równoważne użyciu *parametru Name* dla każdego tagu.

### Przykład 4. Pobierz cały zestaw tagów w subskrypcji

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

To polecenie pobiera cały zestaw tagów subskrypcji za pomocą {subId}.

### Przykład 5. Uzyskiwanie całego zestawu tagów dla zasobu

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

To polecenie pobiera cały zestaw tagów zasobu za pomocą {resourceId}.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Szczegóły
Wskazuje, że ta operacja powoduje dodanie do danych wyjściowych informacji o wartościach tagów.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Nazwa wstępnie zdefiniowanego tagu.
Domyślnie **get-aztag otrzymuje** podstawowe informacje o wszystkich wstępnie zdefiniowanych tagach w subskrypcji.
Określenie parametru *Name (Nazwa)* nie *ma* wpływu na parametr Szczegóły.

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu dla otagowanego elementu. Może zostać otagowany zasób, grupa zasobów lub subskrypcja.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Management.Automation.SwitchParameters

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTATKI

## LINKI POKREWNE

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
