---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189219"
---
# Remove-AzTag

## SYNOPSIS
Usuwa wstępnie zdefiniowane tagi lub wartości | Usuwa cały zestaw tagów dla zasobu lub subskrypcji.

## SKŁADNIA

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

## OPIS

**RemovePredefinedTagSet:** Polecenie cmdlet **Remove-AzTag** usuwa wstępnie zdefiniowane tagi i wartości platformy Azure z subskrypcji.
Aby usunąć określone wartości ze wstępnie zdefiniowanego tagu, użyj *parametru Value.*
Domyślnie **remove-aztag** usuwa określony tag i wszystkie jego wartości. Nie można usunąć tagu ani wartości, które są obecnie stosowane do zasobu lub grupy zasobów.
Przed użyciem **polecenia Remove-AzTag** użyj parametru *Tag* Set-AzResourceGroup cmdlet, aby usunąć tag lub wartości z zasobu lub grupy zasobów.
Moduł Tagi platformy Azure, do których należy **remove-aztag,** może ułatwić zarządzanie wstępnie zdefiniowanymi tagami platformy Azure.
Tag Azure to para wartości nazw, za pomocą których można kategoryzować zasoby platformy Azure i grupy zasobów, na przykład według działów lub centrum kosztów, a także śledzić notatki i komentarze dotyczące zasobów i grup.
Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane tagi pozwalają ustalić standardowe, spójne i przewidywalne nazwy oraz wartości tagów w subskrypcji.

**RemoveByResourceIdParameterSet:** Polecenie cmdlet **Remove-AzTag** z tagiem **ResourceId** usuwa cały zestaw tagów zasobu lub subskrypcji.

## PRZYKŁADY

### Przykład 1. Usuwanie wstępnie zdefiniowanego tagu
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

To polecenie usuwa wstępnie zdefiniowany tag o nazwie Dział i wszystkie jego wartości.
Jeśli tag został zastosowany do jakichkolwiek zasobów lub grup zasobów, polecenie kończy się niepowodzeniem.

### Przykład 2. Usuwanie wartości ze wstępnie zdefiniowanego tagu
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

To polecenie usuwa wartość HumanResources ze wstępnie zdefiniowanego tagu Department (Dział).
Tag nie jest usuwany.
Jeśli wartość została zastosowana do jakichkolwiek zasobów lub grup zasobów, polecenie kończy się niepowodzeniem.

### Przykład 3. Usuwanie całego zestawu tagów w subskrypcji

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

To polecenie spowoduje usunięcie całego zestawu tagów w subskrypcji za pomocą {subId}. Nie zwróci on usuniętego obiektu, jeśli nie przejdzie w "-PassThru".

### Przykład 4. Usuwanie całego zestawu tagów zasobu

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

To polecenie usuwa cały zestaw tagów zasobu za pomocą {resourceId}. Zwraca usunięty oject podczas przechodzenia w "-PassThru".

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

### — Nazwa
Określa nazwę wstępnie zdefiniowanego tagu do usunięcia.
Domyślnie **remove-aztag** usuwa określony tag i wszystkie jego wartości.
Aby usunąć wybrane wartości, ale nie usunąć tagu, użyj *parametru Value.*

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

### — Wartość
Usuwa określone wartości ze wstępnie zdefiniowanego tagu, ale nie usuwa tagu.

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
Identyfikator zasobu dla otagowanego elementu. Może zostać otagowany zasób, grupa zasobów lub subskrypcja.

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
Zwraca obiekt reprezentujący usunięty tag lub końcowy tag z usuniętymi wartościami.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.String[]

### System.Management.Automation.SwitchParameters

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTATKI

## LINKI POKREWNE

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)