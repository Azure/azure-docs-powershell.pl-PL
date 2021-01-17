---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365869"
---
# New-AzTag

## STRESZCZENIe
Tworzy wstępnie zdefiniowany tag Azure lub dodaje wartości do istniejącego tagu | Umożliwia utworzenie lub zaktualizowanie całego zestawu tagów zasobu lub abonamentu.

## POLECENIA

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

## Opis

**CreatePredefinedTagSet**: polecenie cmdlet **New-AzTag** tworzy wstępnie zdefiniowany tag Azure z opcjonalną wstępnie zdefiniowaną wartością.
Można go również użyć w celu dodania kolejnych wartości do istniejących wstępnie zdefiniowanych znaczników.
Aby utworzyć wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę znacznika.
Aby dodać wartość do istniejącego wstępnie zdefiniowanego znacznika, określ nazwę istniejącego znacznika i nową wartość.
To polecenie cmdlet zwraca obiekt reprezentujący nowy lub zmodyfikowany znacznik wraz z jego wartościami oraz liczbą zasobów, do których został on zastosowany.
Moduł Tagi platformy Azure, który jest częścią funkcji **New-AzTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.
Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.
Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.
Aby zastosować wstępnie zdefiniowany znacznik do zasobu lub grupy zasobów, użyj parametru *tag* polecenia cmdlet New-AzTag.
Aby wyszukać grupy zasobów o określonej nazwie lub nazwie lub wartości znacznika, użyj parametru *tag* polecenia cmdlet Get-AzResourceGroup.
Każdy znacznik ma nazwę.
Wartości są opcjonalne.
Wstępnie zdefiniowany tag platformy Azure może mieć wiele wartości, ale po zastosowaniu znacznika do zasobu lub grupy zasobów należy zastosować nazwę znacznika i tylko jedną z jego wartości.
Możesz na przykład utworzyć wstępnie zdefiniowany tag dział z wartością dla każdego działu, na przykład finanse, zasoby ludzkie i.
Po zastosowaniu znacznika dział do zasobu należy zastosować tylko pojedynczą wstępnie zdefiniowaną wartość, na przykład finanse.

**CreateByResourceIdParameterSet**: polecenie cmdlet **New-AzTag** z identyfikatorem **ResourceID** powoduje utworzenie lub zaktualizowanie całego zestawu tagów w zasobie lub subskrypcji.
Ta operacja umożliwia dodawanie lub zamienianie całego zestawu tagów w określonym zasobie lub subskrypcji. Określona encja może zawierać maksymalnie 50 tagów.

## Przykłady

### Przykład 1. Tworzenie wstępnie zdefiniowanego znacznika
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

To polecenie tworzy wstępnie zdefiniowany znacznik o nazwie FY2015.
Ten tag nie zawiera wartości.
Aby dodać wartości do znacznika, możesz zastosować tag bez wartości do zasobu lub grupy zasobów albo użyć przycisku **New-AzTag** .
Wartość można również określić po zastosowaniu znacznika do grupy zasobów lub zasobów.

### Przykład 2: Tworzenie wstępnie zdefiniowanego znacznika z wartością
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

To polecenie umożliwia utworzenie wstępnie zdefiniowanego tagu o nazwie dział z wartością finansową.

### Przykład 3: Dodawanie wartości do wstępnie zdefiniowanego znacznika
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

Te polecenia tworzą wstępnie zdefiniowany tag o nazwie dział z dwiema wartościami.
Jeśli nazwa znacznika istnieje, polecenie **New-AzTag** dodaje wartość do istniejącego znacznika zamiast tworzyć nowy.

### Przykład 4: stosowanie wstępnie zdefiniowanego znacznika
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

Polecenia w tym przykładzie tworzą i używają wstępnie zdefiniowanego znacznika.

### Przykład 5: Tworzenie lub aktualizowanie całego zestawu tagów w subskrypcji

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

To polecenie powoduje utworzenie lub zaktualizowanie całego zestawu tagów w subskrypcji przy użyciu programu {subId}.

### Przykład 6: Tworzenie lub aktualizowanie całego zestawu tagów w zasobie

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

To polecenie umożliwia utworzenie lub zaktualizowanie całego zestawu tagów w zasobie za pomocą zasobu {resourceId}.

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
Określa wstępnie zdefiniowaną nazwę znacznika.
Aby utworzyć nowy wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę.
Aby dodać wartość do istniejącego znacznika, wprowadź nazwę istniejącego znacznika.
Jeśli istniejący wstępnie zdefiniowany znacznik ma określoną nazwę, to polecenie **New-AzTag** dodaje określoną wartość (jeśli istnieje) do znacznika o tej nazwie zamiast tworzyć nowy znacznik.

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

### -Value
Określa wstępnie zdefiniowaną wartość znacznika.
Wstępnie zdefiniowane Tagi mogą zawierać wiele wartości, ale w każdym poleceniu można wprowadzić tylko jedną wartość.
Ten parametr jest opcjonalny, ponieważ znaczniki mogą zawierać imiona i nazwiska bez wartości.

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
Identyfikator zasobu oznakowanej jednostki. Zasób, Grupa zasobów lub abonament mogą być oznakowane.

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

### -Tag
Tagi, które mają zostać umieszczone w zasobie.

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

### System. Collections. Hashtable

## WYSYŁA

### Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. model. PSTagResource

## INFORMACYJN

## LINKI POKREWNE

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)