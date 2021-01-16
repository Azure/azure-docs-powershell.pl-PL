---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354826"
---
# Remove-AzTag

## STRESZCZENIe
Usuwa wstępnie zdefiniowane Tagi lub wartości platformy Azure | Usuwa cały zestaw tagów zasobu lub abonamentu.

## POLECENIA

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## Opis

**RemovePredefinedTagSet**: polecenie cmdlet **Remove-AzTag** usuwa wstępnie zdefiniowane Tagi i wartości platformy Azure z subskrypcji.
Aby usunąć określone wartości ze wstępnie zdefiniowanego znacznika, należy użyć parametru *Value* .
Domyślnie polecenie **Remove-AzTag** usuwa określony znacznik i wszystkie jego wartości. Nie można usunąć znacznika lub wartości, która jest obecnie zastosowana do zasobu lub grupy zasobów.
Przed użyciem polecenia **Remove-AzTag** Użyj parametru *Tag* polecenia cmdlet Set-AzResourceGroup, aby usunąć znacznik lub wartości z grupy zasób lub zasób.
Moduł Tagi platformy Azure, który jest częścią funkcji **Remove-AzTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.
Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.
Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.

**RemoveByResourceIdParameterSet**: polecenie cmdlet **Remove-AzTag** z identyfikatorem **ResourceID** powoduje usunięcie całego zestawu tagów w zasobie lub subskrypcji.

## Przykłady

### Przykład 1. Usuń wstępnie zdefiniowany tag
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

To polecenie powoduje usunięcie wstępnie zdefiniowanego tagu o nazwie dział i wszystkich jego wartości.
Jeśli znacznik został zastosowany do żadnych zasobów lub grup zasobów, wykonanie polecenia nie powiodło się.

### Przykład 2: usuwanie wartości ze wstępnie zdefiniowanego znacznika
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

To polecenie usuwa wartość HumanResources ze znacznika uprzednio zdefiniowanego działu.
Nie powoduje usunięcia znacznika.
Jeśli wartość została zastosowana do żadnych zasobów lub grup zasobów, wykonanie polecenia nie powiodło się.

### Przykład 3: usunięcie całego zestawu tagów w subskrypcji

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

To polecenie usuwa cały zestaw tagów z subskrypcji przy użyciu programu {subId}. Nie zwróci on usuniętego obiektu, jeśli nie przejdzie w "-PassThru".

### Przykład 4: usuwanie całego zestawu tagów w zasobie

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

To polecenie usuwa cały zestaw tagów z zasobu o identyfikatorze {resourceId}. Funkcja zwraca usunięte oject podczas przekazywania "-PassThru".

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

### -Name (nazwa)
Określa nazwę wstępnie zdefiniowanego tagu do usunięcia.
Domyślnie polecenie **Remove-AzTag** usuwa określony znacznik i wszystkie jego wartości.
Aby usunąć zaznaczone wartości, ale nie usuwać znacznika, użyj parametru *Value* .

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Usuwa określone wartości ze wstępnie zdefiniowanego znacznika, ale nie usuwa znacznika.

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu oznakowanej jednostki. Zasób, Grupa zasobów lub abonament mogą być oznakowane.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Zwraca obiekt reprezentujący usunięty znacznik lub wynikowy znacznik z usuniętymi wartościami.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. String []

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource

## INFORMACYJN

## LINKI POKREWNE

[Get-AzTag](./Get-AzTag.md)

[Nowe — AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)