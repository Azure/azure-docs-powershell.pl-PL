---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365276"
---
# Get-AzTag

## STRESZCZENIe
Pobiera wstępnie zdefiniowane Tagi platformy Azure | Pobiera cały zestaw tagów zasobu lub abonamentu.

## POLECENIA

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis

**GetPredefinedTagSet**: polecenie cmdlet **Get-AzTag** pobiera wstępnie zdefiniowane Tagi platformy Azure w ramach abonamentu.
To polecenie cmdlet zwraca podstawowe informacje o tagach lub szczegółowych informacjach na temat znaczników oraz ich wartości.
Wszystkie obiekty wyjściowe zawierają Właściwość Count oznaczającą liczbę zasobów i grup zasobów, do których zastosowano znaczniki i wartości.
Moduł Tagi platformy Azure, który jest częścią programu **AzTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.
Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.
Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.
Aby utworzyć wstępnie zdefiniowany znacznik, użyj polecenia cmdlet New-AzTag.
Aby zastosować wstępnie zdefiniowany znacznik do grupy zasobów, użyj parametru *tag* polecenia cmdlet New-AzTag.
Aby wyszukać grupy zasobów dla konkretnej nazwy lub nazwy lub wartości znacznika, użyj parametru *tag* polecenia cmdlet Get-AzResourceGroup.

**GetByResourceIdParameterSet**: polecenie cmdlet **Get-AzTag** z identyfikatorem zasobu zasobu lub abonamentem **Pobiera cały** zestaw tagów.

## Przykłady

### Przykład 1. Pobierz wszystkie wstępnie zdefiniowane Tagi
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

To polecenie pobiera wszystkie wstępnie zdefiniowane Tagi w subskrypcji.
Właściwość Count wskazuje, ile razy znacznik został zastosowany do zasobów i grup zasobów w subskrypcji.

### Przykład 2: uzyskiwanie tagu według nazwy
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

To polecenie pobiera szczegółowe informacje na temat znacznika działu i jego wartości.
Właściwość Count wskazuje, ile razy znacznik i każda z jego wartości została zastosowana do zasobów i grup zasobów w subskrypcji.

### Przykład 3: pobieranie wartości ze wszystkich znaczników
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

To polecenie używa parametru *szczegółowy* , aby uzyskać szczegółowe informacje na temat wszystkich wstępnie zdefiniowanych znaczników w subskrypcji.
Użycie parametru *Szczegółowa* jest równoznaczne z użyciem parametru *name* dla każdego znacznika.

### Przykład 4: pobieranie całego zestawu tagów w subskrypcji

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

To polecenie pobiera cały zestaw tagów w subskrypcji przy użyciu programu {subId}.

### Przykład 5: pobieranie całego zestawu tagów w zasobie

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

To polecenie pobiera cały zestaw tagów z zasobu o identyfikatorze {resourceId}.

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

### — Szczegółowe informacje
Wskazuje, że ta operacja dodaje informacje o wartościach znaczników do danych wyjściowych.

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

### -Name (nazwa)
Nazwa wstępnie zdefiniowanego znacznika.
Domyślnie polecenie **Get-AzTag** pobiera podstawowe informacje o wszystkich wstępnie zdefiniowanych znacznikach w subskrypcji.
Gdy jest określany parametr *name* , parametr *szczegółowy* nie ma żadnego wpływu.

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
Identyfikator zasobu oznakowanej jednostki. Zasób, Grupa zasobów lub abonament mogą być oznakowane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
