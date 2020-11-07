---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: dd115a7d0445a7b07557b884dd2c7413f5269d00
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899044"
---
# New-AzureRmResourceGroup

## STRESZCZENIe
Tworzy grupę zasobów platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmResourceGroup** tworzy grupę zasobów platformy Azure.
Grupę zasobów można utworzyć za pomocą samej nazwy i lokalizacji, a następnie za pomocą polecenia cmdlet New-AzureRmResource utworzyć zasoby, które mają zostać dodane do grupy zasobów.
Aby dodać wdrożenie do istniejącej grupy zasobów, użyj polecenia cmdlet New-AzureRmResourceGroupDeployment. Aby dodać zasób do istniejącej grupy zasobów, użyj polecenia cmdlet **New-AzureRmResource** . Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych lub witryna sieci Web. Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.

## Przykłady

### Przykład 1. Tworzenie pustej grupy zasobów
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

To polecenie tworzy grupę zasobów bez zasobów. Za pomocą poleceń cmdlet **New-AzureRmResource** lub **New-AzureRmResourceGroupDeployment** można dodawać zasoby i wdrożenia do tej grupy zasobów.

### Przykład 2: Tworzenie pustej grupy zasobów przy użyciu parametrów pozycyjnych
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

To polecenie tworzy grupę zasobów bez zasobów.

### Przykład 3: Tworzenie grupy zasobów ze znacznikami
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

To polecenie tworzy pustą grupę zasobów. To polecenie jest takie samo jak w przypadku polecenia z przykładu 1, z wyjątkiem tego, że przypisuje znaczniki do grupy zasobów. Pierwszy znacznik o nazwie Empty może być wykorzystywany do identyfikowania grup zasobów, które nie mają zasobów. Drugi znacznik ma nazwę dział i ma wartość marketingową. Możesz użyć znacznika, takiego jak ten, aby przydzielić grupy zasobów do administrowania lub budżetowania.

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

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

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

### — Lokalizacja
Określa lokalizację grupy zasobów. Określ lokalizację centrum danych platformy Azure, na przykład Azja Zachodnia lub Południowo-Wschodnia. Grupę zasobów można umieścić w dowolnej lokalizacji. Grupa zasobów nie musi znajdować się w tej samej lokalizacji w ramach subskrypcji platformy Azure ani w tej samej lokalizacji co zasoby.
Aby określić, która lokalizacja obsługuje poszczególne typy zasobów, użyj polecenia cmdlet Get-AzureRmResourceProvider z parametrem *ProviderNamespace* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę grupy zasobów. Nazwa zasobu musi być unikatowa w subskrypcji. Jeśli grupa zasobów o tej nazwie już istnieje, polecenie monituje o potwierdzenie przed zastąpieniem istniejącej grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
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
Pary klucz-wartość w formie tabeli skrótów. Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"} aby dodać lub zmienić znacznik, należy zamienić kolekcję znaczników dla grupy zasobów.
Po przypisaniu znaczników do zasobów i grup można użyć parametru *znacznika* Get-AzureRmResource i Get-AzureRmResourceGroup do wyszukiwania zasobów i grup według nazwy znacznika lub według nazwy i wartości. Za pomocą znaczników można klasyfikować zasoby, na przykład według działów lub MPK, a także śledzić notatki i komentarze dotyczące zasobów.
Aby uzyskać wstępnie zdefiniowane Tagi, użyj polecenia cmdlet Get-AzureRMTag.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. ResourceManagement. models. PSResourceGroup

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmResourceProvider](./Get-AzureRmResourceProvider.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Nowe — AzureRmResource](./New-AzureRmResource.md)

[Nowe — AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)
