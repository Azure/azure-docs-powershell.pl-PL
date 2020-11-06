---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 945af88df11e210c3af3a11bd69123dd32befe4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553400"
---
# Get-AzureRmTag

## STRESZCZENIe
Pobiera wstępnie zdefiniowane Tagi platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmTag** pobiera wstępnie zdefiniowane Tagi platformy Azure w ramach abonamentu.
To polecenie cmdlet zwraca podstawowe informacje o tagach lub szczegółowych informacjach na temat znaczników oraz ich wartości.
Wszystkie obiekty wyjściowe zawierają Właściwość Count oznaczającą liczbę zasobów i grup zasobów, do których zastosowano znaczniki i wartości.
Moduł Tagi platformy Azure, który jest częścią programu **AzureRMTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.
Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.
Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.
Aby utworzyć wstępnie zdefiniowany znacznik, użyj polecenia cmdlet New-AzureRmTag.
Aby zastosować wstępnie zdefiniowany znacznik do grupy zasobów, użyj parametru *tag* polecenia cmdlet New-AzureRmTag.
Aby wyszukać grupy zasobów dla konkretnej nazwy lub nazwy lub wartości znacznika, użyj parametru *tag* polecenia cmdlet Get-AzureRMResourceGroup.

## Przykłady

### Przykład 1. Pobierz wszystkie wstępnie zdefiniowane Tagi
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

To polecenie pobiera wszystkie wstępnie zdefiniowane Tagi w subskrypcji.
Właściwość Count wskazuje, ile razy znacznik został zastosowany do zasobów i grup zasobów w subskrypcji.

### Przykład 2: uzyskiwanie tagu według nazwy
```
PS C:\>Get-AzureRmTag -Name "Department"

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
```
PS C:\>Get-AzureRmTag -Detailed

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

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę znacznika, który ma być wyświetlany.
Domyślnie polecenie **Get-AzureRmTag** pobiera podstawowe informacje o wszystkich wstępnie zdefiniowanych znacznikach w subskrypcji.
Gdy jest określany parametr *name* , parametr *szczegółowy* nie ma żadnego wpływu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Commands. resourceName. Common. Tags. PSTag

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmTag](./New-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


