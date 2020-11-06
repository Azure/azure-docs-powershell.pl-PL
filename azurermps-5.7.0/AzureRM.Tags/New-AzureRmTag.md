---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: 77bf93905b0cba4e8f8a23cb9f3cb8945fff74f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550464"
---
# New-AzureRmTag

## STRESZCZENIe
Tworzy wstępnie zdefiniowany tag Azure lub dodaje wartości do istniejącego znacznika.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmTag** tworzy wstępnie zdefiniowany tag Azure z opcjonalną wstępnie zdefiniowaną wartością.
Można go również użyć w celu dodania kolejnych wartości do istniejących wstępnie zdefiniowanych znaczników.
Aby utworzyć wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę znacznika.
Aby dodać wartość do istniejącego wstępnie zdefiniowanego znacznika, określ nazwę istniejącego znacznika i nową wartość.

To polecenie cmdlet zwraca obiekt reprezentujący nowy lub zmodyfikowany znacznik wraz z jego wartościami oraz liczbą zasobów, do których został on zastosowany.

Moduł Tagi platformy Azure, który jest częścią funkcji **New-AzureRmTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.
Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.

Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.
Jeśli subskrypcja zawiera wszystkie wstępnie zdefiniowane Tagi, nie można stosować niezdefiniowanych tagów ani wartości do żadnych zasobów lub grup zasobów w subskrypcji.

Aby zastosować wstępnie zdefiniowany znacznik do zasobu lub grupy zasobów, użyj parametru *tag* polecenia cmdlet New-AzureRmTag.
Aby wyszukać grupy zasobów o określonej nazwie lub nazwie lub wartości znacznika, użyj parametru *tag* polecenia cmdlet Get-AzureRMResourceGroup.

Każdy znacznik ma nazwę.
Wartości są opcjonalne.
Wstępnie zdefiniowany tag platformy Azure może mieć wiele wartości, ale po zastosowaniu znacznika do zasobu lub grupy zasobów należy zastosować nazwę znacznika i tylko jedną z jego wartości.
Możesz na przykład utworzyć wstępnie zdefiniowany tag dział z wartością dla każdego działu, na przykład finanse, zasoby ludzkie i.
Po zastosowaniu znacznika dział do zasobu należy zastosować tylko pojedynczą wstępnie zdefiniowaną wartość, na przykład finanse.

## Przykłady

### Przykład 1. Tworzenie wstępnie zdefiniowanego znacznika
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

To polecenie tworzy wstępnie zdefiniowany znacznik o nazwie FY2015.
Ten tag nie zawiera wartości.
Aby dodać wartości do znacznika, możesz zastosować tag bez wartości do zasobu lub grupy zasobów albo użyć przycisku **New-AzureRmTag** .
Wartość można również określić po zastosowaniu znacznika do grupy zasobów lub zasobów.

### Przykład 2: Tworzenie wstępnie zdefiniowanego znacznika z wartością
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

To polecenie umożliwia utworzenie wstępnie zdefiniowanego tagu o nazwie dział z wartością finansową.

### Przykład 3: Dodawanie wartości do wstępnie zdefiniowanego znacznika
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Te polecenia tworzą wstępnie zdefiniowany tag o nazwie dział z dwiema wartościami.
Jeśli nazwa znacznika istnieje, polecenie **New-AzureRmTag** dodaje wartość do istniejącego znacznika zamiast tworzyć nowy.

### Przykład 4: stosowanie wstępnie zdefiniowanego znacznika
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę znacznika.
Aby utworzyć nowy wstępnie zdefiniowany znacznik, wprowadź unikatową nazwę.

Aby dodać wartość do istniejącego znacznika, wprowadź nazwę istniejącego znacznika.
Jeśli istniejący wstępnie zdefiniowany znacznik ma określoną nazwę, to polecenie **New-AzureRmTag** dodaje określoną wartość (jeśli istnieje) do znacznika o tej nazwie zamiast tworzyć nowy znacznik.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Określa wartość znacznika.
Wstępnie zdefiniowane Tagi mogą zawierać wiele wartości, ale w każdym poleceniu można wprowadzić tylko jedną wartość.
Ten parametr jest opcjonalny, ponieważ znaczniki mogą zawierać imiona i nazwiska bez wartości.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Tags. model. PSTag

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


