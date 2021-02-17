---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183651"
---
# New-AzTag

## SYNOPSIS
Tworzy wstępnie zdefiniowany tag platformy Azure lub dodaje wartości do istniejącego tagu | Tworzy lub aktualizuje cały zestaw tagów dla zasobu lub subskrypcji.

## SKŁADNIA

### CreatePredefinedTagParameterSet

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateByResourceIdParameterSet

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## OPIS

**CreatePredefinedTagSet:** polecenie cmdlet **New-AzTag** tworzy wstępnie zdefiniowany tag platformy Azure z opcjonalną wstępnie zdefiniowaną wartością.
Za jego pomocą można również dodawać dodatkowe wartości do istniejących wstępnie zdefiniowanych tagów.
Aby utworzyć wstępnie zdefiniowany tag, wprowadź unikatową nazwę tagu.
Aby dodać wartość do istniejącego wstępnie zdefiniowanego tagu, określ nazwę istniejącego tagu i nową wartość.
To polecenie cmdlet zwraca obiekt reprezentujący nowy lub zmodyfikowany tag wraz z wartościami i liczbą zasobów, do których został zastosowany.
Moduł Tagi platformy Azure, do których należy program **New-AzTag,** może ułatwić zarządzanie wstępnie zdefiniowanymi tagami platformy Azure.
Tag Azure to para wartości nazw, za pomocą których można kategoryzować zasoby platformy Azure i grupy zasobów, na przykład według działów lub centrum kosztów, a także śledzić notatki i komentarze dotyczące zasobów i grup.
Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane tagi pozwalają ustalić standardowe, spójne i przewidywalne nazwy oraz wartości tagów w subskrypcji.
Aby zastosować wstępnie zdefiniowany tag do zasobu lub grupy zasobów, użyj parametru *Tag* New-AzTag cmdlet.
Aby wyszukać grupy zasobów z określoną nazwą tagu lub nazwą i wartością, użyj parametru *Tag* Get-AzResourceGroup cmdlet.
Każdy tag ma nazwę.
Wartości są opcjonalne.
Wstępnie zdefiniowany tag platformy Azure może mieć wiele wartości, ale po zastosowaniu tagu do zasobu lub grupy zasobów należy zastosować nazwę tagu i tylko jedną z jej wartości.
Można na przykład utworzyć wstępnie zdefiniowany tag Dział z wartością dla każdego działu, takiego jak Finanse, Kadry i DZIAŁ IT.
Po zastosowaniu tagu Dział do zasobu stosuje się tylko jedną wstępnie zdefiniowaną wartość, na przykład Finanse.

**CreateByResourceIdParameterSet:** Polecenie cmdlet **New-AzTag** z tagiem **ResourceId** tworzy lub aktualizuje cały zestaw tagów dla zasobu lub subskrypcji.
Ta operacja umożliwia dodanie lub zastąpienie całego zestawu tagów dla określonego zasobu lub subskrypcji. Określona jednostka może mieć maksymalnie 50 tagów.

## PRZYKŁADY

### Przykład 1. Tworzenie wstępnie zdefiniowanego tagu
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

To polecenie tworzy wstępnie zdefiniowany tag o nazwie ROK2015.
Ten tag nie ma wartości.
Do zasobu lub grupy zasobów można zastosować tag bez wartości albo dodać wartości do tagu przy użyciu tagu **Nowy-AzTag.**
Wartość można także określić podczas stosowania tagu do zasobu lub grupy zasobów.

### Przykład 2. Tworzenie wstępnie zdefiniowanego tagu z wartością
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

To polecenie tworzy wstępnie zdefiniowany tag o nazwie Dział o wartości Finanse.

### Przykład 3. Dodawanie wartości do wstępnie zdefiniowanego tagu
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Te polecenia tworzą wstępnie zdefiniowany tag o nazwie Dział z dwiema wartościami.
Jeśli nazwa tagu istnieje, **nowy-aztag** dodaje wartość do istniejącego tagu, zamiast tworzyć nowy.

### Przykład 4. Używanie wstępnie zdefiniowanego tagu
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

Polecenia w tym przykładzie tworzą i używają wstępnie zdefiniowanego tagu.

### Przykład 5. Tworzenie lub aktualizacja całego zestawu tagów w subskrypcji

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

To polecenie tworzy lub aktualizuje cały zestaw tagów subskrypcji za pomocą {subId}.

### Przykład 6. Tworzenie lub aktualizacja całego zestawu tagów dla zasobu

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

To polecenie tworzy lub aktualizuje cały zestaw tagów zasobu za pomocą {resourceId}.

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
Określa wstępnie zdefiniowaną nazwę tagu.
Aby utworzyć nowy wstępnie zdefiniowany tag, wprowadź unikatową nazwę.
Aby dodać wartość do istniejącego tagu, wprowadź nazwę istniejącego tagu.
Jeśli istniejący wstępnie zdefiniowany tag ma określoną nazwę, element **New-AzTag** doda określoną wartość (o ile taki tag się znajduje) do tagu o tej nazwie, zamiast tworzyć nowy tag.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wartość
Określa wstępnie zdefiniowaną wartość tagu.
Wstępnie zdefiniowane tagi mogą mieć wiele wartości, ale w każdym z poleceń można wprowadzić tylko jedną wartość.
Ten parametr jest opcjonalny, ponieważ tagi mogą mieć nazwy bez wartości.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu dla otagowanego podmiotu. Może zostać otagowany zasób, grupa zasobów lub subskrypcja.

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tag
Tagi, które mają być umieszczane dla zasobu.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
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

### System.Collections.Hashtable

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTATKI

## LINKI POKREWNE

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)