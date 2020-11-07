---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: f51411c4683a79283ad5e0a73554f6db3ce7e52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716470"
---
# Remove-AzureRmTag

## STRESZCZENIe
Usuwa wstępnie zdefiniowane Tagi lub wartości platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureRmTag** usuwa wstępnie zdefiniowane Tagi i wartości platformy Azure z subskrypcji.
Aby usunąć określone wartości ze wstępnie zdefiniowanego znacznika, należy użyć parametru *Value* .
Domyślnie polecenie **Remove-AzureRmTag** usuwa określony znacznik i wszystkie jego wartości. Nie można usunąć znacznika lub wartości, która jest obecnie zastosowana do zasobu lub grupy zasobów.

Przed użyciem polecenia **Remove-AzureRmTag** Użyj parametru *Tag* polecenia cmdlet Set-AzureRMResourceGroup, aby usunąć znacznik lub wartości z grupy zasób lub zasób.

Moduł Tagi platformy Azure, który jest częścią funkcji **Remove-AzureRmTag** , może pomóc w zarządzaniu wstępnie zdefiniowanymi tagami platformy Azure.
Tag Azure to para nazwa-wartość, która umożliwia kategoryzowanie zasobów platformy Azure i grup zasobów, na przykład według działów lub MPK, oraz śledzenie notatek i komentarzy dotyczących zasobów i grup.

Tagi można definiować i stosować w jednym kroku, ale wstępnie zdefiniowane znaczniki umożliwiają ustalenie standardowych, spójnych, przewidywalnych nazw i wartości znaczników w subskrypcji.
Jeśli subskrypcja zawiera wszystkie wstępnie zdefiniowane Tagi, nie można stosować niezdefiniowanych tagów ani wartości do żadnych zasobów lub grup zasobów w subskrypcji.

## Przykłady

### Przykład 1. Usuń wstępnie zdefiniowany tag
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

To polecenie powoduje usunięcie wstępnie zdefiniowanego tagu o nazwie dział i wszystkich jego zasobów.
Jeśli znacznik został zastosowany do żadnych zasobów lub grup zasobów, wykonanie polecenia nie powiodło się.

### Przykład 2: usuwanie wartości ze wstępnie zdefiniowanego znacznika
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
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
Określa nazwę znacznika, który ma zostać usunięty.
Domyślnie polecenie **Remove-AzureRmTag** usuwa określony znacznik i wszystkie jego wartości.
Aby usunąć zaznaczone wartości, ale nie usuwać znacznika, użyj parametru *Value* .

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

### -PassThru
Zwraca obiekt reprezentujący usunięty znacznik lub wynikowy znacznik z usuniętymi wartościami.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Usuwa określone wartości ze wstępnie zdefiniowanego znacznika, ale nie usuwa znacznika.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Brak lub Microsoft. Azure. Commands. Tags. model. PSTag

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Nowe — AzureRmTag](./New-AzureRmTag.md)


