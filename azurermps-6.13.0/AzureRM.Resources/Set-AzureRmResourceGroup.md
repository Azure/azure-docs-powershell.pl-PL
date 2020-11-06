---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: 4ba57d1f8e1abe8c506f1bcd6625a7a90551f164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552547"
---
# Set-AzureRmResourceGroup

## STRESZCZENIe
Modyfikuje grupę zasobów.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### SetByResourceGroupName (domyślny)
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmResourceGroup** modyfikuje właściwości grupy zasobów.
Za pomocą tego polecenia cmdlet można dodawać, zmieniać i usuwać Tagi platformy Azure zastosowane do grupy zasobów.
Określ parametr *name (nazwa* ), aby zidentyfikować grupę zasobów i parametr *znacznika* , aby zmodyfikować znaczniki.
Za pomocą tego polecenia cmdlet można zmienić nazwę grupy zasobów.

## Przykłady

### Przykład 1. Stosowanie znacznika do grupy zasobów
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

To polecenie powoduje zastosowanie znacznika działu z wartością do grupy zasobów bez istniejących tagów.

### Przykład 2: Dodawanie znaczników do grupy zasobów
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

W tym przykładzie dodano znacznik statusu z wartością zatwierdzony i tag FY2016 do grupy zasobów zawierającej istniejące znaczniki. Ponieważ znaczniki, które określisz, zastępują istniejące znaczniki, należy uwzględnić istniejące znaczniki w nowej kolekcji znaczników lub je utracić.
Pierwsze polecenie pobiera grupę zasobów ContosoRG i używa metody z kropką w celu uzyskania wartości właściwości znaczników. Polecenie zapisuje znaczniki w zmiennej $Tags.
Drugie polecenie pobiera znaczniki ze zmiennej $Tags.
W trzecim poleceniu użyto operatora + =, aby dodać znaczniki statusu i FY2016 do tablicy znaczników w zmiennej $Tags.
W czwartym poleceniu *Tag* użyto parametru tag **Set-AzureRmResourceGroup** w celu zastosowania znaczników w zmiennej $Tags do grupy zasobów ContosoRG.
W piątym poleceniu są pobierane wszystkie Tagi zastosowane do grupy zasobów ContosoRG. Wyjście wskazuje, że grupa zasobów zawiera tag dział, a dwa nowe tagi, stan i FY2015.

### Przykład 3: Usuwanie wszystkich znaczników grupy zasobów
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

To polecenie określa parametr *znacznika* z pustą wartością tabeli skrótów, aby usunąć wszystkie Tagi z grupy zasobów ContosoRG.

## PARAMETRÓW

### -ApiVersion
Określa wersję API obsługiwaną przez dostawcę zasobów.
Możesz określić inną wersję niż wersja domyślna.

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -ID
Określa identyfikator grupy zasobów do zmodyfikowania.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę grupy zasobów do zmodyfikowania.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Pary klucz-wartość w formie tabeli skrótów. Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"} tag to para nazwa-wartość, którą można tworzyć i stosować do zasobów i grup zasobów. Po przypisaniu znaczników do zasobów i grup można użyć parametru *znacznika* Get-AzureRmResource i Get-AzureRmResourceGroup do wyszukiwania zasobów i grup według nazwy lub nazwy lub wartości znacznika. Za pomocą znaczników można klasyfikować zasoby, na przykład według działów lub MPK, a także śledzić notatki i komentarze dotyczące zasobów.
Aby dodać lub zmienić znacznik, należy zamienić kolekcję znaczników dla grupy zasobów. Aby usunąć znacznik, wprowadź tabelę skrótów zawierającą wszystkie znaczniki, które są obecnie stosowane do grupy zasobów, z poziomu **Get-AzureRmResourceGroup** , z wyjątkiem znacznika, który chcesz usunąć. Aby usunąć wszystkie znaczniki z grupy zasobów, określ pustą tabelę skrótów: `@{}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
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

### Microsoft. Azure. Commands. resources. models. PSResourceGroup

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmResource](./Get-AzureRmResource.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Nowe — AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)
