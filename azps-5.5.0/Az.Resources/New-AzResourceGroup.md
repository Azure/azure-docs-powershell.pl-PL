---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192730"
---
# New-AzResourceGroup

## SYNOPSIS
Tworzy grupę zasobów platformy Azure.

## SKŁADNIA

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzResourceGroup** tworzy grupę zasobów platformy Azure.
Grupę zasobów można utworzyć, używając tylko nazwy i lokalizacji, a następnie za pomocą polecenia cmdlet New-AzResource utworzyć zasoby w celu dodania ich do grupy zasobów.
Aby dodać wdrożenie do istniejącej grupy zasobów, użyj New-AzResourceGroupDeployment cmdlet. Aby dodać zasób do istniejącej grupy zasobów, użyj polecenia cmdlet **New-AzResource.** Zasób platformy Azure to jednostka platformy Azure zarządzana przez użytkownika, taka jak serwer bazy danych, baza danych lub witryna internetowa. Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.

## PRZYKŁADY

### Przykład 1. Tworzenie pustej grupy zasobów
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

To polecenie tworzy grupę zasobów, która nie ma zasobów. Aby dodać zasoby i wdrożenia do tej grupy zasobów, możesz użyć polecenia cmdlet **New-AzResource** lub **New-AzResourceGroupDeployment.**

### Przykład 2. Tworzenie pustej grupy zasobów przy użyciu parametrów pozytowych
```
PS> New-AzResourceGroup RG01 "South Central US"
```

To polecenie tworzy grupę zasobów, która nie ma zasobów.

### Przykład 3. Tworzenie grupy zasobów z tagami
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

To polecenie tworzy pustą grupę zasobów. To polecenie jest takie samo, jak polecenie w przykładzie 1, z tym wyjątkiem, że przypisuje tagi do grupy zasobów. Pierwszy tag o nazwie Pusty może być używany do identyfikowania grup zasobów, które nie mają zasobów. Drugi tag nosi nazwę Dział i ma wartość Marketing. Do kategoryzowania grup zasobów w celu administrowania lub budżetowania można użyć tagu takiego jak ten.

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

### — Wymuszanie
Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.

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
Określa lokalizację grupy zasobów. Określ lokalizację centrum danych platformy Azure, taką jak Stany Zjednoczone i Azja Południowo-Wschodnia. Grupę zasobów można umieścić w dowolnej lokalizacji. Grupa zasobów nie musi być w tej samej lokalizacji co subskrypcja platformy Azure ani w tej samej lokalizacji co jej zasoby.
Aby określić, która lokalizacja obsługuje poszczególne typy zasobów, użyj Get-AzResourceProvider cmdlet z parametrem *ProviderNamespace.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę grupy zasobów. Nazwa zasobu musi być unikatowa w subskrypcji. Jeśli grupa zasobów o tej nazwie już istnieje, polecenie wyświetli monit o potwierdzenie przed zastąpieniem istniejącej grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
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
Pary klucz-wartość w postaci tabeli skrótu. Na przykład: @{key0="value0";key1=$null;key2="wartość2"} Aby dodać lub zmienić tag, musisz zastąpić kolekcję tagów dla grupy zasobów.
Po przypisaniu tagów do zasobów i grup możesz użyć parametru *Tag* Get-AzResource i Get-AzResourceGroup, aby wyszukiwać zasoby i grupy według nazwy tagu lub według nazwy i wartości. Za pomocą tagów można kategoryzować zasoby( na przykład według działu lub centrum kosztów) albo śledzić notatki lub komentarze dotyczące zasobów.
Aby uzyskać wstępnie zdefiniowane tagi, użyj Get-AzTag cmdlet.

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

### Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroup

## NOTATKI

## LINKI POKREWNE

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
