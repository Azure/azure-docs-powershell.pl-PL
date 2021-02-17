---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183642"
---
# Set-AzResourceGroup

## SYNOPSIS
Modyfikuje grupę zasobów.

## SKŁADNIA

### SetByResourceGroupName (Domyślna)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Set-AzResourceGroup** modyfikuje właściwości grupy zasobów.
To polecenie cmdlet umożliwia dodawanie, zmienianie i usuwanie tagów platformy Azure zastosowanych do grupy zasobów.
Określ parametr *Name (Nazwa),* aby zidentyfikować grupę zasobów, oraz *parametr Tag* w celu zmodyfikowania tagów.
Za pomocą tego polecenia cmdlet nie można zmienić nazwy grupy zasobów.

## PRZYKŁADY

### Przykład 1. Stosowanie tagu do grupy zasobów
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

To polecenie powoduje zastosowanie tagu Dział z wartością IT do grupy zasobów, która nie ma istniejących tagów.

### Przykład 2. Dodawanie tagów do grupy zasobów
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

W tym przykładzie do grupy zasobów, która ma istniejące tagi, dodano tag stanu z wartością Zatwierdzony i tag roku 2016. Ponieważ określone tagi zastępują istniejące tagi, musisz uwzględnić istniejące tagi w nowej kolekcji tagów lub je utracisz.
Pierwsze polecenie pobiera grupę zasobów ContosoRG i używa metody kropki w celu uzyskania wartości właściwości Tagi. To polecenie przechowuje tagi w $Tags zmienną.
Drugie polecenie pobiera tagi w $Tags zmienną.
Trzecie polecenie używa operatora przydziału += w celu dodania tagów Status i FY2016 do tablicy tagów w $Tags zadania.
Czwarte polecenie używa *parametru Tag* **set-AzResourceGroup** w celu zastosowania tagów w zmiennej $Tags do grupy zasobów ContosoRG.
Piąte polecenie pobiera wszystkie tagi zastosowane do grupy zasobów ContosoRG. Wynik pokazuje, że grupa zasobów ma tag Dział oraz dwa nowe tagi: Stan i ROK2015.

### Przykład 3. Usuwanie wszystkich tagów dla grupy zasobów
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

To polecenie określa *parametr Tag z* pustą wartością tabeli skrótu, aby usunąć wszystkie tagi z grupy zasobów ContosoRG.

## PARAMETERS

### -ApiVersion
Określa wersję interfejsu API obsługiwaną przez dostawcę zasobów.
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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — Identyfikator
Określa identyfikator grupy zasobów do zmodyfikowania.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę grupy zasobów do zmodyfikowania.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Przed
Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.

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

### — Tag
Pary klucz-wartość w postaci tabeli skrótu. Na przykład: @{key0="value0";key1=$null;key2="value2"} Tag to para wartości nazwy, która można utworzyć i zastosować do zasobów i grup zasobów. Po przypisaniu tagów do zasobów i grup możesz użyć parametru *Tag* Get-AzResource i Get-AzResourceGroup, aby wyszukiwać zasoby i grupy według nazwy tagu lub nazwy i wartości. Za pomocą tagów można kategoryzować zasoby( na przykład według działu lub centrum kosztów) albo śledzić notatki lub komentarze dotyczące zasobów.
Aby dodać lub zmienić tag, musisz zastąpić kolekcję tagów grupy zasobów. Aby usunąć tag, wprowadź tabelę skrótów ze wszystkimi tagami zastosowanymi obecnie do grupy zasobów z grupy **Get-AzResourceGroup,** z wyjątkiem tagu, który chcesz usunąć. Aby usunąć wszystkie tagi z grupy zasobów, określ pustą tabelę `@{}` skrótów:

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroup

## NOTATKI

## LINKI POKREWNE

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
